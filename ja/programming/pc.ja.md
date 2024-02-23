{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC ファイル - Pro*C ソース コード ファイル - .pc ファイルとは何ですか?またその開き方は?",
  "description" : "PC Pro*C ソース コード ファイルとそれを開く方法について説明します。",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-ja",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## PCファイルとは何ですか？

PC ファイルまたは .pc ファイルは、ProC ソース コード ファイルです。 ProC は、C または C++ コード内に SQL ステートメントを埋め込むために Oracle データベースで使用されるプリコンパイラです。 Pro*C ファイルをコンパイルすると、SQL コマンドが埋め込まれた通常の C または C++ コードが生成されます。これにより、SQL データベース操作を C または C++ プログラムとシームレスに統合できます。

Pro*C ファイルがどのようなものになるかの基本的な例を次に示します。

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

この例では、SQL ステートメントには、埋め込み SQL ステートメントであることを示すために EXEC SQL というプレフィックスが付けられています。これらの文は、ファイルのコンパイル時に Pro*C プリコンパイラによって処理され、Oracle データベースと対話するための適切な C コードが生成されます。

## PCファイルを開くにはどうすればよいですか?

PC ファイルを開くには、通常、C または C++ ソース コードの編集をサポートするテキスト エディターまたは統合開発環境 (IDE) が必要です。一般的なオプションをいくつか示します。

1.  **テキストエディタ:**
    
- **メモ帳** (Windows)
- **テキストエディット** (Mac)
- **gedit** (Linux)
- **崇高なテキスト**
- **原子**
- **Visual Studio コード**
2.  **統合開発環境 (IDE):**
    
- **Eclipse** と CDT (C/C++ 開発ツール)
- **Visual Studio** (Visual C++ を使用)、または Visual Studio Code (C++ 拡張機能を使用)
- **コード::ブロック**
- **NetBeans** と C/C++ パック
  
## 参考文献
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


