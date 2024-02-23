{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "쉘 스크립트 - Ubuntu 및 Linux에서 실행하는 방법",
  "description":"Shell Script가 무엇인지, Ubuntu 및 Linux에서 실행하는 방법에 대해 알아보세요.",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-ko",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## 쉘 스크립트란 무엇입니까?

쉘 스크립팅에는 **쉘 스크립트**라고도 하는 일반 텍스트 파일에 일련의 명령을 작성하는 작업이 포함됩니다. 이러한 스크립트는 명령줄 해석기인 셸에 의해 실행됩니다. 가장 일반적인 껍질에는 다음이 포함됩니다.

1. 배쉬(Bourne Again SHell)
2. Zsh(Z 쉘)
3. 물고기.

쉘 스크립트는 단순한 한 줄짜리 프로그램부터 복잡한 프로그램까지 다양하며 파일 조작, 시스템 관리, 반복 작업 자동화 등 다양한 작업을 수행하는 데 사용됩니다.

## 쉘 스크립팅의 이점:

1.  **자동화:** 셸 스크립트를 사용하면 사용자는 반복 작업을 자동화하여 시간을 절약하고 인적 오류 가능성을 줄일 수 있습니다.
    
2.  **사용자 정의:** 사용자는 특정 요구 사항에 맞게 스크립트를 생성하여 높은 수준의 사용자 정의를 제공할 수 있습니다.
    
3.  **일괄 처리:** 셸 스크립트는 여러 명령을 순서대로 실행해야 하는 일괄 처리 작업을 처리하는 데 탁월합니다.
    
4.  **시스템 관리:** 셸 스크립트는 일반적으로 백업, 로그 순환, 소프트웨어 설치 등의 시스템 관리 작업에 사용됩니다.

## 간단한 쉘 스크립트 작성:

인사말 메시지를 인쇄하는 기본 셸 스크립트를 만들어 보겠습니다. 텍스트 편집기를 열고 `greeting.sh`라는 파일을 만듭니다. 다음 줄을 추가합니다.

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

파일을 저장하고 터미널에서 다음 명령을 실행하여 실행 가능하게 만듭니다.

```
chmod +x greeting.sh
```

이제 스크립트를 실행할 수 있습니다.

```
./greeting.sh
```

출력은 다음과 같아야 합니다.

```
Hello, welcome to the world of shell scripting!
```

## Ubuntu 및 Linux에서 쉘 스크립트 실행:

이제 **Ubuntu 및 Linux에서 .sh 파일을 실행하는 방법**에 대해 설명하겠습니다.

1.  **스크립트를 실행 가능하게 만들기:** 쉘 스크립트를 실행하기 전에 실행 가능한지 확인하십시오. 앞에서 설명한 대로 `chmod` 명령을 사용합니다.
    
2.  **스크립트 디렉토리로 이동:** 터미널을 열고 `cd` 명령을 사용하여 쉘 스크립트가 포함된 디렉토리로 이동합니다.
    
3.  **스크립트 실행:** 터미널에 './scriptname.sh'를 입력하고 scriptname을 실제 스크립트 이름으로 바꿔서 스크립트를 실행하세요.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Bash 명령 사용:** 스크립트가 `#!/bin/bash`(**shebang**이라고도 함)로 시작하는 경우 `bash` 명령을 사용하여 실행할 수도 있습니다.

```
bash greeting.sh
```

## 쉘 스크립트에서 $@는 무엇을 의미합니까?

쉘 스크립트에서 `$@`는 스크립트에 전달된 모든 명령줄 인수를 나타냅니다. 인수 목록을 별도의 엔터티로 참조하는 데 자주 사용됩니다. `$@`와 같이 큰따옴표 안에 사용하면 공백과 특수 문자를 고려하여 개별 인수를 유지합니다.

간단한 설명은 다음과 같습니다.

- `$@`: 스크립트나 함수에 전달된 모든 위치 매개변수(인수)를 나타냅니다. 각 인수는 별도의 단어로 처리됩니다.
    
- `$@`: 큰따옴표로 묶은 경우 인수 구분을 유지하여 개별 인수 내에 공백이나 특수 문자를 허용합니다.
    

다음은 설명하기 위한 간단한 예입니다.

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

예를 들어 인수를 사용하여 이 스크립트를 실행하는 경우:

```
bash example.sh arg1 "argument 2" arg3
```

다음과 같이 출력됩니다.

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

보시다시피 `$@`는 모든 인수를 나타내며 `$@`는 공백이 포함되어 있어도 개별 인수를 유지합니다.

