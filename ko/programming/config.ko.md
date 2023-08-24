{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - 구성 파일",
  "description":"CONFIG 파일을 생성하고 열 수 있는 API와 CONFIG 예제를 통해 CONFIG 파일 형식에 대해 알아보세요.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## .CONFIG 파일이란?
CONFIG 파일은 구성 파일로 알려져 있습니다. 여러 컴퓨터 소프트웨어에 대한 매개변수 및 기본 설정을 구성하는 데 사용됩니다. 일부 소프트웨어는 시작 시 **구성 파일**만 읽습니다. 다른 사람들은 주기적으로 구성 파일의 변경 사항을 확인합니다.

## CONFIG 파일 형식
**CONFIG 파일 형식**은 서버 프로세스, 소프트웨어 응용 프로그램 및 운영 체제 설정에 사용됩니다. 프로그래머는 일정 시간이 지나면 구성 파일을 계속해서 읽고 현재 프로세스에 변경 사항을 적용하도록 소프트웨어에 지시하는 코드를 작성할 수 있습니다. CONFIG 파일 시스템에 대한 확실한 표준이나 강력한 규칙은 없습니다. 예를 들어 Microsoft의 Web.config 파일은 [XML](/web/xml/) 기반 태그 집합으로 구성된 CONFIG 파일 형식에 속합니다. Microsoft Visual Studio 또는 다른 텍스트 편집기로 편집할 수 있습니다.

## 구성 파일의 예:
구성 파일은 규칙, 표준 또는 규칙에 따라 생성되지 않으므로 이러한 파일은 다른 형식을 사용하여 작성되었을 수 있습니다. .config 파일은 XML, [JSON](/web/json/) 또는 기타 형식을 기반으로 할 수 있습니다. 다음은 잘 알려진 운영 체제 및 소프트웨어에 대한 구성 파일의 예입니다.

### Linux의 구성 파일
모든 Linux 프로그램은 CPU가 일반적인 작업을 수행하기 위해 실행하는 **opcode** 목록을 유지하는 실행 파일입니다. 거의 모든 프로그램의 작업은 구성 파일을 변경하여 요구 사항에 맞게 사용자 지정할 수 있습니다. Linux 시스템의 여러 구성 파일은 /etc 디렉토리에 있습니다. 구성 파일은 다음 범주로 분류할 수 있습니다.
|카테고리|예시| 댓글|
---|---|---|
|액세스 파일|/etc/host.conf|네트워크 도메인 서버에 호스트 이름을 찾는 방법을 알려줍니다.|
|부팅 및 로그인/로그아웃|/etc/rc.d/rc.local|공식이 아닙니다. rc, rc.sysinit 또는 /etc/inittab에서 호출할 수 있습니다.|
|파일 시스템|/etc/mtools.conf|DOS 유형 파일 시스템의 모든 작업(mkdir, 복사, 형식 등)에 대한 구성.|
|시스템 관리|/etc/shells|시스템에서 사용할 수 있는 가능한 "쉘" 목록을 보유합니다.|
|네트워킹|/etc/gated.conf|게이트 설정. gated 데몬에서만 사용됩니다.|
|시스템 명령|/etc/logrotate.conf|동적 링커 구성.|
|Daemons|/etc/httpd.conf|웹 서버인 Apache의 구성 파일입니다. 이 파일은 일반적으로 /etc에 없습니다.|
|사용자 프로그램| /etc/lynx.cfg| 프록시 설정|
### AWS CONFIG 파일 예시
자주 사용하는 구성 설정 및 자격 증명은 AWS CLI에서 유지 관리하는 CONFIG 파일에 저장할 수 있습니다. CONFIG 파일은 다음 형식을 사용하는 일반 텍스트 파일이어야 합니다.
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG 파일 예
OpenSSH 클라이언트 측 구성 파일의 이름은 CONFIG이며 .ssh 디렉토리에 저장됩니다. SSH CONFIG 파일은 다음 구조로 구성됩니다.
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG 파일 예제
Python CONFIG 파일은 다음과 같습니다.

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## 참고문헌

* [리눅스 설정 파일 이해하기](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [구성 및 자격증명 파일 설정](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [파이썬 설정 파일](https://martin-thoma.com/configuration-files-in-python/)

