# Network



<br>

-----------------------

### DNS (Domain Name System)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ IP를 사람이 읽을 수 있는 주소로 변경해주는 시스템
+ www.naver.com
+ domain
  + 인터넷 상에서 사용되는 고유한 이름




</details>

-----------------------

<br>





<br>

-----------------------

### DNS 동작 원리

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ <img width="588" alt="image" src="https://user-images.githubusercontent.com/57162257/185788645-b9640485-8eed-479b-9169-914daf599420.png">

1. 사용자가 www.naver.com을 입력하면 local DNS에 요청된 도메인에 대한 IP를 질의한다.
2. 만약 local DNS에 IP가 존재하지 않는다면 local DNS는 Root DNS에 www.naver.com에 대한 IP를 질의한다.
3. Root DNS는 com도메인을 관리하는 com DNS의 정보를 local DNS에 전달한다.
4. localDNS는 com DNS서버에 www.naver.com 질의.
5. Com DNS서버는 naver.com을 관리하는 DNS 서버의 정보를 local DNS에 전달한다.
6. local DNS는 naver.com을 관리하는 DNS서버에 naver.com에 대한 IP를 질의한다.
7. naver.com을 관리하는 DNS서버는 www.naver.com에 대한 ip를 전달받는다.
8. 도메인 ip를 전달받은 local DNS는 ip를 캐싱 하고 사용자에게 ip를 전달한다.



</details>

-----------------------

<br>



<br>

-----------------------

### OSI 7계층

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 통신 접속부터 완료까지의 과정을 7단계로 정의한 국제 통신 표준 규약
+ 통신이 일어나는 과정을 단계별로 알 수 있고 문제가 생겼을 때 그 단계만 수정하기 위함.

1. 물리 계층 (1계층)
   - 전송하는데 필요한 통신 케이블로 데이터 제공 (케이블, 허브 ...)
2. 데이터 계층 (2계층)
   - 물리계층으로 송수신 되는 정보의 오류와 흐름을 관리하여 안전한 정보를 전달하기 위한 계층
   - 브릿지나 스위치를 통해 MAC 주소를 가지고 물리계층에서 받은 정보를 전달.
   - 이 계층에서 전송되는 단위를 프레임
3. 네트워크 계층 (3계층)
   - IP를 지정하고 라우터로 경로를 선택해 네트워크를 통해 패킷을 전달하는 계층
   - 이 계층에서 전송되는 단위를 패킷
4. 전송 계층 (4계층)
   - 종단 간의 사용자들에게 신뢰성 있는 데이터를 전달하는 계층
     - 흐름 제어 : 송신측과 수신측 사이의 데이터 처리 속도 차이 제어
     - 혼잡 제어 : 네트워크 혼잡을 피하기 위해 데이터의 전송 속도 제어
     - 오류 제어 : 오류 검출과 재전송
5. 세션 계층 (5계층)
   - 데이터를 통신하기 위한 논리적 연결을 담당하는 계층
   - API, Socket
6. 표현 계층 (6계층)
   - 데이터 압축, 변환이 이루어지는 계층
   - JPEG, MPEG
7. 응용 계층 (7계층)
   - 응용 프로그램과 연관하여 서비스를 수행하는 계층
   - HTTP, DNS



</details>

-----------------------

<br>





<br>

-----------------------

### 전송계층

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 전송계층은 송신자와 수신자에게 신뢰성 있는 데이터를 전달하기 위해 TCP 프로토콜과 UDP 프로토콜을 사용한다.
+ TCP (Transmission Control Protocol)
  + 인터넷 상에서 데이터를 메시지 형태로 보내기 위해 IP와 함께 사용하는 프로토콜
  + IP를 통해 목적지를 지정하고, TCP를 통해 논리적 연결을 생성하고 신뢰성 있는 데이터 전달을 한다.
  + <img width="489" alt="image" src="https://user-images.githubusercontent.com/57162257/185790986-173c2460-8ff8-48a8-83e8-63738c3f8d1c.png">
  + 특징
    + 연결형 서비스로 가상 회선 방식 사용
    + 3-way handshaking과정으로 연결을 설정하고, 4-way handshaking을 통해 해제한다. (연결 지향적)
    + 흐름 제어 및 혼잡 제어
    + 패킷 추적으로 높은 신뢰성을 보장한다.
    + UDP보다는 속도가 느리다.

