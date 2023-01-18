## 🔎 **싱글톤 패턴이란❓**

![image](https://user-images.githubusercontent.com/96826217/213198696-80b8c63d-dab9-48d1-a5b9-72faa10cc261.png)


클래스의 오브젝트 개수를 제한시키는 방법론으로, 하나의 클래스당 한 개의 특정 오브젝트만 존재하도록 하는 거 ㅅ이다. 싱글톤 패턴을 구현하여 얻을 수 있는 이점은

1️⃣ 불필요한 메모리 누수를 방지한다.

2️⃣ 공통된 오브젝트를 사용해야 하는 상황에서 특정한 하나의 오브젝트만 사용하게 해준다. ex) DBConnectionPool

---

## **🔎 자바의 싱글톤 패턴**

#### **⚙️ 구현 방법**

1️⃣ 생성자를 private으로 선언 : 외부에서 클래스의 오브젝트를 생성할 수 없게 된다.

2️⃣ 참조는 static으로 정의 : 어느 영영에서든 접근이 가능하도록 된다.

👉 클래스가 classloader에 의해 단 한번만 인스턴스화 되는 것을 이용하여 구현한다.

#### **⚙️ Thread Safety를 보장하는 구현 방법**

**𝟏. getter 메소드의 Synchronized 선언**

아래의 코드에서는 인스턴스를 리턴해줄 getInstance() 메서드에서 synchronized를 선언해주었다. synchronnized를 선언하지 않았을 때에 발생할 수 있는 문제에 대해 생각해보면, 2개의 쓰레드가 동시에 getInstance()를 호출한다면 동시에 2개의 객체가 생성되어 버릴수도 있다.

```
public class JavaSingleton{
 
    private static JavaSingleton instance;
 
 	// 생성자
    private JavaSingleton(){}
     
    // thread safety getter
    public static synchronized JavaSingleton getInstance(){
        if(instance == null){
            instance = new JavaSingleton();
        }
        return instance;
    }
}
```

이 구현 방법의 단점은

1️⃣ locking overhead로 인한 성능 저하

2️⃣ 인스턴스가 초기화되고 나면 필요없는 synchronization이 계속해서 발생하기 때문에 효율성이 떨어진다.

2️⃣ 의 단점을 보완하기 위해서 synchronized 키워드를 if 블록 안으로 이동시킨다면, synchronization이 초기화시점에서만 진행되게 되어 퍼포먼스가 훨씬 향상될 수 있다.

```
public static JavaSingleton getInstance() 
  { 
    if (instance == null)  
    { 
      synchronized (JavaSingleton.class) 
      { 
        if(instance==null) 
        { 
          instance = new JavaSingleton(); 
        } 
      } 
    } 
    return instance; 
  }
```

**𝟐. Bill Pugh 구현법 : 클래스 내부에 static class 선언**

이 방법은 제안한 개발자의 이름을 따서 Bill Pugh 구현법으로 불리는데, 가장 보편적으로 사용되는 싱글톤 구현법이다. static 키워드로 선언된 객체는 메모리 할당이 단 한번만 이루어지고 final 키워드로 선언되면 그 값을 덮어쓸 수 없음을 이용하는 것이다. getInstance()가 최초로 BillPughSingleton클래스의 instance를 호출한 순간 해당 클래스는 최초 인스턴스를 생성하고, 그 후부터는 호출될때마다 해당 메모리번지에 저장된 인스턴스를 리턴한다.

```
public class JavaSingleton  
{ 
  
  private JavaSingleton()
  
  private static class BillPughSingleton 
  { 
    private static final JavaSingleton instance = new JavaSingleton(); 
  } 
  
  public static JavaSingleton getInstance()  
  { 
    return BillPughSingleton.instance; 
  } 
}
```

---

## **🔎 스프링의 싱글톤 패턴**

스프링의 싱글톤 패턴은 자바의 싱글톤 패턴과 달리 클래스 자체에 의해서가 아니라, 스프링 컨테이너(Bean Factory / Application Context)에 의해 구현된다.

스프링에서는 컨테이너 내에서 특정 클래스에 대해 @Bean이 정의되면, 스프링 컨테이너는 그 클래스에 대해 딱 한개의 인스턴스를 만든다. 이 공유 인스턴스는 설정 정보에 의해 관리되고, bean이 호출될 때마다 스프링은 생성된 공유 인스턴스를 리턴 시킨다.

공유 인스턴스의 생성시점은 스프링 컨테이너에 따라 달라지는데, 빈팩토리는 최초 호출시점에서 인스턴스를 생성하고, 애플리케이션 컨텍스트는 미리 모든 공유 인스턴스를 다시 초기화 해두었다가 호출될 때 바로 리턴시켜준다.

![image](https://user-images.githubusercontent.com/96826217/213198791-4992abd4-d16c-4325-968e-984c6bffe297.png)


bean 관리의 주체인 스프링 컨테이너는 그 어떤 호출에도 단일 공유 인스턴스를 리턴시키기 때문에 thread safety도 자동으로 보장된다.

---

## **🔎 요약**

1.  자바 싱글톤은 클래스로더에 의해 구현되고, 스프링의 싱글 톤은 스프링 컨테이너에 의해 구현된다.
2.  자바 싱글톤의 scope는 코드 전체이고, 스프링 싱글톤의 scope는 해당 컨테이너 내부이다.
3.  스프링에 의해 구현되는 싱글톤패턴은 Thread safety를 자동으로 보장한다. 자바로 구현하는 싱글톤패턴은 개발자의 로직에 따라 thread safety를 보장할수도, 보장하지 않을수도 있다.
