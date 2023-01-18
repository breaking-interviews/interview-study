2023/01/18

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 Annotation

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Spring ] Annotation

**🔩 Annotation**

---

**프로그램에게 추가적인 정보를 제공하는 메타데이터**

주석과 비슷하나, 애너테이션은 프로그램에게 정보 제공

```java
**@GetMapping()**
public String hello() {
    return "hello";
}
```

1. 컴파일러를 통해 문법 에러 체크
2. 자동으로 코드를 생성
3. 런타입에 특정 기능 실행

<br><br>

**+ Annotation 동작 순서**

---

1. `@` 사용하여 애너테이션 정의
2. 사용하고자 하는 코드 위에 배치
3. 코드 실행 중 Reflection을 통해 추가 정보 획득하여 기능 실시

<br><br>

**+ Annotation 용도**

---

- 문서화
- 컴파일러 체크
- 코드 분석과 자동 생성
- 런타임 프로세싱

<br><br>

**+ Reflection**

---

구체적인 클래스 타입을 알지 못할 때, 클래스의 메소드와 타입, 변수들을 접근할 수 있도록 해주는 자바 API

Reflection을 이용하면 Annotation의 적용 여부와 엘리먼트 값을 읽고 처리할 수 있음

Annotation 지정만으로도 원하는 클래스 주입 가능

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

[애너테이션이란?](https://eatnows.tistory.com/92)

[[Java] 심화 Effective1](https://www.notion.so/Java-Effective1-114975584b77478d87f6e97021370d3c)

<br><br>