+ UDP (User Datagram Protocol)
  + 패킷을 데이터그램 단위로 처리하는 프로토콜
    + <img width="513" alt="image" src="https://user-images.githubusercontent.com/57162257/185790984-b5c4cb5b-8650-4f50-bd73-7495a05efafb.png">
    + 데이터그램 : 독립적인 관계를 가지는 패킷

  + 특징
    + 비연결형 서비스로 데이터그램 방식을 사용한다.
    + 데이터를 주고받을때 신호절차를 거치지 않는다.
    + 신뢰성이 낮다.
    + TCP보다 속도가 빠르다.




</details>

-----------------------

<br>



<br>

-----------------------

### TCP / IP 4계층

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 컴퓨터들이 정보를 주고 받는데 사용되는 통신 규약(프로토콜)의 모음
+ OSI 7계층과 같은 역할을 하지만 OSI는 이론적 표준, TCP/IP는 실무적 표준
+ <img width="261" alt="image" src="https://user-images.githubusercontent.com/57162257/185791580-f89957e7-dc52-4630-9ece-6f99bc9f9960.png">

1. 네트워크 연결 계층 (1계층)
   - 원하는 MAC주소로 데이터를 전송
   - 단위 : 프레임
   - 전송 주소 : MAC
   - 장비 : 브릿지, 스위치
2. 인터넷 계층 (2계층)
   - 데이터 전송을 위한 논리적 주소(IP) 지정 및 경로 지정
   - 단위 : 패킷
   - 전송 주소 : IP
   - 장비 : 라우터
3. 전송 계층 (3계층)
   - 호스트 간의 데이터 송수신 및 연결 제어
   - 단위 : 세그먼트
   - 전송 주소 : Port
   - 장비 : 게이트 웨이
4. 응용 계층 (4계층)
   - 응용 프로그램으로 서비스 제공
   - 단위 : 데이터, 메시지



</details>

-----------------------

<br>



<br>

-----------------------

### TCP의 논리적 연결

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 서버는 socket생성 -> socket 주소 할당 -> 연결 요청 대기 -> 연결 허용 -> 데이터 송수신 -> 연결 종료

- 클라이언트는 socket생성 -> 연결 요청 -> 데이터 송수신 -> 연결 종료

- TCP를 이용해 서버와 클라이언트간의 통신을 위해서는 특별한 신호 절차를 거쳐야한다.

- 3 - way handshaking

  - TCP/IP 프로토콜을 이용해 데이터를 전송하기 전에 서로 통신할 준비가 되었는지 확인하는 절차
  - <img width="397" alt="image" src="https://user-images.githubusercontent.com/57162257/185792690-7c95f566-483d-4832-b7c8-05ad1df5e9d1.png">

  1. 클라이언트에서 서버에게 SYN패킷을 보낸다.
     - 이 때 클라이언트는 SYN/ACK 응답을 기다리는 SYN_SEND 상태가 된다.
  2. 서버에서 SYN패킷을 받고 수락하는 SYN/ACK 패킷을 발송한다.
     - 이 때 서버는 ACK를 받기 위해 SYN_RECEIVED 상태가 된다.
  3. 클라이언트는 SYN/ACK 패킷을 받은 후 서버에 ACK패킷을 전송한 후 부터 데이터 통신이 이루어 진다.

- 4 - way handshaking

  - 세션을 종료하기 위해 수행되는 절차
  - <img width="347" alt="image" src="https://user-images.githubusercontent.com/57162257/185792697-47b4ff15-f77c-40c3-84f8-573610ea86b9.png">

  1. 클라이언트가 연결을 종료하겠다는 FIN 패킷 전송
  2. 서버에서 FIN 패킷을 받고 ACK패킷을 보낸 후 자신의 작업이 끝날때 까지 기다린다.
  3. 서버의 작업이 끝나게 되면 연결이 종료되었다는 FIN 패킷을 보낸다.
  4. 클라이언트는 확인했다는 ACK패킷을 보내게된다.



</details>

-----------------------

<br>



<br>

-----------------------

### 4 - way handshaking에서 서버의 통신이 FIN패킷보다 늦게 도착하면 어떻게 되나?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 서버의 FIN 패킷보다 서버의 통신이 늦게 도착하게 되면 데이터가 유실되게 된다.
+ 하지만 이를 위해 클라이언트에서 FIN패킷을 받게 되어도 240초 동안 세션을 남겨놓고 잉여 패킷을 기다리는 과정을 거치게된다.



