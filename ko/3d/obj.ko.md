{
  "date" : "2019-10-11",
  "keywords" :[ "obj 파일", "obj 파일 형식", "obj 파일이란", "파일", "obj 예제", "obj 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ 파일 형식",
  "description":"OBJ 파일 형식과 OBJ 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .OBJ 파일이란?

**OBJ** 파일은 Wavefront의 Advanced Visualizer 응용 프로그램에서 기하학적 개체를 정의하고 저장하는 데 사용됩니다. OBJ 파일을 통해 기하학적 데이터의 앞뒤 전송이 가능합니다. 점, 선, 텍스처 정점, 면 및 자유형 기하학(곡선 및 표면)과 같은 다각형 기하학은 모두 OBJ 형식에서 지원됩니다. 이 형식은 애니메이션이나 조명 및 장면의 위치와 관련된 정보를 지원하지 않습니다.

OBJ 파일은 일반적으로 CAD(Computer Aided Design)로 생성된 3D 모델링 프로세스의 최종 제품입니다. 정점을 저장하는 기본 순서는 면 법선의 명시적 선언을 피하는 시계 반대 방향입니다. OBJ 파일이 주석 줄에 축척 정보를 선언하지만 OBJ 좌표에 대해 단위가 선언되지 않았습니다.

## 3D OBJ 형식의 역사

Wavefront Technologies는 기하학적 개체와 3D 데이터를 저장하기 위해 Advanced Visualizer 응용 프로그램을 위한 OBJ 파일 형식을 만들었습니다. 버전 2.11은 새로 문서화된 버전 3으로 대체되었습니다. 파일 형식은 열려 있으며 3D 그래픽 응용 프로그램을 위해 다른 공급업체에서 구현했습니다. Wavefront Technologies는 이 파일 형식을 오픈 소스로 중립적으로 유지했습니다.

## OBJ 파일 형식

3D 개체에서 표면 형상을 인코딩하는 것은 OBJ 파일 형식이 매우 잘 수행한 어려운 작업입니다. 이 형식은 표면 지오메트리를 인코딩할 수 있는 다양한 선택 사항을 제공하므로 매우 다양합니다. 다음은 고유한 장점과 단점이 있는 허용되는 세 가지 형식입니다.

### 다각형 면을 사용한 테셀레이션

OBJ 파일 형식을 사용하면 사용자가 단순하거나 복잡한 기하학적 모양을 사용하여 3D 모델 표면을 테셀레이션할 수 있습니다. 모델의 표면 지오메트리 인코딩의 경우 파일은 각 다각형에 대한 정점과 법선을 저장합니다. 테셀레이션은 모델의 거칠기를 증가시키지만 파일 크기와 인쇄 품질 사이의 올바른 균형을 찾는 것이 필요합니다.

### 자유형 곡선

OBJ 파일 형식을 사용하면 사용자 정의 자유형 서피스 커브가 모델의 서피스 형상을 지정할 수 있습니다. 자유형 곡선은 수학적 매개변수가 거의 없으므로 자유형 곡선으로 곡선을 가장 잘 정의할 수 있기 때문에 다각형 면보다 더 복잡합니다. 따라서 다각형 테셀레이션에 비해 적은 수의 데이터로 자유 형식 곡선을 사용하여 파일 크기를 확장하지 않고 모든 3D 모델의 고품질 인코딩을 생성합니다.

### 자유형 서피스

OBJ 파일 형식은 또한 자유형 표면 패치를 사용하여 표면 형상의 타일링을 지정합니다. 이러한 종류의 자유형 표면 패치(NURBS)는 트럭의 몸체, 헬리콥터의 날개 또는 보트의 선체와 같이 단단한 반경 치수가 없는 표면에 매우 적합합니다. 자유형 표면을 사용하면 파일 크기를 더 작은 정밀도로 유지하기 위해 더 정확하기 때문에 매우 유리합니다. 이러한 표면은 낮은 정밀도가 허용되지 않는 항공우주 및 자동차 산업의 필수적인 부분입니다.

다음 키워드는 표면 기하학을 정의하기 위해 데이터 유형별로 정렬됩니다.


|요소|자유형 커브/서피스 바디 문|자유형 커브/서피스 속성
---|---|---|
|p|점|parm|매개변수 값|도|도
|l|Line|trim|외부 트리밍 루프|bmat|기저 행렬
|f|페이스|구멍|내부 트리밍 루프|스텝|스텝 사이즈
|curv|커브|scrv|특수 커브|cstype|커브 또는 표면 유형
|curv2|2D 곡선|sp|특수점|**표면의 연결 및 그룹화**
|surf|Surface|end|문 끝|con|connect
|**표시/렌더링 속성**|g|그룹 이름
|베벨|베벨 보간|shadow_obj|그림자 투사|s|스무딩 그룹
|lod|세부 수준|trace_obj|레이 트레이싱|mg|병합 그룹
|d_interp|해산 보간|ctech|곡선 근사 기술|o|객체 이름
|c_interp|색상 보간|stech|표면 근사 기술|
|usemtl|재료 이름|mtllib|재료 라이브러리|
|**기하학적 정점**|
|v|기하학적 정점|vn|정점 법선|
|vt|텍스처 정점|vp|매개변수 공간 정점|

### 색상과 질감

OBJ 파일을 사용하면 색상 및 텍스처 정보를 MTL(Material Template Library)이라는 관련 파일 형식으로 저장할 수 있습니다. 다중 색상 기하학적 모델은 이 두 파일을 함께 사용하여 렌더링합니다. MTL 파일은 ASCII 기반이며 Phong 반사 모델을 사용하여 표면의 빛 반사 속성을 설명하여 컴퓨터 렌더링을 용이하게 합니다. 이 표준은 재료 교환을 위해 활용하는 많은 소프트웨어 공급업체에서 채택했습니다. MTL 형식은 스페큘러 및 시차 맵과 같은 최신 기술을 지원하지 않기 때문에 약간 구식입니다.

## 참고문헌

* [Wavefront .obj 파일](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
