{
"data":"20/07/2023",
   "keywords":[
"BIN",
"Arquivo BIN",
"arquivo",
"Extensão de arquivo BIN",
"extensão",
"arquivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"Formato de arquivo BIN - arquivo executável Unix",
   "description":"Aprenda sobre o formato BIN e APIs que podem criar e abrir arquivos BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent" : "executable"
}
},
"último mod":"2023-07-20"
}

## O que é um arquivo .BIN?

Um arquivo BIN é um arquivo executável em sistemas operacionais baseados em Unix, como Linux ou FreeBSD. Ele contém um programa compilado composto de código binário derivado do código-fonte, tornando-o compatível com a arquitetura do sistema subjacente. Os arquivos BIN executáveis Unix podem ser comparados aos arquivos .EXE do Windows e aos arquivos .APP do macOS em termos de sua função como formatos executáveis.

No domínio do desenvolvimento de software para sistemas Unix, os arquivos BIN são comumente empregados pelos desenvolvedores para empacotar e distribuir programas. Eles oferecem um meio conveniente de entrega de software aos usuários, permitindo fácil instalação e execução. Juntamente com os arquivos BIN, existem outros tipos de executáveis Unix, incluindo [.ELF](/pt/executável/elf/), .X86, [.RUN](/pt/executável/run/) e .X86_64, cada um adaptado para hardware específico ou requisitos de sistema.

Quando se trata da estrutura interna de um arquivo BIN, ela consiste em dados codificados que o sistema operacional Unix utiliza para identificar, ler e executar o programa incluído. O sistema depende de assinaturas ou cabeçalhos de arquivos específicos para reconhecer o arquivo BIN como um executável, seguido pela interpretação e execução das instruções binárias contidas nele.

Os arquivos BIN geralmente vêm acompanhados de um arquivo **INSTALL.TXT**, que fornece instruções detalhadas sobre como instalar e configurar corretamente o programa. Esta documentação garante que os usuários possam navegar pelo processo de instalação com êxito e começar a utilizar o software sem complicações.

## Como abrir o arquivo BIN?

Os arquivos BIN não foram projetados para serem abertos e visualizados diretamente. No entanto, você pode executar os programas ou extrair os dados que eles contêm. Para acessar o conteúdo de um arquivo BIN, siga estas etapas na linha de comando, assumindo que o nome do arquivo BIN seja "sample.bin":

1. **Garanta permissões executáveis:**

Antes de executar o arquivo BIN, certifique-se de que ele tenha as permissões necessárias para ser executado como executável. Use o comando:

```
$ chmod +x sample.bin
```

Este comando concede privilégios executáveis ao arquivo.

2. **Execute o arquivo BIN:**

Depois de definir as permissões executáveis, você pode executar o arquivo BIN digitando o seguinte comando:

```
$ ./sample.bin
```

**Aviso**

_Tenha cuidado ao lidar com arquivos BIN baixados ou enviados por e-mail, pois eles podem ser potencialmente usados por cibercriminosos para distribuir malware. Execute apenas arquivos BIN de fontes confiáveis para mitigar o risco de ataques executáveis maliciosos._

## Outros arquivos BIN

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.bin**.

- [BIN - Arquivo codificado MacBinary](/pt/compression/bin/)
- [BIN - Arquivo de imagem de disco binário](/pt/disc-and-media/bin/)
- [BIN - Arquivo de política de TI do BlackBerry](/pt/settings/bin/)
- [BIN - ROM do jogo Sega Genesis](/pt/game/bin/)
- [BIN - Imagem do BIOS do PSX PlayStation](/pt/game/bin-pcsx/)

## Referências

* [Como executar arquivos binários no Linux](https://linuxhint.com/execute-binary-files-in-linux/)