</details>

-----------------------

<br>



<br>

-----------------------

### www.naver.com 검색시 발생하는 과정

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

1. www.naver.com을 브라우저 주소창이 입력한다.
2. 브라우저는 local DNS을 확인하여 www.naver.com에 대한 IP정보가 있는지 확인한다.
3. 요청한 도메인이 존재하지 않는다면 도메인을 호스팅하고 있는 서버의 IP 주소를 찾기 위해 Recursive Query를 한다.
4. 브라우저는 도메인의 IP를 받아 서버와 TCP연결을 한다 (3-way handshaking)
   1. 브라우저는 서버에 접속 요청 SYN패킷을 보낸다.
   2. 서버는 수락하는 SYN/ACK 패킷을 보낸다.
   3. 클라이언트는 확인 ACK패킷을 보낸다.
5. TCP연결이 완료되면 브라우저가 웹 서버에 HTTP 요청을 보낸다.
6. 서버는 요청을 처리하고 response를 생성한다.
7. 브라우저가 HTML을 사용자에게 보여준다.



</details>

-----------------------

<br>



<br>

-----------------------

### HTTP & HTTPS

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ HTTP
  + 인터넷에서 클라이언트와 서버 사이에서 이루어지는 요청을 처리하는 프로토콜
  + TCP (HTTP/1, HTTP/2), UDP (HTTP/3)을 사용하며 80번 포트를 사용한다.

+ HTTPS
  + HTTP에 SSL과 TSL로 보안이 추가된 프로토콜로 데이터를 암호화해 보안을 통해 신뢰성 있는 요청을 하기 위함
    - SSL과 TSL 암호화는 전송 계층과 응용 계층 사이에서 발생한다.
    - SSL (Secure Sockey Layer) : 전송된 데이터를 암호화하여 보안을 유지하는 표준 기술
  + 개인키 암호화와 공개키 암호화 방식을 사용한다.
    - 공개키 암호화
      - 공개키로 암호화하고 개인키로 복호화한다.
      - 개인키로 복호화 할 수 있기 때문에 나만 요청을 볼 수 있다.
    - 개인키 암호화
      - 개인키로 암호화하고 공개키로 복호화한다.
      - 공개키로 데이터가 탈취 될 수 있지만, 개인키로 암호화했기 때문에 내가 인증한 정보임을 알려 신뢰성을 보장할 수 있다 (전자 서명)
  + 443번 포트를 사용한다.

+ HTTP 프로토콜 특징
  + 비연결 지향 (connection less) : Request와 Response가 끝나면 연결을 끊는다.
  + 상태 정보 유지 안함 (state less) :  연결을 끊는 순간 클라이언트와 서버간의 상태를 유지하지 않는다.




</details>

-----------------------

<br>



<br>

-----------------------

### Http 멱등성

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 특정 HTTP메서드를 여러 번 요청했을때, 매번 요청 결과가 같은 것.
+ GET : 여러번 수행해도 서버의 상태가 변하지 않고 같은 결과를 가져온다.
+ PUT : 여러번 수행해도 데이터는 요청한 값으로 수정된 같은 상태이다.
+ DELTE : 여러번 수행해도 그 데이터는 요청을 보낸 시점에 사라진다.
+ POST : 여러번 수행하면 부가적인 결과를 가져온다. (같은 데이터 계속 추가)



</details>

-----------------------

<br>



<br>

-----------------------

### http1.0 & http1.1

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ http 1.0
  + connection 하나당 하나의 요청을 처리할 수 있다. 그렇기 때문에 응답을 받아야 다음 요청을 진행 할 수 있다.

+ http 1.1
  + keep alive를 통해 connection 하나당 N개의 요청을 처리할 수 있다.
    + 특정 시간까지 access가 오지 않더라도 연결을 끊지않고 유지하는 헤더

  + 응답이 오지않아도 연속적으로 요청을 보낸다. (파이프 라이닝)
  + http 1.0은 하나의 ip당 하나의 도메인 운영이 가능. http 1.1은 여러 ip로 하나의 도메인 운영이 가능하다.


