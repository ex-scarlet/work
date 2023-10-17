JAVA 환경 변수 설정하기
=======================

1-1. 윈도우 하단 검색 칸에 __환경 변수__ 를 입력하여 시스템 환경 변수 편집 기능에 진입합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/a73be6f8-af36-4d91-91e4-48e3b6be2376)

1-2. 또는 윈도우 하단 검색 칸에 __내 PC__ 를 입력 후 속성에 들어간 후 우측에 있는 __고급 시스템 설정__ 을 클릭 후   
     환경 변수 편집 기능에 진입합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/92718989-fcab-410e-a19b-8e0a3e767a89)

![image](https://github.com/ex-scarlet/work/assets/58895345/884b4849-3a83-49ef-add1-8fb9bda7f2ab)

2. __시스템 변수__ 에서 새로 만들기 버튼을 클릭 후 작성되어 있는 정보를 넣고 확인 버튼을 클릭합니다.
   변수 이름은 __JAVA_HOME__ , 변수 값은 JDK를 설치한 폴더의 경로를 찾거나 작성하면 됩니다.
   
![image](https://github.com/ex-scarlet/work/assets/58895345/9658991d-9f48-452f-aa92-a8e22b1e2637)

4. 마찬가지로 __시스템 변수__ 에서 새로 만들기 버튼을 클릭한 후 작성되어 있는 정보를 넣고 확인 버튼을 클릭합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/6c028fc3-76c3-42f0-9328-7230c5655076)

5. __시스템 변수__ 리스트에서 __PATH__ 를 더블클릭하거나 클릭 후 편집 버튼을 클릭하여 편집 창에 진입합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/bdfc98e1-d56f-45e3-a227-fc29495fb73e)

6. 우측의 새로 만들기 버튼을 클릭한 후 __%JAVA_HOME%\bin__ 을 입력한 후 __위로 이동__ 버튼을 클릭하여 맨 위로 올린 후
   확인 버튼을 클릭합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/b7ce2738-09ec-4801-88fe-b455daa8f5f1)

여기까지 JAVA 환경 변수 편집을 완료하였습니다. 이제 제대로 인식이 되었는지 cmd 창을 연 후   
javac -version, java -version을 입력하여 설치된 jdk 버전이 제대로 출력되는지 확인합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/5a25981e-e035-4fcc-9320-2226b8bf8dfb)

사용자 변수와 시스템 변수의 차이
================================

#### 사용자 변수
사용자 변수는 말 그대로 로그인을 한 사용자에 대한 변수를 이야기합니다.  
user1 계정에만 등록한 변수는 user1 cmd 창에서 java -version 또는 javac -version을 입력하면  
자바 버전에 대한 정보가 출력되지만 user2 계정에서는 출력되지 않습니다.  
즉 모든 사용자가 아닌 __각각의 사용자(계정)만 권한을 준다__ 라고 할 수 있습니다.

#### 시스템 변수
시스템 변수는 사용자 변수와 반대의 개념을 가지고 있습니다.
사용자(계정) 개별로 권한을 부여하는 것이 아니라 컴퓨터(시스템) 자체에 권한을 부여하는 것이라  
모든 사용자가 동일하게 java -version을 입력하면 같은 출력값을 얻을 수 있습니다.


