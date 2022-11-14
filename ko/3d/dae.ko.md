{
  "date" : "2019-10-11",
  "keywords" :[ "대 파일", "대 파일 형식", "대 파일이란", "파일", "대 예제", "대 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"DAE 파일 형식과 DAE 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "title" :"DAE - 디지털 자산 교환 파일 형식",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .DAE 파일이란?

DAE 파일은 대화형 3D 응용 프로그램 간에 데이터를 교환하는 데 사용되는 디지털 자산 교환 파일 형식입니다. 이 파일 형식은 그래픽 소프트웨어 응용 프로그램 간의 디지털 자산 교환을 위한 개방형 표준 XML 스키마인 COLLADA(COLLAborative Design Activity) XML 스키마를 기반으로 합니다. ISO에서 공개 사양인 ISO/pAS 17506으로 채택했습니다. DAE 파일은 Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD와 같은 응용 프로그램 및 [Aspose.CAD](https://products)와 같은 API에서 열 수 있습니다. .aspose.com/cad).

## DAE 파일 형식

DAE 파일 형식은 모든 요소가 XML 태그로 정의되는 [COLLADA XML 스키마](https://www.khronos.org/files/collada_spec_1_5.pdf)를 기반으로 합니다. 다양한 DCC 및 3D 처리 도구를 3D 자산용 프로덕션 파이프라인에 바인딩할 수 있습니다. 지오메트리, 애니메이션, 셰이더 및 물리학을 포함한 시각적 장면의 포괄적인 인코딩이 있습니다. 형식은 개방적이고 아카이브 등급이며 메타 정보를 유지합니다.

### 콜라다 태그

COLLADA 스키마 태그는 다음과 같습니다.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### 자산 태그

자산 태그는 파일의 작성자와 환경을 설명합니다.

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### 카메라 라이브러리

COLLADA 자산은 라이브러리 내에 포함되어 있습니다. 카메라 라이브러리에는 당연히 카메라가 포함되어 있습니다. 일반적인 카메라는 원근 또는 직교입니다. 카메라 라이브러리 태그는 다음과 같이 정의됩니다.
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### 불

일반적인 조명은 포인트, 스팟 또는 방향성입니다.
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### 머티리얼 인스턴스

Materials 인스턴스 효과는 다음과 같이 정의됩니다.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### 공통 효과

공통 효과는 OpenGL 1 상태처럼 작동하며 다음과 같이 정의할 수 있습니다.

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### 지오메트리 속성

기하학은 OpenGL 속성을 설명하고 다음과 같이 정의됩니다.
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### 시각적 장면

시각적 장면은 단일 장면과 같으며 다음과 같은 노드 계층 구조를 포함합니다.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## 참고문헌
* [COLLADA 1.5.0 사양](https://www.khronos.org/files/collada_spec_1_5.pdf)