<img width="421" alt="image" src="https://user-images.githubusercontent.com/57162257/185845135-53c5ddc8-231b-4c2c-9c19-2df4501c8099.png">



</details>

-----------------------

<br>



<br>

-----------------------

### http2.0

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ Multiplexd Stream
  + <img width="965" alt="image" src="https://user-images.githubusercontent.com/57162257/185845962-4b009599-2c65-451a-a7ba-2284bfd704f8.png">
  + Connection당 여러개의 메시지를 주고 받을 수 있으며 순서에 상관없이 Stream으로 주고 받는다.

+ Stream Prioritization
  + Stream으로 전달시 렌더링 문제를 예방하기 위해 리소스 간의 의존관계에 따른 우선순위를 적용한다.

+ Server Push
  + <img width="750" alt="image" src="https://user-images.githubusercontent.com/57162257/185845983-276ac35c-c95d-47aa-a20c-aa52343e43d5.png">
  + 서버는 클라이언트에서 요청하지 않은 리소스도 보낼 수 있다.
  + http 1.1에서는 HTML을 요청했을때 그 안에 css, img가 있었다면 재 요청을 했다. 하지만 http 2.0에서는 HTML요청시 안에 css, img가 있다면 HTML문서에 포함된 리소스도 Push해서 반환해준다.

+ Header Compresion
  + <img width="700" alt="image" src="https://user-images.githubusercontent.com/57162257/185846030-7acce1d7-b2eb-4d91-bd61-5ea4272a2418.png">
  + Header에서 중복되는 내용이나 필드를 재전송하지 않아서 데이터를 절약한다.
  + http 2.0 이전에는 Header가 평문이였지만 http 2.0에서는 HashTable과 HPACK 헤더 압축 방식을 사용해서 데이터를 효율적으로 전송한다.




</details>

-----------------------

<br>



<br>

-----------------------

### TCP의 오류 제어, 흐름 제어

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 흐름 제어 : 송신 측은 수신 측의 데이터 처리 속도를 감안해서 전송할 데이터 크기를 제어한다.
  + Stop and Wait
    + 송신측이 수신측의 완료 패킷은 ACK를 받을 때까지 대기하고 전송하는 방법

  + Sliding Window
    + 송신측에서는 ACK를 받지 않아도 계속해서 데이터를 송신하는 방법
    + 수신측의 버퍼를 고려하여 수신측은 ACK에 남은 버퍼 크기를 담아서 전송하고 송신측은 남은 버퍼 크기를 고려하여 데이터를 전송한다.

+ 오류 제어 : 데이터가 유실되었거나 오류가 발생했을때 송신측에서 데이터를 재전송하는것.
  + Stop and Wait
    + 송신측에서 ACK를 기다리다가 타임아웃시 동일한 데이터를 전송하는 방법
    + <img width="323" alt="image" src="https://user-images.githubusercontent.com/57162257/185849036-2eccb373-20c2-43ab-97ad-89a5f15f162d.png">

  + Go back N
    + 송신측에서 여러개의 데이터를 전송한 후 특정 데이터에 대해 수신측에서 NACK를 보내면 해당 데이터부터 다시 요청하는 방법.
    + <img width="310" alt="image" src="https://user-images.githubusercontent.com/57162257/185848913-86968508-7f0b-4891-a3ed-8d64b713adb9.png">

  + Selective Repeat
    + Stop and Wait보다 효율적인 Go back N방식이지만 특정 데이터에 오류가 발생하면 그 이후의 데이터는 폐기처분되어 비효율적일 수 있다.
    + 에러난 데이터에 대해서만 선택적으로 재전송하는 방법
    + <img width="312" alt="image" src="https://user-images.githubusercontent.com/57162257/185849337-e82a6b7b-728d-4277-9d0c-857d494d6030.png">
    + 수신측의 버퍼에 쌓인 데이터가 연속적이지 못하다는 단점




</details>

-----------------------

<br>



<br>

-----------------------

### 포트와 소켓

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 포트
  + 네트워크를 통해 데이터를 주고 받는 통신 프로세스를 식별하기 위해 프로세스가 할당받는 고유한 값
  + 하나의 IP주소에서 통신 프로세스의 식별 값

+ 소켓
  + 네트워크 상에서 동작하는 프로그램간 통신의 종착점 (End Point)
  + 두 시스템간 네트워크 연결을 나타내는 객체




