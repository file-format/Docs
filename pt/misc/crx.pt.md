{
"data": "08/06/2023",
  "keywords": [
"arquivo crx",
"o que é um arquivo crx",
"como instalar o arquivo crx no google chrome",
"como abrir arquivo crx",
"o que contém o arquivo crx",
"qual é o formato do arquivo crx",
"arquivo",
"extensão de arquivo crx",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo CRX - extensão do Google Chrome",
  "description":"Aprenda sobre o formato CRX e APIs que podem criar e abrir arquivos CRX.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent": "misc"
}
},
"último mod": "08/06/2023"
}

## O que é um arquivo .CRX?

O formato de arquivo CRX está associado às extensões do navegador Google Chrome. Um arquivo CRX é essencialmente um pacote compactado que contém os arquivos e metadados necessários para que uma extensão seja instalada e executada no Google Chrome. Ele aprimora a funcionalidade ou a aparência de um navegador da Web, fornecendo um recurso ou tema extra.

Quando um arquivo CRX é baixado e instalado no Google Chrome, o navegador verifica a integridade da extensão usando chave pública e assinatura. Se a verificação for bem-sucedida, o Chrome extrai o conteúdo do arquivo CRX e instala a extensão, disponibilizando-a para uso. Os usuários podem gerenciar suas extensões através da página Extensões do Chrome, que permite ativar, desativar ou remover extensões instaladas.

## Como instalar o arquivo CRX no Google Chrome?

Para instalar um arquivo CRX no Google Chrome, você pode seguir estas etapas:

1. Abra o navegador Chrome.
2. Digite `chrome://extensions` na barra de endereço e pressione Enter.
3. Ative o botão de alternância "Modo de desenvolvedor" localizado no canto superior direito da página Extensões.
4. Clique no botão "Carregar descompactado".
5. Localize e selecione a pasta que contém o conteúdo extraído do arquivo CRX (ou simplesmente selecione o próprio arquivo CRX).
6. Clique em “Abrir” para instalar a extensão.

## O que o arquivo CRX contém?

Um arquivo CRX contém os arquivos e metadados necessários para a extensão do Google Chrome. Aqui está uma análise do conteúdo típico encontrado em um arquivo CRX:

- **Arquivo de manifesto (manifest.json):** Este arquivo é um arquivo no formato JSON que inclui informações sobre a extensão, como nome, versão, descrição, permissões e scripts de segundo plano. Ele define a estrutura e o comportamento da extensão.
- **Arquivos JavaScript:** Esses arquivos contêm o código que define a funcionalidade da extensão. Eles podem incluir scripts para lidar com eventos, modificar páginas da web ou interagir com APIs do Chrome.
- **Arquivos HTML, CSS e de imagem:** as extensões geralmente incluem elementos da interface do usuário, como janelas pop-up ou páginas de opções. Os arquivos HTML definem a estrutura dessas interfaces, enquanto os arquivos CSS controlam sua aparência. Arquivos de imagem são usados para ícones ou outros recursos gráficos.
- **Arquivos de recursos opcionais:** As extensões podem incluir recursos adicionais, como arquivos de localização para suporte a vários idiomas. Esses arquivos contêm traduções de texto usado na interface do usuário da extensão.
- **Scripts em segundo plano:** Se uma extensão tiver processos em segundo plano ou scripts executados independentemente da página da Web ativa, esses scripts serão incluídos no arquivo CRX.
- **Scripts de conteúdo:** Scripts de conteúdo são scripts que podem ser injetados em páginas da Web para modificar seu comportamento ou interagir com seu conteúdo. Se a extensão usar scripts de conteúdo, os arquivos necessários para esses scripts estarão presentes no arquivo CRX.
- **Outros ativos:** Dependendo dos requisitos específicos de extensão, arquivos adicionais, como arquivos de áudio ou vídeo, fontes ou arquivos de dados, podem ser incluídos.

O formato de arquivo CRX é essencialmente um pacote compactado que contém todos esses arquivos e pastas de forma estruturada. Quando o arquivo CRX é instalado no Google Chrome, o navegador extrai o conteúdo e o coloca nos locais apropriados, permitindo que a extensão seja carregada e executada no navegador.

## Qual é o formato do arquivo CRX?

O formato de arquivo CRX é um formato específico para empacotar e distribuir extensões do Google Chrome. É essencialmente um arquivo ZIP compactado com extensões de arquivo diferentes. A estrutura básica do arquivo CRX é a seguinte:

- **Assinatura do arquivo:** Os primeiros 4 bytes do arquivo contém o número mágico "Cr24" (hexadecimal: 43 72 32 34) que serve como assinatura para identificar o arquivo como arquivo CRX.
- **Número da versão:** Os próximos 4 bytes representam o número da versão do formato CRX.
- **Comprimento da chave pública:** Os 4 bytes a seguir indicam o comprimento da chave pública codificada usada para verificação de assinatura de extensão.
- **Comprimento da assinatura:** Os 4 bytes subsequentes especificam o comprimento da assinatura da extensão.
- **Chave pública:** Esta seção contém a chave pública codificada usada para verificar a integridade da extensão.
- **Assinatura:** Esta seção contém a assinatura da extensão, que é gerada assinando o conteúdo da extensão usando uma chave privada correspondente à chave pública mencionada acima.
- **Arquivo ZIP:** Os bytes restantes do arquivo CRX compreendem um arquivo ZIP compactado. Este arquivo contém todos os arquivos e pastas de extensão necessários, incluindo arquivo de manifesto, arquivos JavaScript, arquivos HTML, arquivos CSS, imagens e quaisquer outros recursos.

## Referências
* [Especificação do formato CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

