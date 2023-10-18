Oracle 19c 설치 전 해야 할 일
=============================

1. root 계정으로 로그인 한 다음 터미널 진입 후 업데이트 실행

   [root@oel7 ~]# yum update


2. 설치를 진행할 것인지 물어보는 알림. y를 입력해 설치를 계속 진행합니다

   ![image](https://github.com/ex-scarlet/work/assets/58895345/c3531105-d547-4273-9fa8-e7e9f68d0b55)

3. 업데이트가 끝나면 준비작업에 들어갑니다. (/etc/hosts 설정)

   [root@oel7 ~]# vi /etc/hosts
   
4. OS를 설치할 때 정했던 hostname과 ip를 입력합니다.

   ![image](https://github.com/ex-scarlet/work/assets/58895345/e099eaf1-146b-48b6-8bf9-36d76ed0e403)

네트워크 자동 설정
==================

1. 오라클 DB를 설치하기 전 버전에 맞는 preinstall 파일을 설치해주어야 합니다.

   [root@oel7 ~]# yum -y install oracle-database-preinstall-19c

2. 유저 및 그룹을 수정합니다.

   [root@oel7 ~]# usermod -g dba -G dba oracle 

3. 패스워드를 설정합니다.
   
   [root@oel7 ~]# passwd oracle

4. selinux를 permissive 설정합니다.
   
   [root@oel7 ~]# vi /etc/selinux/config
   ![image](https://github.com/ex-scarlet/work/assets/58895345/9503660c-3f89-4745-8248-86124f7c6889)

5. 방화벽을 해제합니다

   [root@oel7 ~]# systemctl stop firewalld
   [root@oel7 ~]# systemctl disable firewalld

6. 설치 경로를 생성합니다.

   [root@oel7 ~]# mkdir -p /ORA19/app/oracle/product/19.0.0/db_1/
   [root@oel7 ~]# mkdir -p /ORA19/app/oradata
   [root@oel7 ~]# chown -R oracle:oinstall /ORA19
   [root@oel7 ~]# chmod -R 775 /ORA19

7. 새로 만든 oracle 계정의 위의 경로에 oracle database 19c 파일 설치 후 권한 부여

   ![image](https://github.com/ex-scarlet/work/assets/58895345/5dd46dec-4b15-4a64-a579-a15ca08d1619)

8. 앞에서 만든 oracle 계정으로 접속 후 .bash_profile 파일 수정

   # su - oracle
   $ vi .bash_profile
   export TMP=/tmp
   export TMPDIR=$TMP
 
   export ORACLE_HOSTNAME=oel7
   export ORACLE_UNQNAME=oracle19
   export ORACLE_BASE=/ORA19/app/oracle
   export ORACLE_HOME=$ORACLE_BASE/product/19.0.0/db_1
   export ORA_INVENTORY=/ORA19/oraInventory
   export ORACLE_SID=oracle19
   export DATA_DIR=/ORA19/app/oradata
   export PATH=/usr/sbin:/usr/local/bin:$PATH
   export PATH=$ORACLE_HOME/bin:$PATH
   export LD_LIBRARY_PATH=$ORACLE_HOME/lib:/lib:/usr/lib
   export CLASSPATH=$ORACLE_HOME/jlib:$ORACLE_HOME/rdbms/jlib
 
   export DISPLAY=192.168.~.1:0.0

9. 이제 설치파일 압축을 해제합니다.

   $ cd $ORACLE_HOME
   $ unzip LINUX.X64_193000_db_home.zip

10. 압축 해제가 완료되면 다시 루트로 돌아가 xhost + 명령어를 실행해줍니다

    ![image](https://github.com/ex-scarlet/work/assets/58895345/cf00cc58-6a0b-4e65-8e19-e5155082ee82)

    그리고 xdpyinfo를 입력하여 정상 출력이 되는지 확인합니다.
    오류가 난다면, __export DISPLAY=:0.0__ 을 입력한 후 다시 xhost + 부터 입력합니다.

11. 그리고 su - oracle을 이용해 oracle 계정에 접속, cd $ORACLE_HOME을 이용하여 runInstaller 파일이 있는 곳에 접속합니다.

12. 여기서도 루트에서 한 것처럼 __export DISPLAY=:0.0__ 을 입력한 후 xhost + 명령어를 실행합니다.

    ![image](https://github.com/ex-scarlet/work/assets/58895345/7cd6722c-8c03-457d-9319-2c873989f5d4)

13. 그리고 ./runInstaller 을 입력하면 Oracle 19c 설치 화면이 나옵니다.

    ![image](https://github.com/ex-scarlet/work/assets/58895345/1e8e0721-e87a-4319-84eb-b47af99bed80)






   


