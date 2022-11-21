{
  "date" : "2021-06-30",
  "keywords" :[ "arquivo exe", "formato de arquivo exe", "o que é um arquivo exe", "arquivo", "exemplo exe", "extensão de arquivo exe", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Um arquivo .exe é um arquivo executável da Microsoft que é executado no sistema operacional Windows. Saiba mais sobre o formato de arquivo EXE.",
  "title" :"O que é um arquivo EXE executável?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## O que é um arquivo EXE?

A palavra EXE é a abreviação de **executável**. Um arquivo .exe é um programa que pode ser executado no sistema operacional Microsoft Windows. Os desenvolvedores de aplicativos publicam principalmente seus programas para o sistema operacional Windows em formato executável como arquivos exe. É o formato de arquivo padrão para executar aplicativos no Windows. **Setup.exe**, **Install.exe** e **cmd.exe** são alguns nomes comuns e bem familiares de arquivos EXE.

## Formato de arquivo EXE

Os compiladores do MS-DOS foram introduzidos com os modelos de memória com a limitação de memória de 64 K. O conceito geral é definir diferentes registradores de segmento na CPU x86 (CS, DS, ES, SS) para apontar para segmentos diferentes ou iguais, permitindo assim vários graus de acesso à memória. Alguns modelos de memória específicos foram:

- **Tiny**: Todos os acessos à memória são de 16 bits (registros de segmento inalterados). Produz um arquivo .COM em vez de um arquivo .EXE.
- **Pequeno**: Todos os acessos à memória são de 16 bits (registros de segmento inalterados).
- **Compacto**: Os endereços de dados incluem tanto o segmento quanto o deslocamento, recarregando os registros DS ou ES no acesso e permitindo até 1M de dados. Os acessos ao código não alteram o registro CS, permitindo 64K de código.
- **Médio**: Os endereços de código incluem o endereço do segmento, recarregando o CS no acesso e permitindo até 1M de código. Os acessos aos dados não alteram os registros DS e ES, permitindo 64K de dados.
- **Grande**: Ambos os endereços de código e dados são pares (segmento, deslocamento), sempre recarregando os endereços dos segmentos. Todo o espaço de memória de 1M byte está disponível para código e dados.
- **Enorme**: Igual ao modelo grande, com aritmética adicional sendo gerada pelo compilador para permitir acesso a arrays maiores que 64K.

Os desenvolvedores têm que decidir qual modelo deve ser selecionado ao criar um arquivo exe.

### Formato de arquivo EXE portátil

O formato de arquivo executável portátil (PE) contém vários cabeçalhos informativos, a seguir está a lista de cabeçalhos:

- **Cabeçalho do DOS**: O cabeçalho do MS-DOS garante compatibilidade com versões anteriores ou redução graciosa de novos tipos de arquivo.
- **PE Header**: No deslocamento 60 (0x3C) do início do cabeçalho DOS é um ponteiro para o cabeçalho do arquivo PE
- **Cabeçalho COFF**: O cabeçalho COFF contém algumas informações úteis para um executável e outras mais úteis para um arquivo objeto.
- **Cabeçalho Opcional PE**: O Cabeçalho Opcional PE ocorre logo após o cabeçalho COFF, e algumas fontes até mostram os dois cabeçalhos como parte da mesma estrutura.
- **Tabela de Seção**: Imediatamente após o Cabeçalho Opcional PE encontramos uma tabela de seção. A tabela de seção consiste em uma matriz de estruturas IMAGE_SECTION_HEADER.
- **Seções mapeáveis**: pode economizar espaço na memória mapeando o código de uma biblioteca em mais de um processo.

## Você pode executar um arquivo EXE em um Mac?

Arquivos exe não são usados como executáveis no Mac OS. No entanto, se você deseja executar um arquivo exe no Mac OS, os métodos a seguir podem ser usados.

1. **Wine** - Wine é a solução perfeita para pessoas que desejam usar seus aplicativos de PC em sistemas Mac. É um acrônimo que significa "Wine Is Not A Emulator", que significa "O vinho não é um emulador". O Wine cria o mesmo ambiente de diretórios usado pela Microsoft para que você possa executar seu aplicativo do Windows usando-o.
2. **Máquinas Virtuais** - Crie uma Máquina Virtual Windows usando Parallel Desktop ou VM Virtual Box e execute seu aplicativo dentro da máquina virtual.
3. **Boot Camp** - Instalar e configurar o Windows Boot Camp no Mac OS permite que você execute o Windows OS em uma máquina Mac.

## Referências

* [.exe- por Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

