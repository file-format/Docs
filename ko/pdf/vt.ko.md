{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT 파일 형식",
  "description":"PDF/VT 파일 형식과 PDF/VT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/VT란 무엇입니까? #

PDF/VT는 2010년 8월 [ISO 16612-2](https://www.iso.org/standard/46428.html)로 표준으로 발표되었으며, 다양한 형태의 가변 문서 인쇄(VDP)가 가능하도록 설계되었습니다. 환경. 이 표준은 가변 정보 및 트랜잭션 인쇄를 표준의 기초로 합니다. 가변 데이터 인쇄는 내용의 수신자마다 정보의 일부가 다른 경우에 사용됩니다. 거래 인쇄에는 청구 정보와 마케팅 정보를 결합한 송장, 명세서 및 기타 문서가 포함됩니다. 그 결과 이미지, 텍스트 및 기타 콘텐츠 유형의 처리가 개선되었습니다. PDF/VT를 사용하면 DPM(문서 부분 메타데이터) 개념을 사용하여 HVTO(고용량 트랜잭션 출력) 인쇄 데이터에 대한 페이지를 안정적이고 동적으로 관리할 수 있습니다. PDF/VT 파일은 다른 구성 요소를 추가할 필요 없이 Adobe Acrobat 뷰어에서 열 수 있습니다.

## 문서 부분 계층 ##

문서 부분(DPart) 계층 구조는 문서의 모든 페이지를 기반으로 하는 문서 부분 노드의 트리 구조와 같습니다. 이 트리의 요소를 DPart 노드라고 합니다. 각 내부 노드는 다른 DPart 노드를 포함하고 각 리프 노드는 수신자에 대해 하나 이상의 페이지를 지정합니다. 기본적으로 DPart 계층은 PDF/VT 파일에 있는 문서 또는 문서 부분의 순서와 관계를 지정합니다. DPart 노드의 트리 구조는 여러 수신자에 대한 하위 문서를 포함할 수 있고 각 문서 부분이 단일 수신자에 대한 페이지에 해당할 수 있으므로 PDF/VT 문서의 내부 내용을 쉽게 나타냅니다. PDF/VT 파일에는 DPart 계층이 필요합니다.

## 문서 부분 메타데이터(DPM) ##

DPM(문서 부분 메타데이터)은 문서 부분 계층 구조의 각 노드와 연결되며 특정 수신자의 하위 문서 및 해당 부분에 대한 정보를 전달하는 데 사용할 수 있습니다. 특히 DPM은 속성에 대한 정보나 받는 사람에 대한 정보를 인코딩된 형식으로 포함할 수 있습니다.

## 적합성 수준 ##

PDF/VT는 다음 세 가지 적합성 수준에 따라 수여됩니다. 모두 [PDF](/ko/pdf/) 1.6 기준입니다.

* `PDF/VT-1` - PDF/X-4를 기반으로 하며 PDF 문서를 렌더링하는 데 필요한 모든 리소스를 포함합니다.
* `PDF/VT-2` - 다중 파일 교환을 위해 설계된 PDF/VT-2 문서는 외부 출력 의도, 외부 콘텐츠 또는 둘 다를 참조할 수 있습니다. PDF/VT 문서와 참조된 모든 PDF 파일 및 외부 출력 의도를 총괄적으로 PDF/VT-2 파일 세트라고 합니다. Acrobat 9 및 이 기능을 지원합니다.
* `PDF/VT-2s` - PDF/VT-2 라이브 스트리밍을 지원합니다. 이를 통해 데이터의 분할된 섹션을 처리할 수 있습니다.

## 참조 ##

* [PDF/VT - 위키피디아 작성](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 그래픽 기술](https://www.iso.org/standard/46428.html)
