Oracle Linux 다운로드 방법
==========================
1. edelivery.oracle.com/ 접속(로그인 필요)

2. 로그인 후 소프트웨어 검색창에 필요한 Oracle Linux OS 버전 검색 후 다운로드창 진입.

![image](https://github.com/ex-scarlet/work/assets/58895345/170ab22d-f1ff-4f19-b24e-7c6c7faef21a)

3. 버전 선택 후 Continue 클릭 시 다운로더가 받아집니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/5e54c195-ed1d-4ed5-ad54-ecbdddde8352)

4. 다운로더를 실행하면 ISO파일을 저장할 위치를 지정할 수 있습니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/84edf697-0780-4835-9389-58f27fb32935)

VMware에서 Oracle Linux 설치 방법(Custom 설치 진행)
=================================

1. VMware 설치 후 Create a New Virtual Machine 클릭

![image](https://github.com/ex-scarlet/work/assets/58895345/11a492e3-88d5-4370-b33e-25a29ed3ff92)

2. Typical 또는 Custom을 선택하여 진행

![image](https://github.com/ex-scarlet/work/assets/58895345/871e0ac8-275e-4d90-8b08-f7fc3f9930a3)

3. 워크스테이션 버전 선택 후 진행

4. 설치할 OS파일을 설정해주는 창

![image](https://github.com/ex-scarlet/work/assets/58895345/b99ff4b8-258d-4cfe-a8a8-c7ba4cb65ec5)

5. 설치할 OS의 종류와 버전을 찾습니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/dc1fbe6d-eee6-4d26-8d39-f3b7fcbfb0d2)

6. VM 이름과 설치 위치를 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/02c83ad4-c3ea-4245-a250-b16b48a42b3d)

7. VM에 할당할 프로세서 개수를 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/1b08b51a-b4b3-4aa7-8e5c-5d0288930173)

8. VM에 할당할 램의 용량을 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/27f8c2f9-0306-4f13-a832-2d73c845967a)

9. VM의 네트워크 타입을 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/2accf2af-0413-49b3-9cf3-d59ae6dbafcd)

10. VM의 I/O 컨트롤러 타입을 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/6799da1c-9679-4b8c-8a99-12b387bd6add)

11. VM의 디스크 타입을 지정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/a71593a9-6805-4b0c-b5af-838f4c231103)

12. 어떤 디스크를 사용할 것인지 결정합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/52200edb-6b4e-4428-b40d-6d1f5bdd40ef)

13. 디스크의 용량을 지정해줍니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/0687af7f-b1ae-4672-9896-f1e3543a0250)

14. 만든 VM의 사양을 확인 후 Finish를 눌러줍니다.

15. VM settings에 들어간 후 CD/DVD에 들어가 기존에 받아두었던 ISO 파일을 찾아서 적용시킵니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/a6aff0a7-d30c-4855-980b-839dc1d42c59)

16. VM을 실행시킵니다.

17. 리눅스 OS 설치 중 INSTALLATION DESTINATION, 디스크 선택 후 Custom을 선택합니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/f0d7bf5f-dc0f-43d6-a3cb-00ec68579296)

18. MANUAL PARTITIONING +버튼 선택 후 /boot, swap, / (root) 총 3가지 파티션으로 나누어줍니다
    /boot에는 부팅 커널이 들어가며, swap은 램이 부족할 때 예비로 사용할 수 있는 하드의 용량입니다.

![image](https://github.com/ex-scarlet/work/assets/58895345/c443cf32-f8d9-4c38-a0f2-c6000ea24b51)

    