</details>

-----------------------

<br>



<br>

-----------------------

### 세션과 쿠키

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ HTTP는 connection less, stateless 의 특성을 가지기 때문에 서버는 클라이언트가 누구인지 매번 확인해야한다.
+ 쿠키
  + 사용자의 정보를 사용자 컴퓨터에 저장하는 작은 기록 파일.
  + 쿠키의 만료시간이 지날때까지 유지된다.
  + 클라이언트의 컴퓨터에 저장되어있기때문에 변질될 수 있다.

+ 세션
  + 서버에 사용자의 정보를 저장한다.
  + 브라우저 종료시 삭제된다.
  + Session Id만 가지고 서버에서 정보를 처리하기 때문에 쿠키보다 보안성이 좋다.

+ 세션보다 쿠키를 더 많이 사용하는 이유
  + 사용자의 요청이 많게 되면 사용자 정보를 저장하는 서버에서 부담이되기 때문에 쿠키를 사용한다.




</details>

-----------------------

<br>



<br>

-----------------------

### JWT

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 세션은 별도의 저장공간을 필요로 하고 확장시 세션을 분리시킬 기술을 설계해야한다.
+ JWT를 사용하면 서버에 JWT를 저장하지 않고 유효한 토큰 여부 검증만 하면 된다.
+ 하지만 탈취되어 악용가능성이 있기 때문에 유효기간을 짧게 가지고 Refresh토큰을 이용해 새 토큰을 받게 한다.



</details>

-----------------------

<br>



<br>

-----------------------

### OAuth

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 외부 인증 프로그램을 이용해서 접근 위임을 위한 개방형 표준 프로토콜.
+ 인증 (authentication) : 사용자 신원 확인
+ 인가 (authorization) : 기능 접근 권한 확인



</details>

-----------------------

<br>



<br>

-----------------------

### URI & URL & URN

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ URI (Uniform Resource Identifier)
  + 인터넷 자원을 식별하기 위한 주소

+ URL (Uniform Resource Locator)
  + 자원에 대한 구체적인 위치.
  + 특정 자원을 어떻게 가져와야하는지 명시하는 것.
  + test.com/food/salad.png : test.com 도메인에서 food 디렉터리에 있는 salad.png 이미지를 가져오는것.

+ URN (Uniform Resource Name)
  + 특정 자원에 대해서 위치에 영향을 받지 않는 유일한 이름 역할
  + 리소스의 위치를 옮기게 되어도 해당 자원을 가져오는데 영향을 받지 않음.




</details>

-----------------------

<br>



<br>

-----------------------

### REST API

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ REST
  + HTTP URI를 통해 자원을 명시하고 HTTP 메소드를 통해 자원을 처리하도록 설계된 아키텍처

+ REST API
  + REST 기반으로 만들어진 API

+ REST ful
  + REST 아키텍처를 따라 구현한 시스템

+ REST 규칙
  1. 후행 슬래시(/) 금지
     - test.com/board/
  2. 계층 관계시 슬래시(/) 사용
     - test.com/board/13
  3. URI 가독성을 위한 하이픈(-) 사용
     - test.com/board/my-first-board
  4. URI 작성시 소문자
  5. 확장자는 URI에 포함하지 않는다.
     - content-type에 미디어 유형을 넣어 본문 컨텐츠 처리
  6. 단어 사용시 복수형
  7. 단어 사용시 동사보단 명사



</details>

-----------------------

<br>



<br>

-----------------------

### CORS (Cross Origin Resource Sharing)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ cors는 교차 출처 리소스 공유로, 다른 출처의 URL을 요청하여 리소스를 가져오는 것을 말한다.
+ 목적
  + 악용 도메인이 사용자의 브라우저에서 쿠키를 탈취하여 다른 도메인(네이버, 카카오)의 URL정보를 가져와 사용자의 웹 브라우저에 올리는 것을 막기 위함.

+ 방법
  + 다른 도메인에서 요청을 보낼때 http header의 origin 속성에 출처의 protocol(http, https) + host + port를 작성하고 요청받는 서버에서 다른 도메인 (출처)으로 부터 온 요청을 허용하는 출처를 http header의 Access Control Allow Origin 미리 명시하여 웹 브라우저가 origin과 Access Control Allow Origin과 비교하여 허용 여부를 판단한다.

