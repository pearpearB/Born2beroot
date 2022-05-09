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
ℹ 내가 선택하 운영체제나, 뭘 사용하고 있는 지 알아야 함
+ Q1 : the differences between `aptitude` and `apt`
+ Q2 : what `SELinux` or `AppArmor` is

`SSH` service port : `4242` only! 보안 이유로, root로 SSH 연결 금지! \
\
ℹ 디펜스 동안 SSH 새로운 계정으로 테스트할 것.  어떻게 작동하는 지 알아야 함 \
\
운영체제는 UFW방화벽 이용, 4242포트만 열어놓기 \

