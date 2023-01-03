2023/01/02

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 DI (Dependency Injection)

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Spring ] DI (Dependency Injection)

**🔩 DI**

---

Dependency Injection

**스프링 프레임워크에서 제공하는 의존 관계 주입 기능**

> *A가 변하면 의존 관계인 B도 변한다*
> 

객체를 직접 생성하는 게 아니라 외부에서 생성한 후 주입 시켜주는 방식

클래스 사이의 의존관계를 빈 설정 정보를 바탕으로 컨테이너가 자동으로 연결

모듈 간의 결합도가 낮아지고 유연성이 높아짐

<br><br>

+ **DI 장점**

---

1. **낮은 객체 간의 결합도**
    
    스프링 자체에서 설정을 통해 연관 관계를 맺어줌으로써 객체간 결합도를 낮춤
    
2. **편리한 유지보수**
3. **클래스 재사용성이 용이**
4. **테스트가 용이**

<br><br>

+ **DI 단점**

---

1. 의존성 주입을 위한 선행 작업이 필요 → 간단한 프로그램 개발 시 번거로움
2. 어려운 코드 추적

<br><br>

🔩 **예비 답변**

---

Q. DI에 대해 설명해주세요.

**DI**는 스프링 프레임워크에서 제공하는 의존 관계 주입 기능입니다. 클래스에 의존 관계를 설정해주면 설정한 정보를 바탕으로 컨테이너가 자동으로 클래스를 연결해주는 것으로 클래스 A에 변경 사항이 생기면 A와 의존 관계가 설정된 클래스 B에도 영향을 주는 것입니다.

DI는객체간의 결합도는 낮아지고 유연성이 높아져 유지보수에 용이하다는 장점이 있고, 코드 추적이 어렵다는 단점이 있습니다. 

<br><br>

🔩 **참고**

---

블로그

[[Spring] DI, IoC 정리](https://velog.io/@gillog/Spring-DIDependency-Injection)

[의존관계 주입(Dependency Injection) 쉽게 이해하기](https://tecoble.techcourse.co.kr/post/2021-04-27-dependency-injection/)

[Dependency Injection : 의존성 주입](https://goni95.tistory.com/15)

<br><br>
