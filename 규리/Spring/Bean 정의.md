2023/01/10

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 Spring Bean

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Spring ] **Bean**

**🔩 Bean**

---

**컨테이너 안에 들어있는 객체**

_스프링 컨테이너가 관리하는 재사용 소프트웨어 컴포넌트_

인스턴스화된 객체

클래스 등록 정보, 게터/세터 메서드 포함

컨테이너의 명령, 인스턴스화, 설정, 조립할 객체를 정의하는 설정 메타데이터로 생성

`@Bean + 메서드명` 을 모두 호출하여 스프링 컨테이너에 등록

<br><br>

**+ Bean 접근방법**

---

```java
**// 1. Bean 생성/인스턴스화**
ApplicationContext context = new ClassPathXmlApplicationContext("services.xml", "daos.xml");

**// 2. getBean 으로 인스턴스 가져오기/인스턴스 검색**
CarStoreService service = context.getBean("noTeaYesCar_store", ntycStoreService.class);

**// 3. 인스턴스 사용**
List<String> userList = service.getUserList();
```

<aside>
❗ 응용프로그램 사용 시에는 getBean() 메서드 호출 사용 ❌

</aside>

<br><br>

🔩 **예비 답변**

---

Q. 빈 Bean에 대해 말해보세요.

빈은 스프링 컨테이너가 관리하는 재사용 소프트웨어 컴포넌트로 컨테이너에 담겨 있으며 필요할 때 컨테이너에서 가져와 사용합니다. @Bean 애너테이션을 사용해 등록하고, 빈으로 등록된 객체는 쉽게 주입하여 사용할 수 있습니다.

<br><br>

🔩 **참고**

---

블로그

[스프링 빈(Spring Bean)이란? 개념 정리](https://melonicedlatte.com/2021/07/11/232800.html)

[[JAVA] Spring Framework DI 심화](https://www.notion.so/c3d791d3650a451785641e0cb6fd7e6c)

<br><br>
