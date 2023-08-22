DUP!(Duplication) 발생 원인
==============

1. DUP! 발생은 icmp sequence number가 중복된다는 의미입니다.

2. 유추해 볼 수 있는 사항
   - 동일 네트워크에 IP가 중복된 경우.(Gateway IP가 충돌할 경우 DUP!가 계속 발생함)
   - LAN 구간 Loop 발생시 DUP! 발생함.

3. Service_BB에서도 DUP 메시지 확인해보기.

해결방안
=============

1. VMware 가상 인터페이스 IP와 Service_BB 인터페이스 IP 중복되는지 확인 후 수정하기.

2. VMware 가상 인터페이스의 IP는 사용할 필요가 없기 때문에 사용하지 않는 IP로 재할당 해보기
