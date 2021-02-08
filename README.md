# 네트워크관리사 2급

 **< 1과목 : TCP/IP >**

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

- - -
### 2021.02.05
* RIP는 경로를 설정하는 프로토콜

* 최대 홉이 15를 넘지 못하며 네트워크 상황 변화에 즉시 대처하지 못함

* nslookup : 호스트 이름을 입력해서 IP주소를 찾거나, IP주소를 사용해 호스트이름을 찾는데 사용

- - -
### 2021.02.08

* TCP는 UDP와 다르게 연결지향. 따라서 신뢰성있는 수신 송신이 가능하다.

* 송신측은 데이터를 패킷으로 나누어 일련번호, 수신측 주소, 에러검출코드를 추가한다.

* 서브넷 마스크(Subnet Mask): 하나의 네트워크 클래스를 여러 개의 네트워크로 분리하여 IP Address를 효율적으로 사용할 수 있다.   
서브넷 마스크는 목적지 호스트의 IP Address가 동일 네트워크상에 있는지 확인한다.   
서브넷 마스크를 이용하면, Traffic 관리 및 제어가 가능하다.

* P에 입력하는 범위가 256개가 존재한다 (0 ~ 255)256부터 2씩 나눈다.   
256 / 2 = 128 - 1 = 127 (A Class 범위 : 0 ~ 127)   
128 / 2 = 64 + 127 = 191 (B Class 범위 : 128 ~ 191)   
64 / 2 = 32 + 191 = 223 (C Class 범위 : 192 ~ 223)   
남은 32의 수는 16씩 나누어서 D Class와 E Class가 가진다.

* IP 헤더 필드들 중 처리량, 전달 지연, 신뢰성, 우선순위 등을 지정해 주는 것은?: A. TOS(Type of Service)

* Telnet = 23   
20 : FTP(data 전송)   
21 : FTP(data 전송 제어)   
22 : SSH   
23 : 텔넷   
25 : SMTP   
53 : DNS   
80 : 월드 와이드 웹(WWW) HTTP   
123 : NTP   
179 : BGP

* ARP(Address Resolution Protocol: 주소 결정 프로토콜)는 네트워크 상에서 IP 주소를 물리적 네트워크 주소(하드웨어 주소)로 대응(bind)시키기 위해 사용되는 프로토콜

* ICMP : 네트워크 컴퓨터에서 돌아가는 운영체제에서 오류 메시지를 전송받는 데 주로 쓰이는 프로토콜

* DNS 서버에 질의를 보내 IP Address와 도메인 주소의 결과를 알려주는데 사용될 수 있는 유틸리티는? A. Nslookup

* 네트워크 계층 프로토콜:   
RARP : 역순 주소 결정 프로토콜(Reverse Address Resolution Protocol)   
ICMP : 인터넷 제어 메시지 프로토콜(Internet Control Message Protocol)   
IGMP : 인터넷 그룹 관리 프로토콜(Internet Group Management Protocol)

* UDP는 상대방이 연결된 것을 확인하지 않고 보내기 때문에 확인 응답 번호(ASK)가 필요하지 않다.

* TFTP 는 데이터를 빠르게 송수신하기 위해 인증 과정 없이 UDP 세션을 통해 전송한다.   
네트워크를 통한 파일 전송 서비스이다.

* IPv6 헤더 형식에서 네트워크 내에서 혼잡 상황이 발생되어 데이터그램을 버려야 하는 경우 참조되는 필드는?   A. Priority

* SNMP는 네트워크 모니터링을 위해 사용되는 프로토콜이다.   
UDP 상에서 작동한다.   
비동기식 요청/응답 메시지 프로토콜이다.   
4가지 기능(Get, Get Next, Set, Trap)을 수행한다

