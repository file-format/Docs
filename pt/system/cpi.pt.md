{
"data":"18/10/2023",
   "keywords":[
"cpi",
"arquivo cpi",
"arquivo de informações da página de código cpi",
"como abrir um arquivo cpi",
"arquivo",
"extensão de arquivo cpi",
"extensão",
"arquivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"Formato de arquivo CPI - Arquivo de informações de página de código",
   "description":"Aprenda sobre o formato de arquivo de informações da página de código CPI e APIs que podem criar e abrir arquivos CPI.",
"linktitle":"IPC",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
"parent":"sistema"
}
},
"última modificação":"2023/10/18"
}

## O que é um arquivo .CPI?

Um arquivo `.cpi`, no contexto dos sistemas operacionais Microsoft Windows e DOS, normalmente é **"Arquivo de informações de página de código."** Esses arquivos contêm informações sobre páginas de código usadas para codificação de texto e mapeamentos de conjuntos de caracteres. As páginas de código são essenciais para exibir e processar texto em vários idiomas e conjuntos de caracteres.

No contexto do Windows e do DOS, as páginas de código são usadas para definir como os caracteres são representados e codificados em diferentes idiomas e regiões. Essas páginas de código determinam como os caracteres são armazenados na memória e exibidos na tela. Cada página de código possui um identificador exclusivo e os arquivos `.cpi` armazenam informações sobre essas páginas de código, incluindo detalhes como mapeamentos de caracteres e informações de fonte.

Os arquivos `.cpi` são comumente encontrados nos diretórios do sistema Windows ou DOS e desempenham um papel crucial ao permitir que o sistema operacional exiba texto corretamente para diferentes localidades e conjuntos de caracteres. Eles ajudam o sistema a entender como interpretar e renderizar caracteres de diferentes idiomas e codificações.

## Arquivos de informações de página de código

Vamos dar uma olhada mais de perto nos arquivos de informações da página de código (.cpi) e como eles funcionam na estrutura do MS-DOS e nas iterações anteriores do Microsoft Windows:

1. **Codificação de caracteres e páginas de código**: As páginas de código são componentes críticos de como o texto é codificado e exibido no computador. Eles definem a codificação de caracteres para um idioma ou conjunto de caracteres específico. Cada página de código atribui valores numéricos (pontos de código) aos caracteres, permitindo que o computador os represente e exiba. Por exemplo, a página de código 437 é comumente usada nos Estados Unidos e na Europa Ocidental, enquanto a página de código 850 é usada para codificação Latin-1.
    







2. **Inicialização do sistema**: Durante a inicialização do sistema (quando o computador inicializa), o MS-DOS e versões mais antigas do Windows leriam arquivos `.cpi` para determinar quais páginas de código suportar. Essas informações foram cruciais para renderização de texto, entrada de teclado e conversões de conjuntos de caracteres.
    







3. **Suporte a tela e teclado**: esses arquivos fornecem informações sobre como os caracteres devem ser exibidos na tela e quais conjuntos de caracteres ou páginas de código devem ser suportados para entrada do teclado. Diferentes páginas de código definem diferentes conjuntos de caracteres, portanto, esses arquivos ajudam o sistema operacional a saber como lidar com a entrada do usuário e exibir o texto corretamente.
    







4. **Localização**: Os arquivos `.cpi` são essenciais para a localização do sistema operacional. Eles permitem que o sistema se adapte a diferentes idiomas, regiões e conjuntos de caracteres, possibilitando que usuários de todo o mundo utilizem o MS-DOS ou o Windows em seus idiomas preferidos.
    







5. **Vários arquivos `.cpi`**: Em computadores com suporte multilíngue, você pode encontrar vários arquivos `.cpi` correspondentes a diferentes páginas de código. Por exemplo, o sistema pode ter `437.cpi` para os Estados Unidos, `850.cpi` para Latin-1, `852.cpi` para a Europa Central e assim por diante. O arquivo apropriado é carregado com base na localidade do usuário ou na página de códigos selecionada.
    







6. **Informações de fonte**: Além dos mapeamentos de caracteres, esses arquivos podem conter informações de fonte, especificando quais fontes usar para cada página de código. Isso é importante para renderizar o texto no estilo e tamanho apropriados.
    







7. **Sistemas legados**: arquivos `.cpi` eram mais comuns em versões mais antigas do MS-DOS e Windows. Versões modernas do Windows (como Windows 10 e posteriores) normalmente usam Unicode para codificação de texto, que oferece suporte a uma ampla variedade de caracteres e idiomas. Unicode simplifica o processamento de texto para ambientes multilíngues e é padrão para software moderno.

## Como abrir o arquivo CPI?

Abrir um arquivo .CPI (Code Page Information) não é uma ação típica do usuário e esses arquivos geralmente não devem ser abertos manualmente. Eles são usados pelo sistema operacional para gerenciar codificação de texto e conjuntos de caracteres e seu conteúdo é acessado e utilizado automaticamente pelo sistema.

No entanto, se estiver interessado em visualizar o conteúdo do arquivo .CPI para fins informativos, você pode tentar abri-lo com um editor de texto ou visualizador hexadecimal. Aqui está como você pode tentar abrir o arquivo .CPI:

1. **Editor de Texto**: Você pode usar um editor de texto como o Bloco de Notas (no Windows) ou qualquer editor de texto simples em outros sistemas operacionais para abrir e visualizar o arquivo .CPI. Lembre-se de que o conteúdo dos arquivos .CPI não deve ser legível por humanos e você poderá ver séries de caracteres difíceis de interpretar.
    







2. **Visualizador hexadecimal**: Um visualizador hexadecimal ou editor hexadecimal pode ser usado para abrir e inspecionar o conteúdo do arquivo .CPI em sua forma binária bruta. Os editores hexadecimais fornecem uma visão mais detalhada dos dados do arquivo, o que pode ser útil se você estiver tentando entender sua estrutura. Exemplos desse tipo de software incluem HxD, Hex Fiend (para macOS) e 010 Editor.

## Outros arquivos CPI

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.cpi**.

**Sistema de vídeo**
- [CPI - Informações do clipe de vídeo AVCHD](/pt/video/cpi/)
- [CPI - Arquivo de informações da página de código](/pt/system/cpi/)

## Referências
* [Página de código](https://en.wikipedia.org/wiki/Code_page)

