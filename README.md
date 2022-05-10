# Born2beroot
\
`VirtualBox` (또는 VirtualBox르 사용할 수 없을 경우 UTM) 설치 [🔹VirtualBox와 UTM 알아보기](https://velog.io/@pearpearb/42서울-Born2beroot)\
\
⚠ 서버를 설정하는 과제이므로 최소한의 서비스만 설치(GUI  설치 금지!; X.org 또는 기타 그래픽 서버를 설치 금지) \
\
latest stable of `Debian` 또는 latest stable of `CentOS` 선택 (시스템 관리가 처음이라면 Debian 추천) [🔹CentOS와 Debian 알아보기](https://velog.io/@pearpearb/42서울-Born2beroot)\
\
ℹ `CentOS` 설정은 복잡하기 때문에 `KDump`를 설정할 필요가 없음. `SELinux` 필수 (구성은 프로젝트의 요구 사항에 맞게), `AppArmor` for Debian 필수 [🔹SELinux와 AppArmor 알아보기](https://velog.io/@pearpearb/42서울-Born2beroot접근-통제)\
\
`LVM`을 사용해 최소한 2개의 암호화된 파티션을 만들어야 함 \
\
ℹ 내가 선택하 운영체제나, 뭘 사용하고 있는 지 알아야 함!
+ Q1 : the differences between `aptitude` and `apt`
+ Q2 : what `SELinux` or `AppArmor` is

`SSH` service port : `4242` only! 보안 이유로, root로 SSH 연결 금지! \
\
ℹ 디펜스 동안 SSH 새로운 계정으로 테스트할 것.  어떻게 작동하는 지 알아야 함 \
\
운영체제는 UFW 방화벽 이용, 4242 포트만 열어놓기 \
\
ℹ 가상 머신을 시작할 때 방화벽 활성화되어야 함. centOS 경우, 디폴트 방화벽 대신  UFW 방화벽을 사용해야 함. 설치 위해 DNF 필요.

+ 가상 머신 `hostname`은 42로 끝나야 함(예. intraID42). 평가 동안 이 호스트네임으 변경해야할 것.
+ 강력한 `password` 정책을 구현해야 함.
+ 엄격한 규칙에 따라 `sudo`를 설치하고 구성(설정)해야 함.
+ 루트 사용자 외에도 사용자 이름으로 로그인한 사용자가 있어야 함.
+ 이 사용자는 user42 및 sudo 그룹에 속해야 함

ℹ 디펜스 동안, 새로운 유저를 만들어야하고 그룹에 등록해야 함.\
\
강력한 `password` 정책을 구현으 구현하기 위해, 갖추어야 할 요구사항:

+ 비밀번호는 30일마다 만료되어야 함(30일마다 업뎃).
+ 최소 2일 후 변경 가능.
+ 사용자는 만료 7일 전, 경고메세지 받아야 함.
+ 비밀번호는 10자 이상, 대문자 소문자 포함, 연속된 동일한 문자 3개 이상 포함 불가.
+ 비밀번호는 유저의 이름 포함 불가
+ 다음 규칙은 root password에는 적용되지 않음: 비밀번호는 이전 비밀번호와 7자 이상 달라야 함.
+ 물론, root password는 이 정책을 따라야 함.

⚠ configuration files 설정 후, 루트 계정을 포함한 가상 머신에 있는 모든 비밀번호를 바꿔야 함.\





