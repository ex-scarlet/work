OSI 7Layer(계층) Review
=======================================================================================================

### OSI 7계층이란?
 - 네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말합니다.
   1. 나눈 이유
      - 통신이 일어나는 과정을 단계별로 파악할 수 있기 때문입니다.
      - 7단계 중 특정한 곳에 이상이 생기면 다른 단계의 S/W를 건드리지 않고 이상이 생긴 단계만 고칠 수 있기 때문입니다.
      - 

### __7계층: Application(응용 계층)__
 - 사용자의 응용프로그램과 통신하는 계층.
 - 네트워크를 이용하려는 프로그램과 사용자에게 서비스를 제공합니다.
 - Protocol: DNS, DHCP, Telnet, SSH, HTTP, FTP 등이 있습니다.

### __6계층: Presentation(표현 계층)__
  - 데이터를 주고 받을 때 데이터를 적절히 표현: 0과 1로만 이루어진 data를 문자와 그림인지를 구분하여 표현합니다.
    -> 파일 뒤에 확장자가 붙는 것과 같습니다.
  - 보내는 방향의 응용 계층에서 받은 정보를 받는 방향의 응용계층에서 읽을 수 있게 해 줍니다.
  - 압축 / 해제하는 일과 암호화 / 복호화를 합니다.
  - Encoding / Decoding, File format
  - 만약 데이터가 변환되어야 한다면 표현 계층에서 책임집니다. ex) ASCII -> EBCDIC

### __5계층: Session(세션 계층)__
  - 네트워크를 이용하여 통신하는 두 프로세스 간의 논리적인 연결
  - 전자결제 시 뒤로가기 클릭: 세션 만료 또는 종료 문구가 출력되는 것
    (웹 브라우저와 해당 기관, 은행 프로그램의 연결이 논리적으로 끊어진 것, 순차적으로 진행되어야 하는데 이를 역으로 가면 연결이 끊어질 수 밖에 없습니다.)
  - Protocol: NetBIOS, SSL(Secure Socket Layer), TLS(Transport layer Secure)  
    SSL, TLS는 암호화와 관련됩니다.
  - 압축, 암호화, 표현(.확장자)

### __4계층: Transport(전송 계층)__
  - 하위 계층의 데이터 이동 시 신뢰성 제공
  - 상위 계층의 서비스(Protocol 구분), Port 주소로 구분합니다.
  - Data를 나누고, 나눠진 Data 조립, 즉 Segment(조각)로 나누어 전송
    -> 이를 원래 Data로 복원
  - Protocol: TCP -> 오버헤드가 크다(속도가 느림), Stateful(상태확인)  
              UDP -> 오버헤드가 적다(속도가 빠름), Stateless(상태미확인)
  - 주소: Port(0~65535) - 어떤 프로그램으로 가야 할지를 지정

### __3계층: Network(네트워크 계층)__
  - 두 시스템 간 연결성과 경로 선택(Routing) -> 목적지까지 가기 위한 경로
  - IP 주소를 사용: TCP/IP 망에서 원하는 목적지까지 데이터를 전달하기 위해 만들어진 표준
  - Data를 Packet단위로 분할하고 전송한 후 다시 합치는 작업
  - Protocol: IP, ICMP
  - PDU(Protocol Data Unit): Packet
  - 장비: Router

### __2계층: Data Link(데이터 링크 계층)__
  - 로컬 시스템 간 물리적 연결
  - 물리적 노드에서의 통신을 담당, 물리적 링크를 통해서 데이터 링크를 신뢰성 있게 전송하고  
    Bit(비트)를 Frame(프레임)이라는 논리적 단위로 구성
  - MAC 주소로 장비 구분 -> Data 전송
  - ARP: IP주소를 MAC 주소로 변환
  - RARP: MAC 주소를 IP 주소로 변환
  - Protocol: ARP, Ethernet, Token Ring, PPP, SLIP, HDLC, X.25, ATM 등
  - Flow Control(흐름 제어), Error Control(오류 제어) -> Checksum -> Footer의 역할
  - PDU: Frame
  - 장비: Switch, Bridge
  - 스위치의 기능(Flooding, Learning, Forwarding, Aging, Filtering)

### __1계층: Physical(물리 계층)__
  - Data가 0과 1, 즉 Bit로 변환이 되어 보내지며 데이터 전송만 해줌, 전기적 신호 전송
  - 장비: Cable, Repeater, Hub
  - 출발지가 목적지를 찾기 위하여 패킷을 보냄
  - 목적지를 발견하여 학습함
  - 300초 주기로 플래쉬, 에이징
  - 스위치 하면 콜리젼 도메인 한다는 것이 필터링하여 충돌을 막아준다는 것(이해가 잘 안되어 계속 찾아볼 예정)
