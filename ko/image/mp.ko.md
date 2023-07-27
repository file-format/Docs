{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP 파일 - LaTeX 메타포스트 파일",
  "description":"MP 파일 형식과 MP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## .MP 파일이란?

MP 파일은 MetaPost 프로그래밍 언어에서 그림을 만들기 위해 생성한 벡터 이미지 파일입니다. MP 파일 형식으로 생성된 벡터 이미지는 [EPS](/ko/page-description-language/eps/)(Encapsulated PostScript) 파일로 저장됩니다. 또한 MetaPost는 TeX 및 Metafont 프레임워크와 함께 배포되며 이러한 응용 프로그램에서 사용하는 TEX 및 LTX 파일 내에서 MP 파일을 생성할 수 있습니다. MP 파일에는 출력 EPS 파일을 렌더링하기 위한 도면 문과 수학 알고리즘 도면이 포함되어 있습니다. PDFTex 엔진은 생성된 EPS를 사용하여 [PDF](/ko/pdf/) 파일을 직접 생성할 수 있습니다.

## MP 파일 형식

MP 파일은 바이너리 파일로 디스크에 저장되며 출력 벡터 이미지 파일 형식으로 내보낼 때 EPS 출력을 생성합니다. MetaPost를 사용하여 작성한 도면은 LaTex로 작성한 기술 문서 및 저널 출판물에 형식화된 형태로 포함됩니다.

### 메타포스트 MP 파일 예

다음은 [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)에서 참조한 예제로, 화살표와 중간 바로 위에 문자 "A"가 포함되어 있습니다. 화살.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## 참조 ##

* [위키피디아의 메타포스트](https://en.wikipedia.org/wiki/MetaPost)
* [Berkeley Educational Wiki의 라텍스 샘플 Metapost](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

