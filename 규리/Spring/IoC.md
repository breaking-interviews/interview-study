2023/01/02

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 IoC (Inverse of Control)

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Spring ] IoC (Inverse of Control)

**🔩 IoC**

---

제어의 역전, Inverse of Control

> *제어의 흐름을 바꾼다*


**메소드나 객체의 호출작업을 개발자가 결정하는 것이 아니라, 외부에서 결정되는 것**

객체의 생성부터 생명주기의 관리까지 모든 객체에 대한 제어권이 바뀌는 것

제어의 흐름을 사용자가 컨트롤 하는 것이 아니라 스프링에게 맡겨 작업을 처리

*스프링이 모든 의존성 객체를 스프링이 실행될때 만들어주고 필요한곳에 주입*

![image](https://user-images.githubusercontent.com/107545016/210350939-66ce931b-9009-4afe-a776-adc23280feb0.png)


<br><br>

+ **IoC 장점**

---

1. 의존성 역전으로 객체간 결합도 낮춤
2. 유연한 코드 작성 가능
3. 편리한 유지 보수
4. 높은 가독성 및 코드 중복 방지

<br><br>

+ **IoC 단점**

---

1. 역제어 구조로 코드를 이해가 어려움

<br><br>

🔩 **예비 답변**

---

Q. IoC에 대해 설명해주세요.

IoC는 제어의 역전으로, 메소드나 객체의 호출작업을 개발자가 결정하는 것이 아니라 스프링에게 제어권을 주어 작업을 처리하도록 하는 것입니다. 스프링이 모든 의존성 객체를 스프링이 실행될때 만들어주고 필요한곳에 주입하며 객체간 결합도는 낮춰주고 유연한 코드 작성이 가능해 유지보수가 편리하도록 하는 장점이 있지만, 역제어 구조로인해 코드를 이해하기 어려울 수 있다는 단점이 있습니다.


<br><br>

🔩 **참고**

---

블로그

[[Spring] DI, IoC 정리](https://velog.io/@gillog/Spring-DIDependency-Injection)

[[Spring] IoC(Inversion of Control)](https://velog.io/@hiy7030/Spring-IoCInversion-of-Control)

<br><br>
