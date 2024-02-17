{
  "date" : "2019-10-11",
  "keywords" : [ "kml file", "what is an kml file", "file", "kml example", "kml file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "KML - কীহোল মার্কআপ ভাষা",
  "description":"KML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা KML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## একটি KML ফাইল কি?

KML, Keyhole Markup Language) XML স্বরলিপিতে ভূ-স্থানিক তথ্য ধারণ করে। KML হিসাবে সংরক্ষিত ফাইলগুলি জিওগ্রাফিক ইনফরমেশন সিস্টেম (GIS) অ্যাপ্লিকেশনগুলিতে খোলা যেতে পারে যদি তারা এটি সমর্থন করে। আন্তর্জাতিক মান হিসেবে গৃহীত হওয়ার পর অনেক অ্যাপ্লিকেশন KML ফাইল ফরম্যাটের জন্য সমর্থন প্রদান করা শুরু করেছে। KML নেস্টেড উপাদান এবং বৈশিষ্ট্য সহ একটি ট্যাগ-ভিত্তিক কাঠামো ব্যবহার করে। সমস্ত ট্যাগ কেস-সংবেদনশীল এবং এই ট্যাগের ক্রম, [KML](https://developers.google.com/kml/documentation/kmlreference) রেফারেন্স অনুযায়ী, অনুসরণ করা গুরুত্বপূর্ণ৷

## সংক্ষিপ্ত ইতিহাস ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. যেহেতু বিন্যাসটি Google আর্থের সাথে ব্যবহারের জন্য তৈরি করা হয়েছিল, তাই এটিই প্রথম KML ফাইলগুলি দেখতে এবং সম্পাদনা করার জন্য বিশিষ্ট। সময়ের সাথে সাথে, এখন আরও অনেক প্রকল্প রয়েছে যা বিভিন্ন ভাষায় বেশ কয়েকটি API সহ KML ফাইল ফর্ম্যাটের জন্য সমর্থন প্রদান করে।

## KML ফাইল ফরম্যাট স্পেসিফিকেশন ##

KML রেফারেন্স সম্পূর্ণ ফাইল ফরম্যাট স্পেসিফিকেশন থাকার জন্য উল্লেখ করার জন্য একটি সম্পূর্ণ গাইড। একটি আদর্শ KML ফাইলের মধ্যে রয়েছে:

* স্থান চিহ্ন

* প্লেসমার্কে বর্ণনামূলক HTML

* গ্রাউন্ড ওভারলে

* পথ

* বহুভুজ


এগুলি ছাড়াও, KML ফাইলের একটি উন্নত সংস্করণ থাকতে পারে:

* জ্যামিতির জন্য শৈলী

* হাইলাইট করা আইকনগুলির জন্য শৈলী

* স্ক্রিন ওভারলে

* নেটওয়ার্ক লিঙ্ক


KML উপাদানগুলির প্রতিটিতে ল্যাট-লং তথ্য রয়েছে যা ফাইলে উপস্থিত তথ্যকে জিও-লোকেট করে। যাইহোক, শিরোনাম, উচ্চতা এবং কাত মত অতিরিক্ত পরামিতি থাকতে পারে।

### স্থানচিহ্ন ###

এটি পৃথিবীর পৃষ্ঠে একটি অবস্থান উপস্থাপন করতে ব্যবহৃত হয় এবং এটি দ্বারা চিহ্নিত করা হয়<Point> উপাদান নিচে একটি উদাহরণ দেওয়া হল কিভাবে একটি প্লেসমার্ক কেএমএল ফাইলে উপস্থাপন করা হয়।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### প্লেসমার্কে বর্ণনামূলক HTML ###

অতিরিক্ত তথ্য একটি স্থানচিহ্নের সাথে যুক্ত হতে পারে যা স্থান চিহ্নের উপস্থাপনাকে আরও উন্নত করে। এই ধরনের তথ্যের মধ্যে রয়েছে লিঙ্ক, ফন্টের আকার, শৈলী এবং রং। উপরন্তু, এটি স্থানচিহ্নের অংশ হতে পাঠ্য সারিবদ্ধকরণ এবং টেবিল অন্তর্ভুক্ত করে।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### গ্রাউন্ড ওভারলে ###

এগুলি পৃথিবীর পৃষ্ঠে একটি চিত্রের স্তরবিন্যাসকে প্রতিনিধিত্ব করে। দ্য<icon> এলিমেন্টে ওভারলে ইমেজ ফাইলের লিঙ্ক রয়েছে।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### পথ ###

পাথ দ্বারা প্রতিনিধিত্ব করা হয়<LineString> উপাদান যা ল্যাট-লং জোড়ার সংগ্রহ। এগুলো ব্যবহার করে গুগল আর্থ-এ অনেক রকমের পাথ তৈরি করা যায়।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML ফাইলে স্থানিক রেফারেন্সিং ##

ভূ-অবস্থান সম্পর্কে যেকোন ভূ-স্থানিক ফাইলে থাকা তথ্য স্থানিক রেফারেন্সিং তথ্য ছাড়াই ভিন্ন অর্থ হতে পারে। ডিফল্টরূপে, KML ফাইলের স্থানিক রেফারেন্সিং ওয়ার্ল্ড জিওডেটিক সিস্টেম অফ 1984, WGS84 দ্বারা সংজ্ঞায়িত করা হয়েছে।

## তথ্যসূত্র ##

* [KML রেফারেন্স](https://developers.google.com/kml/documentation/kmlreference)

* [KML এর জন্য Google ডেভেলপার টিউটোরিয়াল](https://developers.google.com/kml/documentation/kml_tut)

* [KML ফাইল ফরম্যাট](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