* 특정 그룹에 속하는 모든 호스트에 메시지를 전송하는 방식을 멀티캐스팅(Multicasting)이라고 한다.   
IGMP (Internet Group Management Protocol)는 임의의 호스트가 멀티캐스트 그룹에 가입하거나 탈퇴할 때 사용하는 프로토콜이다.

**< 2과목 : 네트워크 일반 >**
### 2021.02.05
* 프로토콜의 가장 기본적인 기능 중에서 전송량, 전송속도 등을 조절하는 것은 Flow Control

* VPN: 네트워크 사설 망이라고도 부르며 보안성이 뛰어나며, 한대의 PC에 한대의 공인IP만 연결하면 되므로 비용적인 부분이 절감된다.

* 표현계층(Presentation Layer): 통신을 수행하는 다양한 정보의 표현 형식을 공통의 전송형식으로 변환하며 암호/복호, 압축, 인증 등의 기능을 수행하는 계층

* 스타형LAN: 모든 기기를 점 대 점으로 연결. 한대의 컴퓨터가 고장을 일으켜도 전체 네트워크에는 영향을 주지 않는다. 장애 발생시 해당 컴퓨터와 허브 사이만 점검해 문제를 쉽게 해결할 수 있다.새로운 컴퓨터를 네트워크에 추가로 설치하기 용이.

* IPv6: 128Bit로 구성. 멀티캐스트, 유니캐스트, 애니캐스트 사용. IPv4에 비해 해더가 단순하다. IP주소 확장 및 인증 및 보안기능이 IPv4에 비해 우수.

- - -
### 2021.02.08
* 패킷 교환망: 연결설정에 따라 가상회선과 데이터그램으로 분류된다.   
메시지를 보다 짧은 길이의 패킷으로 나누어 전송한다.   
블록킹 현상이 없다.

*

*
**< 3과목 : NOS >**
### 2021.02.05
* chage는 계정의 비밀번호를 관리하는 명령어. chgrp는 파일의 소유자 그룹을 변경할 때 사용하는 명령어. chmod는 파일의 허가권을 숫자로 변경하고자 할 때 사용. usermod는 사용자 계정을 변경할 때 사용

* Linux 디렉터리 구성: /tmp - 임시파일이 저장되는 디렉터리  
/boot - 시스템이 부팅 될 때 부팅 가능한 커널 이미지 파일을 담고 있는 디렉터리
/var - 시스템의 로그 파일과 메일이 저장되는 위치  
/usr은 시스템, 응용프로그램에서 필요한 파일들이 저장되어 있는 디렉터리

* 컴퓨터가 부팅될 수 있도록 Linux 운영체제의 핵이 되는 커널을 주 기억 장소로 상주시키는데 사용되는 부트 로더는? A. GRUB  
 GRUB는 컴퓨터가 시작될 때에 처음 실행되는 프로그램으로 운영체제를 불러오는 역할.   
 MBR - 하드디스크의 첫번째 파티션을 생성할 때 만들어짐   
 SWAP - 메모리의 여유 공간을 디스크에 확보

* -rwxr-x--x는 수치로 계산하게 된다면 r(4)w(2)x(1)로써 맨 앞의 r(4) + w(2) + x(1) = 7또한 rx는 r(4) + x(1) = 5, 그리고 마지막 x는 그냥 1이기 때문에 이 파일 모드는 751.

* top - 실시간으로 프로세스를 모니터링 할 수 있는 명령어   
kill - 프로세스를 종료시키는 명령어   
nice - 프로세스의 우선순위를 변경하는 명령어   
pstree - 프로세스를 트리형태로 보여주는 명령어

- - -
### 2021.02.06
* Linux 데몬:  
crond - 사용자가 지정한 프로그램을 특정 시간에 주기적으로 실행할 수 있도록 해주는 표준 유닉스 데몬   
named - 호스트 이름을 IP로 변환시켜 주는 DNS 데몬

* 앞서 내렸던 명령취소: shutdown –c

