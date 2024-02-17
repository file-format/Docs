{
  "date" : "2019-10-11",
  "keywords" : [ "x3d file", "x3d file format", "what is an x3d file", "file", "x3d example", "x3d file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "X3D - 3D চিত্র ফাইল",
  "description":"X3D ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা X3D ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## একটি X3D ফাইল কি?
X3D is an [XML](/web/xml/) based 3D graphics file format for presentation of 3D information. It is a modular standard and is defined through several ISO specifications. The format supports vector and raster graphics, transparency, lighting effects, and animation settings including rotations, fades, and swings. It became successor of [VRML](/3d/vrml/) file format in 2001. X3D-তে রঙের তথ্য এনকোড করার সুবিধা রয়েছে ([STL](/cad/stl/) এর বিপরীতে) যা একটি রঙিন 3D প্রিন্টারে মডেলটি প্রিন্ট করার সময় ব্যবহৃত হয়। বিন্যাসে VRML-এর এক্সটেনশনগুলি রয়েছে, XML সিনট্যাক্সের পাশাপাশি VRML97 বা বাইনারি বিন্যাসের ওপেন ইনভেনটর-সদৃশ সিনট্যাক্স ব্যবহার করে দৃশ্যটিকে এনকোড করার ক্ষমতা প্রদান করে।

The abstract specification for X3D (ISO/IEC 19775) was first approved by the ISO in 2004. X3D (ISO/IEC 19776) এর জন্য XML এবং ClassicVRML এনকোডিংগুলি 2005 সালে প্রথম অনুমোদিত হয়েছিল।

## X3D ফাইল ফরম্যাট

X3D দৃশ্য ফাইলগুলির একটি সাধারণ ফাইল কাঠামো রয়েছে:

* ফাইল হেডার (হয় এক্সএমএল, ক্লাসিকভিআরএমএল, বা সংকুচিত বাইনারি)

* সংস্করণ এবং প্রোফাইল বৈশিষ্ট্য সহ X3D রুট নোডের শুরু

* উপাদান এবং মেটা বিবৃতি সহ একটি প্রধান বিভাগ (উভয় ঐচ্ছিক)

* X3D দৃশ্য গ্রাফ এবং এর চাইল্ড নোড

* X3D রুট নোডের শেষ


## X3D ফাইল ফরম্যাটের উদাহরণ

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'-bn/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## তথ্যসূত্র ##

* [X3D - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/X3D)

* [ওয়েব3ডি কনসোর্টিয়ামের অফিসিয়াল ওয়েবসাইট](https://www.web3d.org/)

* [X3D অফিসিয়াল ওয়েবসাইট](https://www.web3d.org/x3d/what-x3d)


