{
  "date" : "2019-10-11",
  "keywords" :[ "tệp dae", "định dạng tệp dae", "tệp dae là gì", "tệp", "ví dụ dae", "phần mở rộng tệp dae","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp DAE và các API có thể mở và tạo tệp DAE.",
  "title" :"DAE - Định dạng tệp trao đổi tài sản kỹ thuật số",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DAE là gì?

Tệp DAE là định dạng tệp Trao đổi tài sản kỹ thuật số được sử dụng để trao đổi dữ liệu giữa các ứng dụng 3D tương tác. Định dạng tệp này dựa trên lược đồ XML COLLADA (COLLAborative Design Activity) là một lược đồ XML tiêu chuẩn mở để trao đổi tài sản kỹ thuật số giữa các ứng dụng phần mềm đồ họa. Nó đã được ISO chấp nhận dưới dạng thông số kỹ thuật có sẵn công khai, ISO/pAS 17506. Các tệp DAE có thể được mở trong các ứng dụng như Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD và các API như [Aspose.CAD](https://products.aspose.com/cad/).

## Định dạng tệp DAE

Định dạng tệp DAE dựa trên [lược đồ COLLADA XML](https://www.khronos.org/files/collada_spec_1_5.pdf) trong đó tất cả các thành phần được định nghĩa là các thẻ XML. Nó cho phép liên kết các công cụ xử lý 3D và DCC đa dạng vào một quy trình sản xuất nội dung 3D. Nó có khả năng mã hóa toàn diện các cảnh trực quan bao gồm hình học, hoạt ảnh, trình đổ bóng và vật lý. Định dạng mở, cấp độ lưu trữ và giữ lại thông tin meta.

### Thẻ COLLADA

Thẻ lược đồ COLLADA như hình bên dưới.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Thẻ nội dung

Thẻ nội dung mô tả tác giả và môi trường của tệp

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Thư viện máy ảnh

Tài sản COLLADA được chứa bên trong thư viện. Không có gì ngạc nhiên khi thư viện máy ảnh chứa các máy ảnh. Máy ảnh phổ biến là phối cảnh hoặc chính tả. Thẻ thư viện máy ảnh được định nghĩa như sau.
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
### Đèn

Đèn phổ biến là điểm, điểm hoặc hướng
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

### Trường hợp tài liệu

Các hiệu ứng đối tượng Vật liệu được định nghĩa như sau.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Hiệu ứng chung

Các hiệu ứng phổ biến hoạt động giống như trạng thái OpenGL 1 và có thể được định nghĩa như sau.

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

### Thuộc tính hình học

Hình học mô tả các thuộc tính OpenGL và được định nghĩa như sau.
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

### Cảnh trực quan

Các cảnh trực quan giống như các cảnh thống nhất và chứa một hệ thống phân cấp các nút như sau.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Người giới thiệu
* [Thông số kỹ thuật COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

