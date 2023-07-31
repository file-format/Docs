{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "파일", "확장자", "파일 형식", "Microsoft Excel 매크로 파일", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLM 파일을 만들고 열 수 있는 XLM 매크로 파일 및 API가 무엇인지 알 수 있는 파일 형식 가이드",
  "title" :"XLM 파일이란?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLM 파일이란?

Excel 매크로용 XLM은 매크로를 저장하는 데 사용되는 스프레드시트 파일 유형입니다. 응용 프로그램의 관점에서 매크로는 프로세스 자동화에 사용되는 일련의 지침입니다. 매크로는 [XLS](/ko/spreadsheet/xls/) 파일 형식에 대해 반복적으로 수행되는 단계를 기록하는 데 사용되며 매크로를 다시 실행하여 작업 수행을 용이하게 합니다. 매크로는 Visual Basic Editor를 사용하여 Excel 통합 문서 내에서 Microsoft의 VBA(Visual Basic for Applications)로 프로그래밍되며 여기에서 직접 실행/디버그할 수 있습니다.

## 간략한 역사 ##

Microsoft Excel은 첫 공개 출시 이후 매크로 프로그래밍을 지원했습니다. 매크로의 기능은 새로운 기능에 따라 확장된 Excel의 후속 버전을 통해 동일하게 유지되었습니다. XLM은 Excel 4.0부터 Excel의 기본 매크로 언어였습니다. Excel 5.0은 기본적으로 VBA에 매크로를 기록했지만 버전 5.0에서는 XLM 기록이 여전히 옵션으로 허용되었습니다. 버전 5.0 이후에는 해당 옵션이 중단되었습니다. Excel 2010을 포함한 모든 Excel 버전은 XLM 매크로를 실행할 수 있지만 Microsoft에서는 사용을 권장하지 않습니다.

## XLM에서 매크로 기록 ##

Excel은 매크로 기록을 위한 사용하기 쉬운 단계를 제공합니다. 매크로를 사용하려면 개발자 도구가 설치되어 있어야 합니다. 매크로 기록이 진행 중이면 나중에 재생할 각 사용자 동작을 기록합니다. 매크로 기록에는 실제로 기록이 시작된 후 사용자가 수행하는 모든 단계가 포함됩니다. 따라서 매크로 기록이 시작된 후 셀의 내용을 굵게, 기울임꼴로 만들고 텍스트 정렬을 설정하면 이러한 모든 명령이 기록됩니다. 기록된 각 매크로는 나중에 빠르게 재생할 수 있도록 바로 가기를 할당할 수도 있습니다. 매크로 기록은 VBE(Visual Basic Editor)를 사용하여 편집할 수 있는 매크로 형식의 VBA 코드를 생성합니다.

## 엑셀 개체 모델 ##

매크로는 뒤에 VBA 루틴을 사용하고 이를 위해 [Excel 개체 모델](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model)을 따릅니다. 이 모델은 사용자 정의 명령 도구 모음, 명령 모음 또는 메시지 상자를 통해 스프레드시트와 상호 작용할 수 있도록 스프레드시트의 개체를 식별합니다. 예를 들어 통합 문서의 속성에 대한 액세스 권한은 Workbook 개체를 통해 부여됩니다. 마찬가지로, 모델에는 통합 문서의 워크시트를 프로그래밍 방식으로 작업할 수 있는 Worksheet 개체가 있습니다.

## 매크로 및 보안 ##

VBA를 사용하면 모든 응용 프로그램 영역과 파일 시스템에 액세스할 수 있으며 위험할 수도 있습니다. 이것은 자신의 끝에서 파일을 실행할 수 있는 사람과 통합 문서를 공유할 때 문제를 야기합니다. 그것은 Microsoft Excel이 그러한 파일을 열 때 경고한다는 것입니다. 매크로는 다른 사용자가 신뢰할 수 있는지 확인하기 위해 디지털 서명으로 인증될 수 있습니다. 따라서 매크로는 소스를 확인한 후에 활성화할 수 있습니다.

## 참조 ##

* [[MS-XLS] - 엑셀 바이너리 파일 형식 구조](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [매크로 프로그래밍](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

