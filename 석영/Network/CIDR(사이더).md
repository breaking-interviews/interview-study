![image](https://user-images.githubusercontent.com/96826217/212695760-b7e3b589-aeec-406b-9fe5-5de231edc1d1.png)

## **🔎 CIDR(Classless Inter-Domain Routing)란?**

클래스 없는 라우팅 기법을 말하며 IP를 좀 더 유연하게 사용할 수 있다. 기존의 네트워크 클래스 방법을 대체하고 1993년에 도입되기 시작했고 빠르게 고갈되고 있는 IPv4를 보다 효율적으로 사용할 수 있다.

#### **CIDR 블록**

![image](https://user-images.githubusercontent.com/96826217/212696951-97fcf794-3c35-407e-bc82-1d6c03b427ed.png)


CIDR 블록은 A.B.C.D/N과 같은 형태를 갖고 있고 IPv4 주소처럼 4개의 8비트 단위 바이트로 이루어진 32비트 이진 숫자이다. '/' 뒤에 N은 prefix 길이고 주소의 왼쪽으로부터 비트의 수를 가리키고 있다.

IPv4는 주소의 길이가 **32비트다**. 따라서 N비트의  CIDR prefix는 32-N 비트의 나머지를 남기며, 남은 비트로로 만들 수 있는 경우의 수는 **2^(32-N)**라고 할 수 있다. 즉, 짧은 CIDR prefix는 더 많은 IP 주소를 가지게 되며, 긴 CIDR prefix는 더 적은 IP 주소를 가지게 된다.

또한 **CIDR****는 IPv6 주소에서도 사용될 수 있다**. 이때 prefix의 길이는 **0에서 128까지**의 범위를 가지고 있다.(0 < N < 128) IPv6도 IPv4처럼 동일한 방식이 적용된다.
