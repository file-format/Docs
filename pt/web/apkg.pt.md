{
  "date" : "2019-10-11",
   "keywords" :[ "apkg", "arquivo apkg", "formato de arquivo apkg", "tipo de arquivo apkg", "arquivo", "tipo", "O que é um arquivo APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck File Format",
  "description" :"Saiba mais sobre o que é um arquivo APKG e APIs que podem criá-los e abri-los.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## O que é um arquivo APKG?

Um arquivo com extensão .apkg é um baralho de flashcards gerado para ser usado no aplicativo de software [Anki](https://ankiweb.net/about), que é um programa de aprendizado baseado em flashcard. Ele contém texto [HTML](/pt/web/html/) a ser carregado e exibido no aplicativo Anki e também pode ter imagens e sons para aprendizado visual e audível. O Anki permite que os usuários criem seus próprios decks de flashcards Anki, bem como importem os decks de flashcards de outros usuários.

## Formato de arquivo APKG

Os baralhos de cartas Anki são criados a partir de modelos escritos em HTML, uma linguagem famosa e comum para a criação de páginas da web. O estilo de cartas de baralho é feito usando CSS, que é a linguagem usada para estilizar páginas da web. O estilo inclui modificações para:

* font-family - O nome da fonte a ser usada no cartão.
* font-size - O tamanho da fonte em pixels.
* text-align - Define se o texto deve ser alinhado ao centro, à esquerda ou à direita.
* color - Define a cor do texto que pode ser nomes de cores simples como "azul", "vermelho", etc. ou códigos de cores HTML.
* background-color - Define a cor de fundo do cartão

As informações de estilo são compartilhadas entre todos os cartões, afetando todos os cartões quando uma alteração é feita. O exemplo a seguir usará um fundo amarelo em todos os cartões, exceto o primeiro:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

O redimensionamento de imagens em um cartão Anki pode ser controlado da seguinte forma.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Incorporando Javascript em cartões Anki

É possível incorporar [Javascript](/pt/web/js/) em um cartão Anki usando os modelos de cartão. No entanto, devido ao nível avançado de Javascript, seu suporte não é fornecido. Além disso, dispositivos de renderização podem mostrar os efeitos de implementação de Javascript no cartão de forma diferente, resultando na necessidade de testar a implementação em todos os dispositivos. Certos recursos Javascript, como window.alert, dificultam a depuração do código Javascript que você escreveu.

## Referências ##

* [Documentação do Anki](https://docs.ankiweb.net/intro.html)

