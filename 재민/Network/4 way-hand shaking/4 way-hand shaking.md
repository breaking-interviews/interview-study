### TCP **(Transmission Control Protocol)**

인터넷상에서 데이터를 메세지 형태로 보내기 위해 IP와 함께 사용하는 프로토콜

TCP는 신뢰적이고 연결지향적인 서비스를 제공하며 TCP는 패킷의 추적 및 관리, IP는 배달을 함 

TCP는 연결형 서비스로 신뢰적인 전송을 보장하나 hand shaking 과정과 데이터의 흐름제어 및 혼잡제어를 수행하여 속도가 느림

### TCP의 특징

- 3-way handshaking과정을 통해 연결을 설정하고 4-way handshaking을 통해 해제
- 흐름 제어 및 혼잡 제어
- 높은 신뢰성 보장
- UDP보다 속도가 느림
- 전이중(Full-Duplex), 점대점(Point to Point) 방식

### 3-way handshaking

클라이언트와 서버가 서로 통신할 준비가 되었음을 확인하는 과정

1. SYN
    1. 클라이언트가 임의의 난수로 생성된 seq(Sequence Number)를 x로 지정하고 SYN 플래그 비트를 1로 설정한 세그먼트를 서버로 전송(seq : x)
    2. 클라이언트 상태는 syn sent 
2. SYN + ACK
    1. 서버는 받은 SYN(x)을 받고 클라이언트로 받았다는 신호인 ACK와 SYN 패킷을 전송(seq : y, ACK : x + 1)
    2. 서버의 상태는 syn received
3. ACK
    1. 클라이언트는 서버의 응답을 ACK(x+1)와 SYN(y) 패킷을 받고 ACK(y+1)을 서버로 보내 통신을 수립
    2. 클라이언트 상태는 established

### 4-way handshaking

클라이언트와 서버가 서로의 통신을 종료하는 과정

1. Clinet → Server : FIN(+ACK)
    1. 클라이언트가 close()를 호출하여 접속을 끊으려함
    2. 클라이언트가 서버에게 연결을 종료한다는 FIN 패킷을 보냄(FIN 패킷에는 실질적으로 ACK도 포함되어 있음)
2. Server → Client : ACK
    1. 서버가 FIN을 받고 ACK를 클라이언트에게 전송 후 자신의 통신이 끝날때까지 기다림(TIME_WAIT 상태)
    2. 서버는 클라이언트에게 응답을 보내고 CLOSE_WAIT 상태로 들어가며 아직 남은 데이터가 있다면 전송을 마친 후 close()를 호출
    3. 클라이언트는 서버에서 ACK를 받은 후 서버가 남은 데이터 처리를 끝내고 FIN 패킷을 보낼 때까지 기다림(FIN_WAIT2)
3. Server → Client : FIN
    1. 데이터를 모두 전송했으면 서버는 클라이언트에게 FIN 패킷을 보내고 승인 번호를 받을 때 까지 LAST_ACK 상태로 진입
4. Client → Server : ACK
    1. 클라이언트는 FIN을 받고 ACK를 서버에게 보냄
    2. 아직 서버로부터 받지 못한 데이터가 있을 수 있기에 TIME_WAIT를 통해 기다림(실질적으로 종료 과정인 CLOSED에 들어가게됨 ,TIME_WAIT 상태는 의도치 않은 에러로 연결이 데드락으로 빠지는 것을 방지 : 에러로 인해 종료가 지연되도 타임이 초과되면 CLOSED로 들어감) 
    3. 서버는 ACK를 받은 이후 소켓을 닫음(CLOSED)
    4. TIME_WAIT가 끝나면 클라이언트도 닫음(CLOSED)


## (면접) 4 way-hand shaking

4 way-hand shaking는 클라이언트와 서버가 통신을 종료하는 과정입니다. 진행과정을 단계별로 말씀드리면 1단계 클라이언트가 서버에게 연결을 종료한다는 FIN 패킷을 보냅니다. 2단계 서버는 FIN을 받고 ACK응답을 클라이언트에게 전송합니다. 이때 남은 데이터가 있다면 모두 전송 후 close()를 호출하고 클라이언트는 ACK를 받은 후 서버에서 FIN을 보낼 때 까지 기다립니다. 3단계 데이터를 모두 전송했으면 서버는 클라이언트에게 FIN을 보냅니다. 4단계 클라이언트는 FIN을 받고 ACK를 서버에게 보냅니다. 서버는 ACK를 받은 이후 소켓을 닫고 일정 시간이 지나면 클라이언트도 닫아 통신이 종료됩니다.
