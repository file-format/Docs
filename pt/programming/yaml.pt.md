{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","o que é um arquivo yaml","como abrir um arquivo yaml", "extensão", "arquivo", "arquivo yaml","formato de arquivo yaml", "extensão .yaml" , "yaml vs json" ,"exemplo de arquivo YAML", "exemplo de arquivo yaml docker"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Saiba mais sobre o formato de arquivo YAML e as APIs que podem criar e abrir um arquivo YAML.",
  "title" :"Formato de arquivo YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## O que é um arquivo YAML? ##

O **arquivo YAML** consiste em uma linguagem YAML (YAML Ain't Markup Language), que é uma linguagem de serialização de dados baseada em Unicode; usado para arquivos de configuração, mensagens da Internet, persistência de objetos, etc. O YAML usa a extensão .yaml para seus arquivos. Sua sintaxe é independente de uma linguagem de programação específica. Basicamente, o YAML é projetado para interação humana e para funcionar bem com linguagens de programação modernas. O suporte para serialização de estruturas de dados nativas arbitrárias aumentou a legibilidade dos arquivos YAML, mas complicou um pouco o processo de análise e geração de arquivos.

## Breve história ##

O YAML foi proposto pela primeira vez em 2001 e foi desenvolvido por Clark Evans, Ingy döt Net e Oren Ben-Kiki. YAML foi dito pela primeira vez para significar "Yet Another Markup Language" para indicar seu propósito como uma linguagem de marcação. Mais tarde, foi reaproveitado como "YAML Aint Markup Language" para indicar seu propósito como orientado a dados.


## Formato de arquivo YAML ##

O arquivo YAML consiste nos seguintes tipos de dados

- **Escalares**: Escalares são valores como Strings, Integers, Booleans, etc.
- **Sequências**: As sequências são listas com cada item começando com um hífen (-). As listas também podem ser aninhadas.
- **Mapeamentos**: O mapeamento permite listar chaves com valores.

### Sintaxe ###

- **Espaço em branco**: o recuo do espaço em branco é usado para indicar o aninhamento e a estrutura geral.

```yaml
nome: John Smith
contato:
casa: 1012355532
escritório: 5002586256
Morada:
rua: |
123 Tornado Alley
Suíte 16
cidade: East Centerville
estado: KS
```

- **Comentários**: Os comentários são escritos começando com o símbolo "#".

```yaml
# Este é um comentário YAML
```

- **Listas**: O hífen (-) é usado para indicar os membros da lista com cada membro em uma linha separada. Os membros da lista também podem ser colocados entre colchetes ([...]) com membros separados por vírgulas (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A, B, C]
```

- **Matriz associativa**: Uma matriz associativa é cercada por colchetes ({...}). As chaves e os valores são separados por dois pontos (:) e cada par é separado por vírgula (,).

```yaml
  {name: John Smith, age: 20}
```

- **Strings**: A string pode ser escrita com ou sem aspas duplas ("") ou aspas simples (').

```yaml
Sequência de Amostra
"Cadeia de Amostra"
'Cadeia de Amostra'
```

- **Conteúdo de bloco escalar**: o conteúdo escalar pode ser escrito em notação de bloco usando o seguinte:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
dados: |
YAML
(YAML não é linguagem de marcação)
é uma linguagem de serialização de dados
```

```yaml
dados: ?
YAML (YAML não é linguagem de marcação)
é uma linguagem de serialização de dados
```

- **Vários documentos**: vários documentos são separados por três hífens (---) em um único fluxo. Os hífens indicam o início do documento. Os hífens também são usados para separar as diretivas do conteúdo do documento. O final do documento é indicado por três pontos (...).

```yaml
  ---
Documento 1
  ---
Documento 2
...
```

- **Tipo**: Para especificar o tipo de valor, são usados pontos de exclamação duplos (!!).

```yaml
a: !!float 123
b: !!str 123
```

- **Tag**: Para atribuir um tag a uma nota, é usado um e comercial (&) e para fazer referência a esse nó, um asterisco (*) é usado.

```yaml
nome: John Smith
faturar para: &id01
rua: |
123 Tornado Alley
Suíte 16
cidade: East Centerville
estado: KS

destino: *id01
```

- **Diretivas**: documentos YAML podem ser precedidos por diretivas em um fluxo. As diretivas começam com um sinal de porcentagem (%) seguido do nome e dos parâmetros separados por espaços.

```yaml
%YAML 1.2
  ---
Conteúdo do documento
```
## Exemplo de arquivo YAML
Aqui você pode ver um **exemplo de arquivo yaml do docker** abaixo:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML x JSON
Basicamente, JSON e YAML são desenvolvidos para fornecer um formato de intercâmbio de dados legível por humanos. O YAML é realizado como um superconjunto do formato JSON. Isso significa que podemos analisar JSON usando um analisador YAML. Embora a implementação prática desta teoria seja um pouco complicada. Portanto, algumas diferenças básicas entre YAML e JSON são fornecidas abaixo:

|YAML| JSON|
---|---|
|Processo complexo e demorado de análise de dados serializados |Análise rápida e fácil de dados serializados JSON com seu design mais simples|
|Menos suporte da comunidade| Maior apoio e popularidade da comunidade|
|Suporta comentários| Não suporta comentários|
|Capacidade de usar referência de outros objetos de dados| Impossível serializar estruturas complexas com referências de objetos|
|A hierarquia é indicada usando caracteres de espaço duplo. Caracteres de tabulação não são permitidos|Objetos e Arrays são indicados entre colchetes e colchetes.|
|Aspas de string são opcionais, mas suporta aspas simples e duplas.|Strings devem estar entre aspas duplas.|
|O nó raiz pode ser qualquer um dos tipos de dados válidos|O nó raiz deve ser uma matriz ou um objeto.|


## Referências ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

