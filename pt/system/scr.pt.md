{
  "date" : "2021-07-13",
  "keywords" :[ "arquivo scr", "o que é um arquivo scr", "arquivo", "exemplo scr", "extensão do arquivo scr", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Arquivo de proteção de tela do Windows",
  "description":"Saiba mais sobre o formato de arquivo SCR e APIs que podem criar e abrir arquivos SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## O que é um arquivo SCR?
Um arquivo com extensão .scr é um arquivo de proteção de tela usado pelo sistema operacional Microsoft Windows. Inclui animações, gráficos, apresentações de slides ou vídeos que podem ser usados como protetor de tela do Windows. Os arquivos SCR geralmente são armazenados no diretório principal do Microsoft Windows. Os protetores de tela deveriam impedir que monitores de computador CRT ou plasma sofressem com uma condição que ocorre quando a tela mostra a mesma imagem por muito tempo. Embora os monitores mais recentes não sofram com essa condição, os protetores de tela ainda são usados para impedir a tela por motivos de segurança.

## Formato de arquivo SCR
Um protetor de tela é um programa de computador que o preenche com imagens ou padrões animados quando nenhuma atividade é executada em um computador por um longo tempo. Os protetores de tela foram introduzidos para evitar a queima de fósforo em plasma, tubo de raios catódicos (CRT) e monitores de computador OLED. Os protetores de tela geralmente são configurados para aplicar uma camada básica de segurança, exigindo uma senha para reabrir o dispositivo. Os protetores de tela geralmente são desenvolvidos e codificados usando várias linguagens de programação, bem como interfaces gráficas. Principalmente os desenvolvedores de screensavers usam as linguagens de programação C ou C++, juntamente com bibliotecas gráficas ou GDIs, como OpenGL, que funciona em muitas plataformas capazes de renderização 3D. A saída dos protetores de tela é salva como um arquivo executável portátil.

### Uso do arquivo SCR
Nos monitores antigos baseados em CRT ou plasma, a queima de tela foi relatada porque a mesma imagem foi exibida na tela por um longo período. A queima de tela é um caso em que as propriedades das áreas expostas do revestimento de fósforo dentro da tela mudam gradualmente e, eventualmente, levam a uma imagem de sombra escura na tela. Assim, os protetores de tela deveriam mudar a imagem da tela continuamente e, geralmente, os arquivos .scr eram essenciais para os monitores de caixas eletrônicos ou máquinas de venda de passagens ferroviárias. Mais tarde, LCDs e versões mais avançadas de monitores resolveram o problema. Portanto, os protetores de tela ainda são usados na era moderna para proteger os dispositivos ociosos do uso da segunda pessoa. Requer a senha ou padrão para acessar novamente o dispositivo.

## Criando um protetor de tela usando C#
Embora possamos criar um protetor de tela em qualquer uma das linguagens de programação .NET, aqui é fornecida a linguagem de programação C#:

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
Altere a extensão do arquivo executável de .exe para .scr. Assim, o arquivo SCR pode ser nomeado como ScreenSaver.scr.

## Referências

* [Protetor de tela](https://en.wikipedia.org/wiki/Screensaver)
* [Escreva um protetor de tela que realmente funcione](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


