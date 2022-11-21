{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "arquivo", "extensão", "formato de arquivo", "Word", "Documento" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Arquivo de Documento do Microsoft Word",
  "description":"Saiba mais sobre o formato de arquivo DOC e APIs que podem criar e abrir arquivos DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## O que é um arquivo DOC?

Arquivos com extensão .doc representam documentos gerados pelo Microsoft Word ou outros documentos de processamento de texto em formato de arquivo binário. A extensão foi inicialmente usada para documentação de texto simples em vários sistemas operacionais diferentes. Ele pode conter vários tipos diferentes de dados, como imagens, formatação e texto simples, gráficos, tabelas, objetos incorporados, links, páginas, formatação de página, configurações de impressão e muitos outros. O formato era popular para todo tipo de documentação devido à variedade de opções que oferece aos usuários para escrever manuais, propostas, especificações, currículos, artigos ou documentos semelhantes. A versão atualizada do DOC é [DOCX](/pt/Word%20Processing/DOCX/) que é baseada no Office OpenXML cujas especificações estão disponíveis abertamente.

## Breve história ##

WordPerfect, um produto da [Corel](https://www.corel.com/en/), usou DOC como extensão de seu formato proprietário. Na década de 1980, o WordPerfect permaneceu como a escolha de uso na maioria dos computadores devido à sua fácil disponibilidade, conformidade com a maioria das máquinas e sistemas operacionais. No entanto, o WordPerfect viu sua queda no sistema operacional Windows quando a Microsoft introduziu o Microsoft Word como seu produto para o formato de arquivo de documentos e escolheu a extensão DOC para seu formato proprietário. À medida que o Microsoft Word se tornou cada vez mais popular, o formato de arquivo DOC passou por várias revisões do Microsoft Word 97 - 2003. Foi em 2007 quando o formato de arquivo DOC padrão foi substituído pelo formato Office Open XML (conhecido como DOCX) e as novas versões do O Microsoft Word agora usa essa nova extensão como formato de arquivo padrão.

## Especificações de formato de arquivo DOC - Mais informações

A Microsoft não lançou as especificações de formato de arquivo DOC por um longo tempo até 2008. Em fevereiro de 2008, as especificações de formato foram lançadas para o formato de arquivo .doc sob a Microsoft Open Specification Promise. Embora a especificação não descreva todos os recursos usados pelo formato DOC, ela fornece amplas informações sobre o conhecimento necessário para trabalhar com esse formato de arquivo. Ainda assim, a engenharia reversa é necessária para fazer uso das informações disponíveis. As especificações foram atualizadas várias vezes e a [revisão] mais recente (https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) é 8.0, atualizada em agosto de 2018 .

### Alguns Conceitos Fundamentais ###

Antes de entrarmos em detalhes sobre as especificações de formato de arquivo para DOC, é necessário entender alguns conceitos fundamentais para trabalhar com esse formato de arquivo.

**File Information Base (Fib):** A estrutura Fib contém informações sobre o documento e especifica os ponteiros de arquivo para várias partes que compõem o documento.
O Fib é uma estrutura de comprimento variável. Com exceção da parte de base que é de tamanho fixo, cada seção é precedida por um campo de contagem que especifica o tamanho da próxima seção.

**Posição do caractere:** CP ou Posição do caractere representa um inteiro sem sinal de 32 bits que serve como índice baseado em zero de um caractere no texto do documento. A localização e o tamanho de cada caractere no arquivo não podem ser recuperados diretamente e precisam ser calculados usando um algoritmo pré-especificado. Os personagens incluem:

* Texto do documento
* Âncoras de objetos como notas de rodapé ou caixas de texto
* Caracteres de controle, como marcas de parágrafo e marcas de célula de tabela

**PLC:** A estrutura do PLC é um array de CPs seguido por um array de elementos de dados. Os elementos de dados para qualquer PLC devem ter o mesmo tamanho de zero ou mais bytes, e por esta razão, o número de CPs deve ser um a mais que o número de elementos de dados. As estruturas PLC são de diferentes tipos, onde cada tipo especifica se CPs duplicados são permitidos para aquele tipo ou não. Uma estrutura de PLC consiste em:

* **aCP (tamanho variável):** Uma matriz de elementos CP. Cada tipo de estrutura **PLC** especifica o significado dos elementos CP e o intervalo permitido.
* **aData (comprimento variável):** Cada tipo de estrutura **PLC** especifica a estrutura e o significado dos elementos de dados, quaisquer restrições sobre o número de elementos de dados e quaisquer restrições sobre os dados contidos nele. Também especifica a relação entre os elementos de dados e os CPs correspondentes.

**Seleção válida:** as construções do arquivo .DOC são descritas principalmente por uma variedade de CPs. Há várias [regras](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) especificadas pela Microsoft a serem seguidas nesse caso.

**STTB:** o STTB é uma tabela de strings composta por um cabeçalho seguido por uma matriz de elementos. O valor **cData** especifica o número de elementos contidos na matriz.

**Armazenamento de propriedades:** um arquivo word pode ter diferentes elementos como texto, parágrafos, tabelas, imagens e seções onde cada um pode ter suas próprias propriedades. As propriedades destes são armazenadas no arquivo do Word como diferenças do padrão. Tais diferenças são especificadas pelo PRl que consiste em um modificador de propriedade única (Sprm) e seu operando. Um aplicativo pode determinar o conjunto final de propriedades pela aplicação de listas de **Prl**s.

**Proteção por senha:** arquivos do Word também podem ser protegidos por senha, para o qual um dos seguintes mecanismos pode ser usado.

* Ofuscação XOR
* Criptografia RC4 de documento binário do Office
* Criptografia RC4 CryptoAPI do documento binário do Office

Se FibBase.fEncrypted e FibBase.fObfuscation forem ambos 1, o arquivo será ofuscado usando ofuscação XOR.

Se FibBase.fEncrypted for 1 e FibBase.fObfuscation for 0, o arquivo será criptografado usando a Criptografia Office Binary Document RC4 ou a Criptografia Office Binary Document RC4 CryptoAPI, com o EncryptionHeader armazenado nos primeiros bytes FibBase.lKey do fluxo Tabela. O EncryptionHeader.EncryptionVersionInfo especifica qual mecanismo de criptografia foi usado para criptografar o arquivo.

### Estrutura do arquivo ###

Um arquivo binário do Word em sua originalidade é um arquivo composto OLE que compreende vários armazenamentos e fluxos. Esses armazenamentos e fluxos possuem estrutura e tamanhos próprios, que especificam os parâmetros de escrita e leitura. Estes são:

#### Fluxo de documentos do Word ####

Este fluxo contém o texto do documento e outras informações referenciadas de outras partes do arquivo. O fluxo não tem estrutura predefinida além do FIB no início, que é obrigatório e deve estar no deslocamento 0. Este fluxo não deve ser maior que 2147 MB.

#### 1TableStream ou 0TableStream ####

Um arquivo binário do Word pode conter fluxos de tabela conhecidos como fluxo 1Table ou fluxo 0Table. Pelo menos um deles deve estar presente no documento. No entanto, se um documento contiver fluxos 1Table e 0Table, somente o fluxo referenciado por base.fWhichTblStm será usado. O fluxo não referenciado DEVE ser ignorado.
O Table Stream NÃO DEVE ser maior que 2147 MB.

#### Fluxo de dados ####

O fluxo de dados não tem estrutura predefinida. Ele contém dados referenciados do FIB ou de outras partes do arquivo. Este fluxo não precisa estar presente se não houver referências a ele. O fluxo de dados NÃO DEVE ser maior que 2147 MB.

#### Armazenamento do conjunto de objetos ####

O armazenamento do Pool de Objetos contém armazenamentos para objetos OLE incorporados. Esse armazenamento não precisa estar presente se não houver objetos OLE incorporados no documento.

#### Armazenamento de dados XML personalizado ####

O armazenamento de dados XML personalizados é um armazenamento opcional cujo nome DEVE ser "MsoDataStore".

#### Fluxo de informações resumidas ####

O fluxo de informações de resumo é um fluxo opcional cujo nome DEVE ser "\005SummaryInformation", onde \005 é o caractere com valor 0x0005 e não a string literal "\005".

#### Fluxo de informações do resumo do documento ####

O fluxo de informações de resumo do documento é um fluxo opcional cujo nome DEVE ser "\005DocumentSummaryInformation", onde \005 é o caractere com valor 0x0005, não a string literal "\005".

#### Fluxo de criptografia ####

O fluxo de criptografia é um fluxo opcional cujo nome DEVE ser "criptografia". Este fluxo NÃO DEVE estar presente a menos que ambas as condições a seguir sejam atendidas:

* O documento é criptografado com Criptografia Office Binary Document RC4 CryptoAPI.
* O valor fDocProps é definido no EncryptionHeader.Flags.

#### Armazenamento de macros ####

O armazenamento de macros é um armazenamento opcional que contém as macros do arquivo. Se estiver presente, DEVE ser um Armazenamento Raiz do Projeto.

#### Armazenamento de assinaturas XML ####

O armazenamento de assinaturas XML é um armazenamento opcional cujo nome DEVE ser "_xmlsignatures".

#### Fluxo de assinaturas ####

O stream de assinaturas é um stream opcional cujo nome DEVE ser "_signatures". Este fluxo contém assinaturas digitais.

#### Gerenciamento de Direitos de Informação Armazenamento de Espaço de Dados ####

O armazenamento do Information Rights Management Data Space é um armazenamento opcional cujo nome DEVE ser "\006DataSpaces", onde \006 é o caractere com valor 0x0006, e não a string literal "\006". Se esse armazenamento estiver presente, o fluxo de conteúdo protegido também DEVE estar presente.
Se este armazenamento estiver presente, todos os fluxos e armazenamentos especificados, exceto este armazenamento e o fluxo de conteúdo protegido, DEVEM ser lidos do fluxo de conteúdo protegido conforme especificado em [MS-OFFCRYPTO] e se algum desses fluxos e armazenamentos existir fora do conteúdo protegido Stream, eles DEVEM ser ignorados.

#### Fluxo de conteúdo protegido ####

O Protected Content Stream é um stream opcional cujo nome DEVE ser "\009DRMContent", onde \009 é o caractere com valor 0x0009, e não a string literal "\009".
Se esse fluxo estiver presente, o Armazenamento do Espaço de Dados do Gerenciamento de Direitos de Informação também DEVE estar presente.

## Referências ##

* [Especificações de formação de arquivo MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

