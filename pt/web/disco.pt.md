{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo DISCO - Formato de arquivo de documento de descoberta DISCO",
  "description":"Saiba mais sobre o que é um arquivo DISCO e APIs que podem criar e abrir arquivos DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## O que é um arquivo DISCO?

Um arquivo DISCO é um formato de arquivo do Microsoft Discovery usado para publicação e descoberta de Web Services. Ele é armazenado no formato de arquivo XML e permite que as ferramentas Web Services Discovery localizem ou descubram um ou mais documentos relacionados para descrever os serviços [XML](/pt/web/xml/) disponíveis. O arquivo DISCO armazena informações como documentos de descoberta, esquemas [XSD](/programming/xsd/) e descrições de serviço. Os serviços da Web XML usam essas informações para acessar os serviços Web XML disponíveis em uma determinada URL.

## Formato de arquivo DISCO - Mais informações

Os arquivos DISCO são salvos no formato de arquivo XML. O Microsoft Discovery Tool (DISCO.exe), que vem junto com o software de desenvolvimento Microsoft ASP.NET, como o Microsoft Studio, usa os arquivos DISCO para descobrir os detalhes sobre os serviços XML da Web listados em um DiscoveryDocument em uma URL específica. A Microsoft forneceu suporte para leitura de arquivos de descoberta no .NET framework.

## Referências

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Descoberta de serviços da Web](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Exemplo C# da classe DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