+ 종류
  + Simple Request
    + <img width="794" alt="image" src="https://user-images.githubusercontent.com/57162257/186048998-ffaf6627-4128-4d71-abc5-822732025f0d.png">
    + 실제 http header origin에 출처의 정보를 넣고 서버에서 응답할때 Access Control Allow Origin에 CORS를 허용하는 출처를 보내 동일한 출저일때만  허용한다.
    + 서버는 요청을 수행하고 CORS여부는 브라우저에서 판단하기 때문에 서버 데이터에 영향을 미치지 않는 GET이나 POST에 사용한다.

  + Prefilght Request
    + <img width="790" alt="image" src="https://user-images.githubusercontent.com/57162257/186048955-f7a13eae-eaa6-4bc2-adf9-75bddb4c33c1.png">
    + 실제 요청전  Prefilght라는 요청을 보내 Origin과 Access Control Allow Origin과 비교하여 허용된 출처인지 확인하고 실제 요청을 하게 하는 방법
    + 서버 데이터에 영향을 받을 수 있는 PUT, DELETE에 사용된다.




</details>

-----------------------

<br>



<br>

-----------------------

### 중간자 공격

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 데이터를 송수신 할때 제 3자가 데이터를 탈취하는 것.
+ 종류
  + 스피닝
    + 전송 중인 데이터 패킷을 캡처

  + 패킷 주입
    + 공격자가 일반 데이터 패킷에 악의적인 데이터 주입

  + 세션 하이재킹
    + 사용자의 연결 상태를 가로채는 것

  + 보안 소켓 계층 스트리핑
    + SSL 연결을 차단하여 HTTPS를 HTTP로 변경하는 것.




</details>

-----------------------

<br>



<br>

-----------------------

### WebSocket과 Socket.IO

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 웹 브라우저에서는 HTTP Protocol을 사용하기 때문에 한번의 요청이 오면 응답을 보내는 비연결형 단방향 구조로 통신한다.

+ 그렇기 때문에 웹 브라우저에서 TCP/IP 프로토콜을 사용하는 Socket처럼 connection이 유지되지 않아 실시간 통신이 불가능하다.

+ 웹 브라우저에서 실시간 통신을 지원하는 기술이 WebSocket

+ 장점

  + 비연결형인 HTTP Protocol에서도 실시간 통신이 가능하다.

+ 단점

  + HTML5 이전의 기술에서는 사용이 어렵거나 제한된다.

+ 동작

  1. 핸드 쉐이킹

     <img width="531" alt="image" src="https://user-images.githubusercontent.com/57162257/185889580-208d52a2-a949-4ce2-9e03-e1857bc49788.png">

     1. 브라우저와 서버를 연결하기 위해 브라우저에서 HTTP Uprade Header를 사용하여 HTTP Protocol을 WebSocket Protocol로 변경하여 웹 소켓 통신이 시작된다.

  2. 데이터 전송
     - 프레임이라는 데이터를 사용하여 메시지를 전송한다.
     - 종류
       - 텍스트 프레임
       - 바이너리 데이터 프레임

  3. 연결 종료
     - 연결 종료를 원하는 측에서 종료 프레임을 전송하면 연결이 종료된다.

+ Socket.io

  + HTML 5 이전 기술에도 WebSocket을 적용하기 위해 만들어진 라이브러리
  + WebSocket을 지원하는 브라우저에는 WebSocket으로 동작하고, 지원하지 않는 브라우저에는 HTTP Protocol을 이용해 실시간 통신을 흉내낸다.




</details>

-----------------------

<br>



<br>

-----------------------

### 로드 밸런싱

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 서버에 가해지는 부하 (Load)를 분산 (Balancing)해주는 기술
+ Load Balancer의 서버 선정 기준
  + Round Robine (라운드 로빈)
    + 요청을 순서대로 돌아가며 서버에 배정하는 방식
    + 서버와의 연결이 오래 지속되지 않는 경우 적합

  + Least Connection
    + 연결 개수가 가장 적은 서버 선택 (가장 많이 사용)

  + 해시 방식
    + 사용자의 IP를 해시함수로 매핑하여 특정 서버만 선택

  + 비율 할당 방식
    + 서버의 성능에 따라 비율을 정하고, 해당 비율 만큼 세션을 맺어주는 방식




</details>

-----------------------

<br>
