{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "확장자", "파일", "형식", "시스템", "동적 링크 라이브러리", "설정", "프로그램", "컴퓨터", "응용 프로그램"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - 동적 링크 라이브러리",
  "description":"DLL 파일 형식과 DLL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .DLL 파일이란? ##

DLL 파일 또는 동적 링크 라이브러리는 실행 파일의 유형입니다. 장치에서 가장 일반적으로 발견되는 확장 파일 중 하나이며 일반적으로 Windows의 System32 폴더에 저장됩니다. DLL 확장 파일은 Microsoft에서 개발했으며 널리 사용됩니다. 높은 인기도를 자랑합니다. DLL은 Windows 서버에서 프로그램/응용 프로그램을 위해 설계 및 적용되는 *드라이버/절차/기능/속성*을 포함하는 선반으로 작동합니다. 단일 DLL 파일은 다양한 Windows 프로그램 간에 공유할 수도 있습니다. 이러한 확장 파일은 파일 쓰기 및 읽기, 설정 외부에 있는 다른 장치와의 연결과 같은 프로그램에서 다양한 기능을 활성화하고 실행하는 역할을 하므로 장치에서 Windows 프로그램을 원활하게 실행하는 데 중요합니다.
그러나 이러한 파일은 모든 버전의 Windows(Windows 7/Windows 10 등)를 지원하는 장치에서만 열 수 있으므로 Mac OS를 지원하는 장치에서는 직접 열 수 없습니다. (Mac OS에서 DLL 파일을 열려면 다양한 외부 응용 프로그램이 도움이 될 수 있습니다.)


## DLL 파일 형식 ##

DLL 파일은 Microsoft에 의해 개발되었으며 유형을 나타내는 ".dll" 확장자를 갖습니다. Windows 1.0 서버 및 그 이후 버전의 필수적인 부분이었습니다. 바이너리 파일 형식이며 모든 버전의 Microsoft Windows에서 지원됩니다. 이 파일 형식은 프로그램을 다시 연결할 필요 없이 프로그램 라이브러리에서 개별적이고 독립적인 편집 또는 변경을 허용하기 위해 Windows 프로그램 내에서 공유 라이브러리 시스템을 만드는 수단으로 만들어졌습니다.


## DLL 예제 ##

DLL 진입점에 대한 예제 코드는 아래에서 찾을 수 있습니다.

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## 참조 ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
