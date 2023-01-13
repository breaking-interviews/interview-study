2023/01/05

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 4 way-hand shaking

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Network ] 4 way-handshaking

**+ TCP란**

---

네트워크 계층 중 전송 계층에서 사용하는 프로토콜

신뢰성을 보장하는 연결형 서비스

<br><br>

**🔩 4 way-handshaking**

---

TCP의 연결을 해제(Connection Termination) 하는 과정

= 클라이언트와 서버가 서로의 통신을 종료하는 과정

<br><br>

**🔩 통신 종료 과정**

---

1. **fin-wait1**
    
    클라이언트가 서버에게 연결을 종료하겠다는 FIN 패킷 전송
    
    서버가 클라이언트에세 우선 ACK 패킷 전송
    
2. **close-wait**
    
    서버는 통신이 끝날 때까지 기다린 후 통신이 끝나면 클라이언트에게 FIN 패킷 전송
    
3. **last-ack**
    
    클라이언트는 ACK 패킷을 서버에게 전송
    
4. **fin-wait2, time-wait**
    
    서버가 보내는 FIN 보다 데이터가 늦게 도착할 수 있기 떄문에 클라이언트는 일정 시간동안 소켓을 열어둔채 패킷을 기다림
    
    이후 연결 종료
    

<br><br>

🔩 **예비 답변**

---

Q. 4 way-handshaking에 대해 설명해주세요.

4 way-handshaking은 클라이언트와 서버가 서로의 통신을 종료하는 4단계 TCP 연결 해제 과정입니다. 

클라이언트가 서버에게 연결을 종료하겠다는 FIN 패킷을 전송하면 서버가 클라이언트에게 ACK 패킷을 전송합니다. 이후 서버는 통신이 끝날 때까지 기다렸다가 통신이 끝난 후 클라이언트에게 FIN 패킷을 전송합니다. 이후 클라이언트는 ACK 패킷을 서버에게 전송하고 서버는 후속 데이터를 기다리는 동안 소켓을 열어둔 후 일정 시간이 지나면 연결을 종료합니다.

<br>

Q. Server에서 FIN 플래그를 전송하기 전에 전송한 패킷이 Routing 지연이나 패킷 유실로 인한 재전송 등으로 인해 FIN 패킷보다 늦게 도작한 상황이 발생하면 어떻게 되는지 설명해주세요.

서버에서 FIN 플래그를 전송하기 전에 먼저 전송했던 패킷이 라우팅 지연이나 패킷 유실로 인한 재전송 때문에 FIN 패킷보다 늦게 도착하게 되는 것을 방지하기 위해서 Client가 Server로 부터 FIN 플래그를 수신한 후에도 일정 시간 Time wait 동안 세션을 닫지 않고 남겨두어 잉여 패킷을 기다리는 과정을 거치게 됩니다.

<br>

Q. 초기 Sequence Number인 ISM을 0부터 시작하지 않고 난수를 생성해서 설정하는 이유에 대해서 설명해주세요.

통신 시 커넥션을 맺을 때 사용하던 포트는 시간이 지나면 재사용됩니다. 그렇기때문에 두 통신이 과거에 포트 번호 쌍을 사용했을 가능성이 생기게 되고, 난수가 아닌 순차적으로 Sequence Number를 전송한다면 이전의 커넥션으로부터 오는 패킷으로 인식할 가능성이 생겨 ISM을 0이 아닌 난수로 생성합니다.

<br><br>

🔩 **참고**

---

블로그

[[네트워크] 3-way / 4-way Handshake 란?](https://bangu4.tistory.com/74)

[TCP 3 way handshake, 4 way handshake 알아보기 (feat wireshark)](https://velog.io/@skyepodium/3-way-handshaking-4-way-handshaking)

<br><br>
