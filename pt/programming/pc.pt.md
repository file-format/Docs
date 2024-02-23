{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo PC - Arquivo de código-fonte Pro * C - O que é arquivo .pc e como abri-lo?",
  "description" : "Aprenda sobre o arquivo de código-fonte do PC Pro*C e como abri-lo.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-pt",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## .PC opção número

Arquivo PC ou arquivo .pc é um arquivo de código-fonte ProC. ProC é um pré-compilador usado com bancos de dados Oracle para incorporar instruções SQL em código C ou C++. Quando você compila o arquivo Pro*C, ele gera código C ou C++ regular com comandos SQL incorporados. Isso permite integrar perfeitamente as operações do banco de dados SQL com seus programas C ou C++.

Aqui está um exemplo básico da aparência do arquivo Pro*C:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

Neste exemplo, as instruções SQL são prefixadas com EXEC SQL para indicar que são instruções SQL incorporadas. Essas instruções serão processadas pelo pré-compilador Pro*C quando o arquivo for compilado e o código C apropriado será gerado para interagir com o banco de dados Oracle.

## Como abrir o arquivo PC?

Para abrir um arquivo de PC, você normalmente precisa de um editor de texto ou de um Ambiente de Desenvolvimento Integrado (IDE) que suporte a edição de código-fonte C ou C++. Aqui estão algumas opções comuns:

1.  **Editores de texto:**
    
- **Bloco de notas** (Windows)
- **Editar texto** (Mac)
- **gedit** (Linux)
- **Texto Sublime**
- **Átomo**
- **Código do Visual Studio**
2.  **Ambientes de desenvolvimento integrados (IDEs):**
    
- **Eclipse** com CDT (ferramentas de desenvolvimento C/C++)
- **Visual Studio** com Visual C++ ou Visual Studio Code com extensão C++
- **Código::Blocos**
- **NetBeans** com pacote C/C++
  
## Referências
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


