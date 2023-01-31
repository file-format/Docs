{
  "date" : "2019-10-11",
  "keywords" :["ملف obj" , "تنسيق ملف obj" , "ما هو ملف obj" , "ملف" , "مثال obj" , "ملحق ملف obj" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف OBJ" ,
  "description":"تعرف على تنسيق ملف OBJ وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات OBJ." ,
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف OBJ؟

يتم استخدام ملفات ** OBJ ** بواسطة تطبيق Advanced Visualizer في Wavefront لتعريف الكائنات الهندسية وتخزينها. أصبح النقل الخلفي والأمامي للبيانات الهندسية ممكنًا من خلال ملفات OBJ. يتم دعم كل من الهندسة متعددة الأضلاع مثل النقاط والخطوط ورؤوس النسيج والوجوه والشكل الهندسي الحر (المنحنيات والأسطح) بواسطة تنسيق OBJ. لا يدعم هذا التنسيق الرسوم المتحركة أو المعلومات المتعلقة بالضوء وموضع المشاهد.

عادةً ما يكون ملف OBJ منتجًا نهائيًا لعملية النمذجة ثلاثية الأبعاد التي تم إنشاؤها بواسطة CAD (التصميم بمساعدة الكمبيوتر). الترتيب الافتراضي لتخزين القمم هو عكس اتجاه عقارب الساعة لتجنب الإعلان الصريح لقواعد الوجه. على الرغم من أن ملفات OBJ تعلن عن معلومات المقياس في سطر التعليق ، إلا أنه لم يتم الإعلان عن أي وحدات لإحداثيات OBJ.

## تاريخ تنسيق 3D OBJ

أنشأت Wavefront Technologies تنسيق ملف OBJ لتطبيقها المتقدم Visualizer لتخزين الكائنات الهندسية والبيانات ثلاثية الأبعاد. تم استبدال الإصدار 2.11 بإصدار موثق حديثًا 3. تنسيق الملف مفتوح وتم تنفيذه بواسطة بائعين آخرين لتطبيق الرسومات ثلاثية الأبعاد الخاص بهم. حافظت Wavefront Technologies على تنسيق الملف هذا مفتوح المصدر وحياديًا.

## تنسيق ملف OBJ

في الكائنات ثلاثية الأبعاد ، يعد ترميز هندسة السطح مهمة صعبة أنجزها تنسيق ملف OBJ جيدًا. هذا التنسيق متعدد الاستخدامات لأنه يوفر عددًا من الخيارات لتشفير هندسة السطح. فيما يلي ثلاثة تنسيقات مسموح بها لها مزاياها وعيوبها:

### تغطية بالفسيفساء ذات وجوه متعددة الأضلاع

يسهل تنسيق ملف OBJ المستخدم على فسيفساء سطح نموذج ثلاثي الأبعاد باستخدام أشكال هندسية بسيطة أو معقدة. لتشفير هندسة السطح لنموذج ما ، يخزن الملف الرؤوس والعادي لكل مضلع. على الرغم من أن التغطية بالفسيفساء تزيد من خشونة النموذج ، إلا أنه من الضروري اكتشاف التوازن الصحيح بين حجم الملف وجودة طباعته.

منحنى الشكل الحر

يسمح تنسيق ملف OBJ لمنحنيات السطح ذات الشكل الحر التي يحددها المستخدم بتحديد هندسة السطح لنموذج ما. نظرًا لأن المنحنيات ذات الشكل الحر أكثر تعقيدًا من الوجوه المضلعة ، حيث يمكن تحديد الخطوط المنحنية بشكل أفضل من خلال منحنيات الشكل الحر ، مع القليل من المعلمات الرياضية. لذلك ، مع وجود بيانات أقل مقارنةً بالفسيفساء متعددة الأضلاع ، تُستخدم المنحنيات ذات الشكل الحر لإنشاء ترميز عالي الجودة لأي نموذج ثلاثي الأبعاد دون توسيع حجم الملف.

### الأسطح ذات الشكل الحر

يحدد تنسيق ملف OBJ أيضًا تبليط هندسة السطح باستخدام تصحيحات السطح ذات الشكل الحر. هذا النوع من البقع السطحية ذات الشكل الحر (NURBS) مناسب جدًا للأسطح التي لا تحتوي على أبعاد شعاعية صلبة مثل جسم الشاحنة أو أجنحة المروحية أو بدن القارب. يعد استخدام الأسطح ذات الشكل الحر مفيدًا للغاية لأنها أكثر دقة للحفاظ على أحجام الملفات أصغر بدقة أعلى. هذه الأسطح جزء أساسي من صناعة الطيران والسيارات حيث الدقة المنخفضة لا ترحم.

الكلمات الأساسية التالية مرتبة حسب نوع البيانات لتحديد هندسة السطح.


| العناصر | منحنى حر الشكل / بيانات جسم السطح | سمات منحنى / سطح حر الشكل
---|---|---|
| p | Point | parm | قيم المعلمة | درجة | الدرجة
| l | الخط | تقليم | حلقة التشذيب الخارجية | bmat | مصفوفة الأساس
| و | الوجه | الثقب | حلقة التشذيب الداخلية | الخطوة | حجم الخطوة
| curv | Curve | scrv | منحنى خاص | cstype | نوع منحنى أو سطح
| curv2 | منحنى ثنائي الأبعاد | sp | نقطة خاصة | ** التوصيل وتجميع الأسطح **
| تصفح | السطح | النهاية | بيان النهاية | يخدع | الاتصال
| ** سمات العرض / العرض ** | g | اسم المجموعة
| bevel | Bevel interpolation | shadow_obj | Shadow casting | s | مجموعة التنعيم
| لودج | مستوى التفاصيل | trace_obj | تتبع الشعاع | mg | مجموعة الدمج
| d_interp | حل الاستيفاء | ctech | تقنية تقريب المنحنى | o | اسم الكائن
| c_interp | الاستيفاء اللوني | stech | تقنية تقريب السطح |
| usemtl | اسم المادة | مطليب | مكتبة المواد |
| ** القمم الهندسية ** |
| v | رؤوس هندسية | vn | معايير الرأس |
| vt | رؤوس الملمس | vp | قيم مساحة المعلمة |

### اللون والقوام

يسمح ملف OBJ بتخزين معلومات اللون والملمس في تنسيق ملف مرتبط يسمى مكتبة قوالب المواد (MTL). يتم عرض النماذج الهندسية متعددة الألوان باستخدام هذين الملفين معًا. تستند ملفات MTL إلى ASCII وتسهل في عرض الكمبيوتر من خلال وصف خصائص انعكاس الضوء للسطح باستخدام نموذج انعكاس Phong. تم اعتماد المعيار من قبل عدد كبير من بائعي البرامج الذين يستغلون ميزته في تبادل المواد. يعد تنسيق MTL قديمًا إلى حد ما نظرًا لعدم وجود دعم في أحدث التقنيات مثل الخرائط المرآوية والمنظر.

## مراجع

* [ملف Wavefront .obj] (https://en.wikipedia.org/wiki/Wavefront_.obj_file)
