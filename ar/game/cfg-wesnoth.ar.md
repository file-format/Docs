{
  "date": "2023-09-27",
  "keywords": [
    "cfg",
    "cfg file",
    "cfg wesnoth markup language file",
    "what is a cfg file",
    "how to open cfg file",
    "file",
    "cfg file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CFG File Format - Wesnoth Markup Language File",
  "description": "تعرف على تنسيق CFG Wesnoth Markup Language File وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CFG وفتحها.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
    }
  },
  "lastmod": "2023-09-27"
}

## What is a CFG file?

يُعرف ملف CFG أيضًا باسم **"Wesnoth Markup Language" (WML)**. إنها لغة ترميزية مخصصة تستخدم بشكل أساسي في لعبة "Battle for Wesnoth"، وهي لعبة إستراتيجية تعتمد على تبادل الأدوار. يتم استخدام WML لتحديد وتخصيص جوانب مختلفة من اللعبة، بما في ذلك السيناريوهات والحملات والوحدات والمزيد. إنها طريقة للمعدلين والمطورين لإنشاء محتوى للعبة.

إنه مكتوب بتنسيق يشبه مزيجًا من XML والبرمجة النصية البسيطة. فيما يلي نظرة عامة على بعض العناصر والهياكل الشائعة التي قد تجدها في ملف WML:

1.  **Tags:** يستخدم WML العلامات لتحديد عناصر مختلفة في اللعبة. العلامات محاطة بين قوسين زاوية. على سبيل المثال:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Attributes:** ضمن العلامات، يمكنك تعريف السمات لتحديد الخصائص أو القيم المرتبطة بالعنصر. في المثال أعلاه، يعد "النوع" و"نقاط الإصابة" من السمات.
    
3.  **Arrays and Arrays of Arrays:** يمكنك إنشاء صفائف من البيانات وحتى صفائف من المصفوفات لتحديد قوائم الوحدات أو أنواع التضاريس أو عناصر اللعبة الأخرى.
    
4.  **Conditional Statements:** يدعم WML العبارات الشرطية للتحكم في تدفق اللعبة. على سبيل المثال:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Loops:** يمكنك استخدام الحلقات للتكرار عبر قوائم العناصر أو تنفيذ الإجراءات بشكل متكرر.
    
6.  **Includes:** يمكنك تضمين ملفات WML أخرى داخل ملف WML رئيسي لتنظيم المحتوى الخاص بك وتعديله.
    
7.  **Event Handlers:** يمكنك تحديد معالجات الأحداث لتشغيل الإجراءات عند حدوث أحداث معينة في اللعبة.
    

فيما يلي مثال مبسط لملف WML الذي يحدد وحدة مخصصة:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## The Battle for Wesnoth

"The Battle for Wesnoth" هي لعبة إستراتيجية شعبية ومفتوحة المصدر تعتمد على الأدوار. وهو متاح لمنصات متعددة، بما في ذلك Mac وWindows وLinux والمزيد. تم تطوير اللعبة بواسطة مجتمع متخصص من المتطوعين، وهي معروفة بأسلوب لعبها العميق والجذاب، فضلاً عن عالمها الخيالي الغني.

تشمل الميزات الرئيسية لـ "The Battle for Wesnoth" ما يلي:

1. **الإعداد الخيالي:** تدور أحداث اللعبة في عالم خيالي يضم أعراقًا مختلفة، بما في ذلك البشر والجان والأقزام والعفاريت والمزيد. تعد تقاليد اللعبة وسرد القصص جزءًا لا يتجزأ من جاذبيتها.
    
2. ** الإستراتيجية المبنية على الأدوار: ** تعتمد طريقة اللعب على الأدوار، حيث يأخذ اللاعبون وقتهم في تخطيط وتنفيذ تحركاتهم على شبكات سداسية. فهو يجمع بين القتال التكتيكي وصنع القرار الاستراتيجي.
    
3. **الحملات:** تقدم اللعبة مجموعة واسعة من حملات اللاعب الفردي، ولكل منها قصة وشخصيات وتحديات خاصة بها. يمكن للاعبين استكشاف روايات وسيناريوهات مختلفة.
    
4. **تعدد اللاعبين:** يدعم "Wesnoth" تعدد اللاعبين عبر الإنترنت، مما يسمح للاعبين بالتنافس ضد بعضهم البعض في معارك استراتيجية. تتضمن أوضاع اللعب الجماعي اللعب التعاوني والمباريات التنافسية.

## كيفية فتح ملف CFG؟

يمكن تحرير ملفات CFG، المرتبطة عادةً بلغة Wesnoth Markup Language (WML) المستخدمة في لعبة "The Battle for Wesnoth"، بسهولة باستخدام أي محرر نصوص قياسي. تحتوي هذه الملفات على تعليمات برمجية يمكن قراءتها بواسطة الإنسان مكتوبة بلغة WML، والتي تحدد الجوانب المختلفة للعبة، بما في ذلك السيناريوهات والوحدات والحملات.

بينما يمكنك استخدام أي محرر نصوص لتعديل ملفات CFG، فإن بعض محررات النصوص المتقدمة مثل Emacs وVi تحتوي على مكونات إضافية متاحة لتسليط الضوء على تركيب WML. توفر هذه المكونات الإضافية ترميزًا وتنسيقًا مفيدًا للألوان لتسهيل على المستخدمين التمييز بين العناصر والهياكل المختلفة داخل كود WML.

تتضمن البرامج التي تفتح أو تشير إلى ملفات CFG

- The Battle for Wesnoth (Free) for (Windows, MAC, Linux)
- Microsoft Notepad

## ملفات CFG أخرى

فيما يلي أنواع الملفات الأخرى التي تستخدم امتداد الملف **.cfg**.

**Settings**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Game**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## مراجع
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)