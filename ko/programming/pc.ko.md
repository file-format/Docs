{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC 파일 - Pro*C 소스 코드 파일 - .pc 파일이란 무엇이며 어떻게 열 수 있나요?",
  "description" : "PC Pro*C 소스 코드 파일 및 여는 방법에 대해 알아보세요.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-ko",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## PC 파일이란 무엇입니까?

PC 파일 또는 .pc 파일은 ProC 소스 코드 파일입니다. ProC는 C 또는 C++ 코드 내에 SQL 문을 삽입하기 위해 Oracle 데이터베이스와 함께 사용되는 사전 컴파일러입니다. Pro*C 파일을 컴파일하면 내장된 SQL 명령이 포함된 일반 C 또는 C++ 코드가 생성됩니다. 이를 통해 SQL 데이터베이스 작업을 C 또는 C++ 프로그램과 원활하게 통합할 수 있습니다.

Pro*C 파일의 기본 예는 다음과 같습니다.

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

이 예에서는 SQL 문 앞에 EXEC SQL이 붙어 Embedded SQL 문임을 나타냅니다. 이러한 명령문은 파일이 컴파일될 때 Pro*C 사전 컴파일러에 의해 처리되며 Oracle 데이터베이스와 상호 작용하기 위해 적절한 C 코드가 생성됩니다.

## PC 파일을 여는 방법은 무엇입니까?

PC 파일을 열려면 일반적으로 C 또는 C++ 소스 코드 편집을 지원하는 텍스트 편집기나 IDE(통합 개발 환경)가 필요합니다. 다음은 몇 가지 일반적인 옵션입니다.

1.  **텍스트 편집기:**
    
- **메모장**(Windows)
- **텍스트 편집**(맥)
- **gedit**(리눅스)
- **숭고한 텍스트**
- **아톰**
- **Visual Studio 코드**
2.  **통합 개발 환경(IDE):**
    
- CDT(C/C++ 개발 도구)가 포함된 **Eclipse**
- Visual C++가 포함된 **Visual Studio** 또는 C++ 확장이 포함된 Visual Studio Code
- **코드::블록**
- C/C++ 팩이 포함된 **NetBeans**
  
## 참고자료
* [프로*C](https://en.wikipedia.org/wiki/Pro*C)