* 정방향 조회는 호스트 이름을 IP주소로 해석   
역방향 조회는 IP주소를 호스트이름으로 해석

* DNS에서 지원하는 레코드 형식:   
CNAME - 이미 지정된 이름에 대한 별칭 도메인 추가 시 사용.   
MX - 지정된 DNS 이름의 메일 교환 호스트에 메일 라우팅을 제공.   
A - DNS 이름과 호소트의 IP주소를 연결.   
PTR - DNS 서버에서 사용하는 리소스 중 도메인에 있는 특정 주소에 DNS 이름을 공급하는 매핑을 제공.

* httpd.conf - 웹 서버 운영시 서비스에 필요한 여러 기능들을 설정하는 파일

* 성능 모니터 도구: perfmon /report 입력

* 이벤트 뷰어 windows 로그: 응용 프로그램,보안,시스템,setup

* (BitLocker)비트로커는 마이크로소프트 윈도우 서버 2008 윈도우 10,7,8 운영 체제에 포함된 완전한 디스크 암호화 기능을 수행

* 3개의 로컬 사용자 계정: Guest, DefaultAccount, Administrator

* 클러스터 OS 롤링 업그레이드를 사용하면 관리자가 Hyper-v 또는 스케일 아웃 파일 서버 작업을 중지하지 않고 클러스터 노드의 운영체제를 업그레이드할 수 있다.

* FSRM(파일 서버 리소스 관리자)은 파일 서버에 저장된 데이터를 관리 및 분류 하는 데 사용할 수 있는 Windows Server의 역할 서비스

* wq는 저장후 종료   
q!는 저장하지않고 종료

* ps 명령어는 프로세스 정보만 보여주고, ps -ef까지 해줘야 현재 실행되고 있는 프로세스 목록을 보여줌.   
w : 로그온된 사용자의 정보와 로그온된 사용자의 현재작업을 보여줌   
at : 나중에 실행할 작업에 대한 설정, 검사, 삭제   
cron : 데몬 스케쥴링 명령어

* SAMBA   
인트라넷이나 인터넷에서 서버의 파일 및 인쇄기를 사용할 수 있는 프리웨어 프로그램.   
리눅스, 유닉스, OpenVMS, OS/2 등 다양한 운영 체계에 설치되는 SMB 및 공통 인터넷 파일 시스템(CIFS) 클라이언트/서버 프로토콜 기반의 프로그램이다.   
이 프로그램을 사용하여 다른 컴퓨터에 파일, 인쇄기, 기타 자원의 접근 요구를 할 수 있다. 삼바 SMB/CIFS 클라이언트를 smbclient라고 한다.

* 멀티 캐스트의 용도로 사용되는 IP 클래스는 D클래스

* 정방향 조회는 도메인 이름을 가지고 IP주소로 반환하는 것이고, 역방향 조회는 그 반대인 IP주소를 가지고 도메인 이름으로 바꾸는 것이다.

* /bin은 명령어가 있는 디렉터리

* Linux의 'fdisk' 명령어 옵션   
-l : list 현재 하드디스크 상태를 나타냄   
-d: 파티션 삭제   
-n: 새로운 파티션 생성  
-a: 부팅파티션 설정가능   
-t : 파티션 타입(용도?)변경가능

* Windows Server 2008 R2가 제공하는 파일 서비스:   
DFS를 이용해 여러 컴퓨터들에 있는 공유 폴더들을 묶어서 마치 하나의 폴더인 것처럼 사용할 수 있다.   
FSRM을 통해 사용자 별 용량을 제한할 수 있고, 특정 파일 유형의 업로드를 제한할 수 있다.   
NTFS 쿼터는 디스크 단위로 설정할 수 있으며, 디스크 속성에 할당량 탭을 통해 설정가능하다.

* nslookup 명령어는 도메인 네임을 입력하면 IP를 반환한다.

