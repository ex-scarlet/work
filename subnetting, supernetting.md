subnetting(서브네팅)이란?
==

한 개의 네트워크를 서브넷 마스크를 이용하여 여러개의 서브넷 네트워크로 분할하는 방법

그렇다면 왜 한개의 네트워크를 여러개로 나눌까?

극단적이지만 A클래스를 일반 가정집에 부여한다면, 16,777,214개 되는 호스트를 낭비할 것입니다. 이러한 문제로 인하여 효율적으로 사용할 수 있도록 한 방법이 서브넷팅입니다.

1. 서브넷 마스크를 사용하여 Host Network로 변환합니다.
2. 네트워크 주소부분의 비트를 연장하고 그 나머지 부분이 호스트의 식별자가 됩니다.
3. 각 네트워크에 속해있는 호스트들은 같은 영역에 존재하기에 라우터까지 거치지 않고도 통신할 수 있습니다.
4. 서브넷 마스크는 255와 0으로 이루어져 있습니다.'
   - 255는 네트워크부분이며 0은 호스트부분입니다.
  
5. 호스트 부분에서 IP를 쪼개는 개념입니다

서브네팅 계산ㅂ법
===
Host id를 네트워크아이디로 변화하기 위해 한 비트씩 가져올 때마다 네트워크 크기는 2배로 증가하고 호스트 수는 2배로 나누어지게 됩니다.
2진수로 표현하였을 떄 네트워크 아이디 부분은 1이 연솏적으로 있어야 하며 호스트 ID 부분은 0이 연속적으로 있어야 한다 중간에 1이나 0이 섞이면 나열될 수 없습니다.
예를 들면 ip 네트워크 주소가 192.168.1.0이면 브로드캐스트 주소는 192.168.1.255입니다.

ㅎ지만 네트워크가 분리되므로 서로가 통신하려면 라우터를 통해서만 통신이 가능하게 됩니다.

슈퍼네팅이란?
==
여러 개의 작은 네트어크를 하나의 커다란 네트워크로 바꾸는 작( 여러 루트를 하나의 루트로 요약
서브넷 마스크를사용하여 네트워크를 호스트로 변환합니다.
바로 문제로 ㄱㄱ