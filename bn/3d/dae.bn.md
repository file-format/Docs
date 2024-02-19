{
  "date": "2019-10-11",
  "keywords": [
    "dae file",
    "dae file format",
    "what is an dae file",
    "file",
    "dae example",
    "dae file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "DAE ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা DAE ফাইল খুলতে এবং তৈরি করতে পারে।",
  "title": "DAE - ডিজিটাল সম্পদ বিনিময় ফাইল বিন্যাস",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-dae-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি DAE ফাইল কি?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE ফাইলগুলি Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, এবং API যেমন [Aspose.CAD](https://products.aspose.com/cad/)-এর মতো অ্যাপ্লিকেশনগুলিতে খোলা যেতে পারে৷

## DAE ফাইল ফরম্যাট

DAE ফাইলের বিন্যাসটি [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf) এর উপর ভিত্তি করে যেখানে সমস্ত উপাদানগুলিকে XML ট্যাগ হিসাবে সংজ্ঞায়িত করা হয়েছে৷ এটি 3D সম্পদের জন্য একটি উত্পাদন পাইপলাইনে বিভিন্ন DCC এবং 3D প্রক্রিয়াকরণ সরঞ্জামের বাঁধাই সক্ষম করে। এতে জ্যামিতি, অ্যানিমেশন, শেডার এবং পদার্থবিদ্যা সহ চাক্ষুষ দৃশ্যগুলির ব্যাপক এনকোডিং রয়েছে। বিন্যাসটি খোলা, সংরক্ষণাগার-গ্রেড এবং মেটা তথ্য ধরে রাখে।

### কোলাডা ট্যাগ

COLLADA স্কিমা ট্যাগটি নীচে দেখানো হয়েছে।
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### সম্পদ ট্যাগ

সম্পদ ট্যাগ ফাইলের লেখক এবং পরিবেশ বর্ণনা করে

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### ক্যামেরা লাইব্রেরি

COLLADA সম্পদ লাইব্রেরির ভিতরে থাকে। ক্যামেরা লাইব্রেরিতে আশ্চর্যজনকভাবে ক্যামেরা রয়েছে। সাধারণ ক্যামেরাগুলি দৃষ্টিকোণ বা অর্থোগ্রাফিক। ক্যামেরা লাইব্রেরি ট্যাগ অনুসরণ হিসাবে সংজ্ঞায়িত করা হয়.
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
### আলো

সাধারণ আলো বিন্দু, স্পট বা দিকনির্দেশক
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

### উপাদানের উদাহরণ

উপকরণ উদাহরণ প্রভাব অনুসরণ হিসাবে সংজ্ঞায়িত করা হয়.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### সাধারণ প্রভাব

সাধারণ প্রভাবগুলি OpenGL 1 স্টেটের মতো কাজ করে এবং অনুসরণ হিসাবে সংজ্ঞায়িত করা যেতে পারে।

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

### জ্যামিতি বৈশিষ্ট্য

জ্যামিতি OpenGL বৈশিষ্ট্য বর্ণনা করে এবং অনুসরণ হিসাবে সংজ্ঞায়িত করে।
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

### চাক্ষুষ দৃশ্য

ভিজ্যুয়াল দৃশ্যগুলি একতা দৃশ্যের মতো এবং অনুসরণ করে নোডগুলির একটি শ্রেণিবিন্যাস ধারণ করে।
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## তথ্যসূত্র
 * [কোলাডা 1.5.0 স্পেসিফিকেশন](https://www.khronos.org/files/collada_spec_1_5.pdf)

