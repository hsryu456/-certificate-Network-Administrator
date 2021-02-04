# 네트워크관리사 2급

- - -

## **< 1과목 : TCP/IP >**

### 2021.02.04

* ping은 ICMP 메시지를 사용한다.

* ping은 인터넷이나 네트워크가 안될 때, 네트워크에 있는 호스트들의 상태를 점검할 때 사용하는 응용프로그램이다.

* ICMP는 전송상의 에러를 확인할 수 는 있지만 정정할 수는 없다.

* TCP는 패킷 전송시 수신측의 대한 인증이 필요하지만 UDP는 필요하지 않다.

* TCP는 대용량의 데이터나 중요한 데이터 전송에 사용되며 반대로 UDP는 단순한 메시지 전송에 주로 사용된다.

* TCP는 신뢰성이지만 UDP는 비신뢰성이라 송수신 간의 세션이 수립될 필요없이 전송이 가능하다.

* 일반적으로 라우터의 한 홉(Hop)을 통과할 때마다 TTL 값이 '1' 씩 감소한다.

* Ping과 Tracert 유틸리티는 특정 호스트 컴퓨터에 접근을 시도하거나 그 호스트까지의 경로를 추적할 때 TTL 값을 사용한다.

* IP 패킷이 네트워크상에서 얼마동안 존재 할 수 있는가를 나타낸다.

* D Class 는 IPv4 Class 중에서 멀티캐스트 용도로 사용된다.

* HOP Limit는 8비트 데이터그램 생존기간을 의미하며, 혼잡이 발생할 때 Traffic Class필드(priority) 데이터그램을 버린다.

* IP 패킷은 네트워크 유형에 따라 전송량에 있어 차이가 나기 때문에 적당한 크기로 분할하게 된다. 이때 기준이 되는 것은? A. MTU

* ARP,RARP프로토콜은 네트워크계층에서 동작한다.

* ARP는 IP주소를 알고있고, 하드웨어 주소를 모를 때 사용된다.(하드웨어의 정확한 번지를 알아내기 위해 사용) RARP는 반대로 하드웨어 주소를 알고 IP주소를 모를 때 사용.

* RARP는 MAC 주소를 알고 있는 상태에서 그 MAC 주소에 대한 IP Address를 알아낼 때 사용한다.

* 127.0.0.1은 루프 백 주소이다.물리적인 네트워크 카드의 이상여부를 체크할 때 사용.

* NAT는 사설 IP 주소를 공인 IP 주소로 바꿔주는데 사용하는 통신망의 주소 변환기술을 말한다.(NAT는 해커와 같은 외부의 칩입자들을 원천 봉쇄할 수 있으며, 내부 사용자들이 공인 IP로 인터넷에 쉽게 접속할 수 있음.)

* 오류 제어는 데이터 링크 계층에서 사용된다. SNMP는 응용계층.

* 기존 HTTP는 보안성이 약하지만 HTTPS는 보안이 강하다.(인증은 어느 방식이나 필요하며 HTTPS는 암호화된 SSL/TLS를 전달한다.)

* SSH는 tcp/22번을 이용

* TCP 3-Way Handshaking 연결수립 절차

      SYN - tcp에서 세션을 성립할 때 가장먼저 보내는 패킷, 시퀸스 번호를 임의적으로 설정하여 세션을 연결하는데 사용된다.
      RST - 재설정을 하는 과정이며 양방향에서 동시에 일어나는 중단 작업. 비정상적인 세션 연결 끊기에 해당한다.
      ACK - 상대방으로부터 패킷을 받았다는 걸 알려주는 패킷으로 다른 플래그와 같이 출력되는 경우도 있음. ACK응답을 통해 보낸 패킷에 대한 성공, 실패를 판단하여 재전송 하거나 다음 패킷을 전송한다.

* UDP 패킷의 헤더에 속하는 것

      Source Port : 송신 측의 응용 프로세스를 식별하기 위한 포트번호.
      Destination Port : 수신 측의 응용 프로세스를 식별하기 위한 포트번호.
      Checksum : 전송 중 세그먼트의 손상여부를 확인
