2023/01/18

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 Spring Annotation

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Spring ] Spring Annotation

**🔩 Spring Annotation**

---

- **@Configuration**
    
    빈(Bean) 정의의 소스로서 쓰이는 클래스 마크를 할 때 사용
    
    빈의 생애 주기 관리 및 빈 생성
    
    @Bean 애너테이션이 붙은 메서드는 빈을 생성
    
    <br>

- **@Bean**
    
    메서드에서 반환된 결과를 빈으로 지정
    
    반환된 빈은 팩토리 메서드와 동일한 이름을 가짐
    
    스프링 컨텍스트에서 관리
    
    <br>
    
- **@ComponentScan**
    
    클래스 Bean들을 찾아서 Context에 bean 등록
    
    Spring이 @Configuration 클래스에 대해 구성된 패키지 스캔
    
    <br>
    

- **@EnableAutoConfiguration**
    
    Application Context를 만들 때 자동으로 빈설정이 되도록 하는 기능
    
    <br>
    

- **@Component**
    
    개발자가 직접 작성한 class를 Bean으로 등록
    
    빈을 선언하는 또다른 방식
    
    자동 스캔 시점에 해당 클래스가 스프링 빈으로 등록됨
    
    <br>
    

- **@Controller**
    
    API와 view를 동시에 사용하는 경우에 사용
    
    view가 필요 없이 API만 지원하는 서비스의 경우 @RestController 사용
    
    <br>
    

- **@Service**
    
    @Component의 특수화된 애너테이션
    
    캡슐화된 상태를 가지지 않음
    
    <br>
    

- **@Autowired**
    
    스프링이 Type에 따라 알아서 Bean을 주입
    
    Type을 먼저 확인한 후 못 찾으면 Name에 따라 주입
    
    필드, 메서드, 생성자에 사용
    
    <br>
    

- **@Scope**
    
    @Component 클래스 또는 @Bean의 범위(Scope)를 정의하기 위해 사용
    
    싱글톤 Singleton, 프로토타입 Prototype, 리퀘스트 Request, 세션 Session, 글로벌 세션GlobalSession, 커스텀 스코프
    
    <br>
    

- **@SpringBootApplication**
    
    @Configuration, @EnableAutoConfiguration, @ComponentScan 3가지를 하나로 합친 애노테이션
    
    <br>
    

<br><br>

🔩 **예비 답변**

---

Q. 스프링 애너테이션에 대해 말해보세요.

대표적인 스프링 애너테이션으로는 @Configuration, @Bean, @Component, @Autowired, @Controller 등이 있습니다. 

@Configuration은 빈을 정의할 때 소스로 사용되는 클래스를 마크 할 때 사용하는 애너테이션이며,

@Bean은 개발자가 직접 제어가 불가능한 외부 라이브러리 등을 빈으로 만들려할 때 사용하는 애너테이션입니다.

또한 @Component는 • 개발자가 직접 작성한 class를 Bean으로 등록하기 위한 애너테이션이며,

@Autowired는 스프링이 타입에 따라 알아서 빈을 주입하도록 하는 애너테이션입니다.

마지막으로 @Controller는 API와 view를 동시에 사용하는 경우에 사용하는 애너테이션인데 view를 사용하지 않고 API만 지원하는 서비스의 경우 @RestController 애너테이션을 사용합니다.

<br><br>

🔩 **참고**

---

블로그

[[Spring] 유용한 Spring Annotation](https://bryceyangs.github.io/study/2021/08/13/Spring-Spring-Annotation/#%EB%A7%88%EB%AC%B4%EB%A6%AC)

JRebel

[Spring Annotations Cheat Sheet](https://www.jrebel.com/blog/spring-annotations-cheat-sheet)


<br><br>
