{
  "date" : "2021-07-13",
  "keywords" :[ "archivo scr", "qué es un archivo scr", "archivo", "ejemplo de scr", "extensión de archivo scr","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Archivo de salvapantallas de Windows",
  "description":"Obtenga información sobre el formato de archivo SCR y las API que pueden crear y abrir archivos SCR",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## ¿Qué es un archivo SCR?
Un archivo con extensión .scr es un archivo de protector de pantalla utilizado por el sistema operativo Microsoft Windows. Comprende animaciones, gráficos, presentaciones de diapositivas o videos que se pueden usar como protector de pantalla de Windows. Los archivos SCR se almacenan comúnmente en el directorio principal de Microsoft Windows. Se suponía que los protectores de pantalla evitarían que los monitores de computadora CRT o de plasma sufrieran una condición que ocurre cuando la pantalla muestra la misma imagen durante demasiado tiempo. Aunque, los últimos monitores no sufren en tal condición, pero los protectores de pantalla todavía se utilizan para evitar la pantalla por razones de seguridad.

## Formato de archivo SCR
Un protector de pantalla es un programa de computadora que lo llena con imágenes animadas o patrones cuando no se realiza ninguna actividad en una computadora durante mucho tiempo. Los protectores de pantalla se introdujeron para evitar que el fósforo se queme en los monitores de computadora de plasma, tubo de rayos catódicos (CRT) y OLED. Los protectores de pantalla generalmente se configuran para aplicar una capa básica de seguridad, al solicitar una contraseña para volver a abrir el dispositivo. Los protectores de pantalla generalmente se desarrollan y codifican utilizando varios lenguajes de programación, así como interfaces gráficas. La mayoría de los desarrolladores de protectores de pantalla utilizan los lenguajes de programación C o C++, junto con bibliotecas gráficas o GDI, como OpenGL, que funciona en muchas plataformas capaces de renderizar en 3D. La salida del protector de pantalla se guarda como un archivo ejecutable portátil.

### Uso del archivo SCR
En los monitores antiguos CRT o basados en plasma, se informó que la pantalla se quemó porque la misma imagen se mostró en la pantalla durante un período prolongado. La quemadura de pantalla es un caso en el que las propiedades de las áreas expuestas del revestimiento de fósforo dentro de la pantalla cambian gradualmente y eventualmente conducen a una imagen de sombra oscura en la pantalla. Por lo tanto, se suponía que los protectores de pantalla cambiaban la imagen de la pantalla continuamente y, por lo general, los archivos .scr eran esenciales para los monitores de cajeros automáticos o máquinas expendedoras de billetes de tren. Más tarde, las pantallas LCD y las versiones más avanzadas de los monitores resolvieron el problema. Por lo tanto, los protectores de pantalla todavía se usan en la era moderna para proteger los dispositivos inactivos del uso en segunda persona. Requiere la contraseña o patrón para volver a acceder al dispositivo.

## Creando un salvapantallas usando C#
Aunque podemos crear un protector de pantalla en cualquiera de los lenguajes de programación .NET, aquí se da el lenguaje de programación C#:

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
Cambie la extensión del archivo ejecutable de .exe a .scr. Entonces, el archivo SCR puede llamarse ScreenSaver.scr.

## Referencias

* [Salvapantallas](https://en.wikipedia.org/wiki/Screensaver)
* [Escriba un salvapantallas que realmente funcione](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


