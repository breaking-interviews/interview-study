2023/01/30

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 IPC, Inter Process Communication

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ OS ] IPC

**🔩 IPC**

---

**프로세스간의 통신을 위한 메커니즘**

프로세스는 커널이 제공하는 IPC 설비를 이용해 프로세스간의 통신 진행

<br><br>

**+ 메모리 공유** Shared Memory

---

**프로세스들이 공유하는 메모리를 이용해 통신하는 것**

생산자(producer) 프로세스가 공유 메모리(buffer)에 item을 생산하고 저장하면, 소비자(consumer) 프로세스가 이를 읽고 소비

<br><br>

**+ 메세지 전달** Message Passing

---

**공유되는 주소 공간 없이 프로세스간 통신하는 것**

파이프(쉘에서 사용하는 파이프), 소켓

<br><br>

🔩 **예비 답변**

---

Q. IPC에 대해 말해보세요.

IPC란 Inter Process Communication으로 프로세스간의 통신을 위한 메커니즘입니다. ****프로세스는 커널 제공하는 IPC 설비를 통해서 프로세스간의 통신을 진행합니다.

이런 IPC의 모델로는 메모리 공유와 메세지 전달 두 가지가 있는데, 메모리 공유는 프로세스들이 공유하는 메모리를 이용하여 통신하는 것이며, 메세지 전달은 프로세스들이 공유되는 주소 공간 없이 통신하는 것입니다.

<br><br>

🔩 **참고**

---

블로그

[[운영체제] IPC(Inter-Process Communication)란? | pipes](https://code-lab1.tistory.com/42)

[[운영체제] 프로세스란? 프로세스 메모리 구조, 상태, 스케줄링](https://code-lab1.tistory.com/38)

<br><br>