* SSL (Secure Sockets Layer)보안 소켓 계층을 이르는 말로, 인터넷에서 데이터를 안전하게 전송하기 위한 인터넷 통신 규약 프로토콜

* SSH서버는 패킷을 인캡슐화하는 과정을 거쳐 암호화를 시킨뒤 패킷이 도착하면 디캡슐화의 과정을 거친다.

* PowerShell: 시스템 관리를 위해서 설계된 명령 라인 셀 및 스크립팅 언어로 강력한 확장성을 바탕으로서버 상의 수많은 기능을 손쉽게 자동화.   
기존의 DOS 명령어와 약간 다르긴 하지만 사용할 수 있음   
대소문자 구분 x   
텍스트로 구성   
콘솔에서 대화형으로 사용 O

- - -
**< 4과목 : 네트워크 운용기기 >**
### 2021.02.06
* 로드밸런싱: 과부화가 발생하지 않도록 여러 루트로 분산하여 사용량, 처리량 및 지연율을 조정하는 역할

* 클라우드 컴퓨팅은 인터넷('클라우드')을 통해 서버, 스토리지, 데이터베이스, 네트워킹, 소프트웨어, 분석, 인텔리전스 등의 컴퓨팅 서비스를 제공하는 것을 말한다.

* 게이트웨이란 서로 다른 네트워크 상의 통신 프로토콜을 적절히 변환해주는 역할.게 이트웨이는 OSI 참조 모델의 전계층을 인식하여 전송방식이 다른 통신망도 흡수하여 서로 다른 기종끼리도 접속을 가능하게 한다.

* Router - 네트워크 계층   
Repeater - 물리계층 /근거리통신망(LAN)의 전송매체상에 흐르는 신호를 정형, 증폭, 중계   
bridge - 데이터링크 계층   
Gateway - 전송 계층

* 10BASE-T는 이더넷의 10Mbps 전송속도를 지원하며(전송 방식은 : 베이스밴드, 전송매체 : 꼬임선)을 사용

* Dummy Hub   
단순히 네트워크나 네트워크 장비들과의 연결과 신호 증폭 기능만을 가진 허브.   
한 개의 백본(backbone)에 포트 수만큼 연결을 하며 노드가 증가될수록 네트워크의 속도가 저하되는 단점이 있다. 따라서 20개 이하의 소규모 네트워크에 적합하다.

* RAID   
여러개의 하드 디스크를 하나의 디스크처럼 보이게 하는 기술   
RAID 0 /스트라이핑데이터를 여러디스크에 분산 저장. 장애시 데이터 복구X, 중복 기록X   
RAID 1 /미러링하나의 디스크에 데이터 저장시 다른 디스크에 동일내용 백업   
RAID 2 /해밍RAID 3 /가상 디스크 블록   
RAID 4 /전용 패리티   
RAID 5 /스트라이프 패리티   
RAID 6 /이중 패리티   
RAID 10: RAID 1가용성 + RAID 0 성능 혼합   
RAID 0+1: RAID 0 빠른속도, RAID 1 장애 대비책

* Router   
네트워크상의 패킷을 전달하는 네트워크 장비이다.   
하드웨어에 따라 패킷을 다시 적절한 크기로 분할하거나, 또는 재조립하고, 이들을 데이터 프레임의 형태로 캡슐화 하는 기능을 가지고 있다.   
패킷 전달을 위해 최적의 경로를 결정   
Network 계층에 대응

* OSPF(Open Shortest Path First) 프로토콜   
OSPF는 AS의 네트워크를 각 Area로 나누고 Area들은 다시 Backbone으로 연결이 되어 있는 계층구조로 되어있다.   
Link-State 알고리즘을 사용하여 네트워크가 변경이 되더라도 컴버전스 시간이 짧고 라우팅 루프가 생기지 않는다.   
VLSM(Variable Length Subnet Mask) 구성이 가능하기 때문에 한정된 IP Address를 효과적으로 활용할 수 있다.
