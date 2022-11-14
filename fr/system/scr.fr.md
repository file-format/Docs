{
  "date" : "2021-07-13",
  "keywords" :[ "fichier scr", "qu'est-ce qu'un fichier scr", "fichier", "exemple scr", "extension de fichier scr", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Fichier d'économiseur d'écran Windows",
  "description":"En savoir plus sur le format de fichier SCR et les API qui peuvent créer et ouvrir des fichiers SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Qu'est-ce qu'un fichier SCR ?
Un fichier avec l'extension .scr est un fichier d'économiseur d'écran utilisé par le système d'exploitation Microsoft Windows. Il comprend des animations, des graphiques, des diaporamas ou des vidéos pouvant être utilisés comme économiseur d'écran Windows. Les fichiers SCR sont généralement stockés dans le répertoire principal de Microsoft Windows. Les économiseurs d'écran étaient censés empêcher les écrans d'ordinateur CRT ou plasma de souffrir d'une condition qui survient lorsque l'écran affiche la même image trop longtemps. Bien que les derniers moniteurs ne souffrent pas dans un tel état, mais les économiseurs d'écran sont toujours utilisés pour empêcher l'écran pour des raisons de sécurité.

## Format de fichier SCR
Un économiseur d'écran est un programme informatique qui le remplit d'images ou de motifs animés lorsqu'aucune activité n'est effectuée sur un ordinateur pendant une longue période. Les économiseurs d'écran ont été introduits pour empêcher la brûlure du phosphore sur les écrans plasma, à tube cathodique (CRT) et OLED. Les économiseurs d'écran sont généralement configurés pour appliquer une couche de sécurité de base, en exigeant un mot de passe pour rouvrir l'appareil. Les économiseurs d'écran sont généralement développés et codés à l'aide de divers langages de programmation ainsi que d'interfaces graphiques. La plupart des développeurs d'économiseurs d'écran utilisent les langages de programmation C ou C++, ainsi que des bibliothèques graphiques ou GDI, comme OpenGL, qui fonctionne sur de nombreuses plates-formes capables de rendu 3D. La sortie des économiseurs d'écran est enregistrée sous forme de fichier exécutable portable.

### Utilisation du fichier SCR
Dans les anciens moniteurs CRT ou plasma, la brûlure d'écran a été signalée car la même image était affichée à l'écran pendant une longue période. La brûlure d'écran est un cas où les propriétés des zones exposées du revêtement de phosphore à l'intérieur de l'écran changent progressivement et conduisent finalement à une image d'ombre assombrie sur l'écran. Ainsi, les économiseurs d'écran étaient censés changer l'image de l'écran en continu et généralement, les fichiers .scr étaient essentiels pour les moniteurs des guichets automatiques ou ferroviaires. Plus tard, les écrans LCD et les versions plus avancées des moniteurs ont résolu le problème. Par conséquent, les économiseurs d'écran sont encore utilisés à l'ère moderne pour protéger les appareils inactifs de l'utilisation par une deuxième personne. Il nécessite le mot de passe ou le modèle pour accéder à nouveau à l'appareil.

## Créer un économiseur d'écran en C#
Bien que nous puissions créer un économiseur d'écran dans n'importe lequel des langages de programmation .NET, ici le langage de programmation C# est donné :

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
Modifiez l'extension du fichier exécutable de .exe à .scr. Ainsi, le fichier SCR peut être nommé ScreenSaver.scr.

## Références

* [Écran de veille] (https://en.wikipedia.org/wiki/Écran de veille)
* [Écrire un économiseur d'écran qui fonctionne réellement] (https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


