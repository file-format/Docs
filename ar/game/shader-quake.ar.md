{
"التاريخ": "2023-10-11",
   "keywords":[
"التظليل",
"ملف التظليل",
"شادر زلزال 3 ملف تظليل المحرك",
"كيفية فتح ملف تظليل",
"ملف",
"امتداد ملف التظليل",
"امتداد",
"ملف"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"العنوان": "تنسيق ملف SHADER - ملف تظليل المحرك Quake 3",
   "description":"تعرف على تنسيق ملف SHADER Quake 3 Engine Shader وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SHADER وفتحها.",
"linktitle": "شادر زلزال",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
"parent": "لعبة"
}
},
"lastmod": "2023-10-11"
}

## ما هو ملف شادر؟

يتم استخدام تنسيق ملف SHADER في محرك **Quake 3** لتحديد التظليل للأنسجة والمواد الموجودة في اللعبة. يتم استخدام التظليل لتحديد كيفية عرض السطح, بما في ذلك مظهره وانعكاسه وشفافيته وخصائصه البصرية الأخرى.

## زلزال 3 ملف تظليل المحرك

فيما يلي نظرة عامة أساسية على هيكل وبناء جملة ملف تظليل المحرك Quake 3:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

في ملف تظليل محرك Quake 3, يمكنك تحديد تظليلات متعددة, لكل منها مجموعة الخصائص والمراحل الخاصة به. تُستخدم هذه التظليلات لتحديد مظهر الأنسجة والمواد المختلفة في عالم اللعبة. يستخدم المحرك هذه المعلومات لعرض الأسطح بتأثيرات وسلوكيات مرئية محددة.

ملفات Shader في محرك Quake 3 هي ملفات نصية بسيطة تحتوي على تعليمات حول كيفية ظهور القوام والمواد في اللعبة. يمكن فتح هذه الملفات وتحريرها باستخدام محرر نصوص عادي, وعادةً ما توجد في دليل **"/scripts"** ضمن حزمة .PK3 الخاصة باللعبة.

## محرك الزلزال 3

يعد محرك Quake 3 محرك ألعاب مؤثرًا للغاية ومتعدد الاستخدامات تم تطويره بواسطة id Software. تم تقديمها لأول مرة مع إصدار لعبة "Quake III Arena" في عام 1999 ومنذ ذلك الحين تم استخدامها في العديد من الألعاب الأخرى. المحرك معروف برسوماته المتقدمة وقدراته على تعدد اللاعبين وقابليته للتعديل.

فيما يلي بعض الميزات والجوانب الرئيسية لمحرك Quake 3:

1. ** محرك الرسومات: ** اشتهر محرك Quake 3 بتكنولوجيا الرسومات المتطورة في ذلك الوقت. لقد قدمت ميزات متقدمة مثل الأسطح المنحنية والتظليل والإضاءة الديناميكية, والتي كانت رائدة في أواخر التسعينيات.
    





2. ** التركيز على اللعب الجماعي: ** تم تصميم Quake 3 Arena في المقام الأول لتكون لعبة إطلاق نار متعددة اللاعبين من منظور الشخص الأول. كان رمز الشبكة الخاص بالمحرك ودعم الألعاب متعددة اللاعبين عبر الإنترنت استثنائيين, مما جعله خيارًا شائعًا للعب التنافسي عبر الإنترنت.
    





3. **قابلية التعديل:** محرك Quake 3 معروف بقابليته للتعديل. أصدرت شركة id Software كود مصدر المحرك بموجب ترخيص GNU العام المفتوح المصدر (GPL). وقد شجع هذا على إنشاء العديد من التعديلات والخرائط المخصصة, مما أدى إلى مجتمع تعديل نابض بالحياة.
    





4. ** أسلوب اللعب المكتوب: ** يستخدم المحرك نظامًا قائمًا على البرنامج النصي لتحديد قواعد اللعبة وسلوكها, مما يجعل من السهل نسبيًا على المعدلين ومصممي الخرائط إنشاء أوضاع لعب مخصصة وتجارب فريدة.
    





5. ** دعم المحتوى المخصص: ** يدعم محرك Quake 3 المحتوى المخصص, بما في ذلك الأنسجة والنماذج وملفات الصوت, مما يسمح بدرجة عالية من التخصيص في الخرائط والتعديلات التي أنشأها المستخدم.
    





6. **تصميم المستوى:** استخدم المحرك نظام تصميم المستوى القائم على الفرشاة, حيث تم إنشاء الخرائط عن طريق اقتطاع مسافات من الفرش الصلبة. كان هذا النهج موثقًا جيدًا وسهل الاستخدام لمصممي المستويات.


على مر السنين, تم استخدام محرك Quake 3 كأساس للعديد من الألعاب والتعديلات الأخرى, بما في ذلك "Return to Castle Wolfenstein" و"Star Wars Jedi Knight II: Jedi Outcast" و"Urban Terror" وغيرها. لقد تركت إرثًا دائمًا في عالم تطوير الألعاب وساعدت في تشكيل نوع ألعاب إطلاق النار من منظور الشخص الأول. في حين ظهرت محركات أحدث وأكثر تقدمًا منذ ذلك الحين, لا يزال محرك Quake 3 يحظى بالاحترام لمساهمته في صناعة الألعاب.

## كيفية فتح ملف شادر؟

تتضمن البرامج التي تفتح ملفات SHADER أو تشير إليها

- **id Software Quake 3** (مدفوع) لأنظمة (Windows وMac وLinux)
- مايكروسوفت المفكرة
- المفكرة ++
- أي محرر نصوص

## ملفات SHADER أخرى

فيما يلي أنواع الملفات الأخرى التي تستخدم امتداد الملف **.shader**.

** ملفات اللعبة **
- [SHADER - ملف تظليل محرك Godot](/ar/game/shader-godot/)
- [SHADER - ملف تظليل محرك Quake 3](/ar/game/shader-quake/)
- [SHADER - أصول تظليل الوحدة](/ar/game/shader-unity/)

## مراجع
- [معرف التقنية 3](https://en.wikipedia.org/wiki/Id_Tech_3)

