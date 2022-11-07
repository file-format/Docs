{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar ファイル形式",
  "description":"ICS ファイル形式と,ICS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .ICS ファイル拡張子

Internet Calendaring and Scheduling Core Object Specification (iCalendar) は、カレンダー イベントとスケジューリングを交換および展開するためのインターネット標準 (RFC 2445) です。 iCalendar 形式は相互運用可能であるため、さまざまな電子メール アプリケーションを使用しているユーザー間でカレンダー情報を交換できます。 iCalendar は、入力データを Multipurpose Internet Mail Extensions (MIME) としてフォーマットし、さまざまなトランスポート プロトコルを介して交換されるオブジェクトを容易にします。これらのトランスポート プロトコルには、SMTP、HTTP、ポイント ツー ポイント非同期通信、および物理メディア ベースのネットワーク トランスポートがあります。

iCalendar を使用すると、ユーザーはイベント、日付/時間依存のタスク、空き時間情報を電子メールで他のユーザーに共有できます。他のユーザーは返信できます。 iCalendar ファイルは、サフィックス「.ics」「.iCalendar」または「.ifb」を使用して保存され、MIME タイプは「text/calendar」です。 iCalendar は、トランスポート プロトコルに依存することなく、自立した状態に保たれています。 Web サーバー (HTTP プロトコルを使用) は iCalendar 情報を転送でき、Web ページには iCalendar を使用して埋め込み形式で iCalendar データを含めることができます。

## ICS ファイル形式の歴史

1998 年、Internet Engineering Task Force (IETF) は iCalendar を標準 (RFC 2445) として定義しました。この標準は、Frank Dawson (Lotus Notes Corporation) と Derik Stenerson (Microsoft) によって文書化されました。 2009 年に、標準は Bernard Desruisseaux (Oracle) によって RFC 5545 として再び洗練されました。今回は、いくつかの新しい機能が追加され、いくつかの古い機能が廃止されました。 2016 年に RFC 7986 がリリースされ、元の iCalendar RFC に拡張されました。 RFC 7986 はメインの VCALENDAR オブジェクトに新しい特性を追加し、新しいサポート機能も会議システムに導入されました。

## ICS ファイル形式 ##

iCalendar のデータが使用する MIME タイプは「text/calendar」です。 iCalendar のデフォルトの文字セットは UTF-8 ですが、MIME でパラメーターを指定することにより、別の文字セットを使用できます。 iCalendar ファイルにはセクションが含まれており、これらのセクション「VCALENDAR」の中で、他のすべてのセクションをカプセル化するグローバル セクションです。 VEVENT セクションはイベントを定義し、VTODO はすべての ToDo 項目をリストし、VJOURNAL はジャーナル エントリを含み、VTIMEZONE はタイム ゾーンの情報を指定します。同様のカテゴリの複数のセクションが許可されます。多数のイベントの場合、複数の VEVENT セクションが iCalendar ファイルに存在する可能性があります。

### コンテンツ行 ###

iCalendar オブジェクトは、個別のテキスト行「コンテンツ行」に配置されます。このファイル形式では、CRLF シーケンスが行を終了しますが、行の長さは改行を除いて 75 オクテットに制限されます。長いデータ項目は、多くの行にまたがることができます。

### リストとフィールド区切り記号 ###

プロパティとパラメータは、COMMA 文字で区切られた値のリストを指定します。引用符で囲まれた文字列は、URI ベースのパラメーター値に使用されます。パラメータのリストは、プロパティ値によって構築できます。このリストの各プロパティ パラメータは、セミコロンで区切る必要があります。

値リストでは、セミコロンはプロパティ パラメータを分離し、COMMA はプロパティ値を分離します。以下に例を示します。

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### 複数の値

一部のプロパティは、複数の値を持つことができます。プロパティ名を使用して新しいコンテンツ行を単純に生成することが、多値プロパティの基本ルールです。ただし、複数の言語バリエーションを持つ単一の値では、複数値のプロパティを使用してはなりません。

### バイナリ コンテンツ

iCalendar オブジェクト内で、プロパティ値は、URI を使用して外部 MIME エンティティに配置されたバイナリ コンテンツ データを参照できます。インライン バイナリ コンテンツは、アプリケーションが iCalendar オブジェクトを単一のエンティティとして表現する必要がある "ENCODING" パラメータを使用した特別な状況で使用できます。次の例では、URI 参照を使用して「ATTACH」プロパティを説明しています。

添付: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

＃＃＃ キャラクターセット

iCalendar のデフォルトの文字セット スキームは UTF-8 ですが、プロパティ値の文字セットを定義するプロパティ パラメータは指定されていません。 MIME 転送では、「charset」パラメータを既存の文字セットに使用する必要があります。

## 参考文献

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

