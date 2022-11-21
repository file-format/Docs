{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Arquivo de referência de macro do Microsoft Office",
  "description":"Saiba mais sobre arquivos MSO e APIs que podem criar e abrir arquivos MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## O que é um arquivo MSO?

Um arquivo MSO é um formato de arquivo de contêiner de dados criado quando uma mensagem HTML é enviada usando o Microsoft Outlook. Isso acontece principalmente com aplicativos do Microsoft Office 2000. Na maioria dos casos, a mensagem de e-mail é anexada com o nome do arquivo **Oledata.mso**. O destinatário do e-mail, ao abrir tal e-mail, pode visualizar o arquivo corretamente mesmo que não tenha o mesmo software instalado. Os arquivos MSO referem-se ao [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Formato de arquivo Microsoft MSO

Os arquivos MSO são salvos no formato de arquivo composto de documento composto da Microsoft (MCDF), que também é conhecido como o formato de arquivo binário de implementação de arquivo composto de armazenamento estruturado de armazenamento estruturado OLE (Object Linking and Embedding) ou COM (Component Object Model).

### Estrutura de formato de arquivo MSO

A estrutura de formato de arquivo interno do formato de arquivo MSO é bem definida nas [Estruturas](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) da documentação do MCDF. A Tabela de Alocação de Arquivos (FAT) gerencia a alocação do setor e as cadeias do setor. Ele contém uma matriz de números de setor de 32 bits. Cada índice na matriz representa um número de setor, enquanto seu valor representa o próximo setor na cadeia ou um valor especial.

## Referências

* [Armazenamento Estruturado COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

