게이트웨이(Gateway)란?
===============================

1. 게이트웨이의 정의

   - 컴퓨터 네트워크에서 게이트웨이(Gateway)란 한 네트워크(segment)에서 다른 네트워크로 이동하기 위해 거쳐야 하는 지점입니다.
   - 게이트웨이(Gateway)는 서로 다른 네트워크(이기종 네트워크)를 연결해줍니다. 서로 다른 네트워크의 프로토콜이 다를 경우에
     중재 역할을 해줍니다.
   - 하위 계층(1~3계층)에서 주로 라우터가 이러한 역할을 합니다.
   - 상위 계층(4~7계층)에서 상이한 프로토콜들 간의 특수한 변환을 담당하는 복잡한 S/W를 수행하는 서버를 의미하기도 합니다.  
     예시로, 전자우편을 여러 양식으로 바꿔주는 Mail Gateway가 있습니다.

2. 비유를 통한 이해

   - 게이트웨이는 다른 언어를 사용하는 두 사람 사이에 통역사나 번역기와 비슷하다고 볼 수 있습니다.
     학생과 논문, 외국 원서 사이를 중재해주는 구글 번역기와 게이트웨이가 유사하다고 볼 수 있습니다.
   - 게이트웨이는 다른 화폐를 사용하는 두 국가 사이에 환전소와 비슷하다고 볼 수 있습니다.
   - 자동차 도로로 비유를 하면 게이트웨이는 톨게이트와 비슷합니다. 한 도시에서 다른 도시로 이동하기 위해
     톨게이트를 지나야 하는 상황과 비교하면 좋습니다.

3. 역할 및 특징

   - 일반적으로 게이트웨이의 주소는 IPv4에서 4번째 옥텟 ex) 192.168.1.xxx 만 다른 경우가 많습니다.
   - 집 컴퓨터에서 인터넷에 접속하려는 경우 집 -> 공유기 -> 인터넷 제공 회사 라우터 -> 인터넷망과 같은 경로를 따라갑니다.
     이 때, 공유기와 인터넷 제공 회사의 라우터는 이전의 단계에서 다음 단계로 넘어 갈 때의 게이트웨이 역할을 담당합니다.
     인터넷에 접속하기 위해서는 수많은 게이트웨이를 거쳐야 합니다.
   - 이 때, 거치는 게이트웨이의 수를 홉 수(Hop count)라고 합니다.

     