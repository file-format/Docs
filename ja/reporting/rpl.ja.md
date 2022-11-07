{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - レポートのページレイアウト",
  "keywords" :[ "rpl", "レポート ページ レイアウト", "XSD", "SQL Server", "レポート"],
  "description":"ビューア コントロールとの接続時に Microsoft SQL Server Reporting Services によって使用される内部バイナリ形式である RPL ストリーム形式について学びます。",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## .RPL オプション番号##

RPL (レポート ページ レイアウト) ストリーム形式は、サーバーからクライアント ビューアー コントロールへのレンダリング作業の一部を削減するためにビューアー コントロールと通信するときに、MS SQL Server Reporting Services によって使用される内部バイナリ形式です。開発者は、RPL を生成する RPL を使用してカスタム レポート デザイナーを作成したり、RPL ファイルを処理および表示してレポートを表示するカスタム レポート レンダラーを作成したりできます。

## RPL 構造

RPL ストリームには、ストリーム構造、レポート構造、レポート プロパティ、および列挙が含まれます。すべての構造には次のものが含まれます。

- 構造の定義。

- 構造の拡張バッカスナウア形式 (ABNF) 文法。

- 構造のビット図。

- 構造内に含まれるすべてのフィールドの定義。

以下は、RPL 構造の一部に関する簡単なメモです。

### ストリーム構造
ストリーム構造は、一連のレコードで構成されます。レコードには、レポート レイアウトを含む 0 個以上の構造化フィールドが含まれます。

#### RPL ストリーム
RPL ストリームにはレポート レコードが 1 つだけ含まれている必要があり、ストリームはレポート階層を保持する一連のバイナリ レコードである必要があります。

＃＃＃＃ 記録
レコードは、レポートに関する情報を保持するために使用される基本的な構成要素です。レコードは、可変長の一連のバイトで構成されます。レコードは、次の 2 つのコンポーネントで構成されます。
- レコード タイプ
- そのレコード タイプに固有のレコード データ。
レコード タイプは、レコードによって指定される情報のタイプと、レコードに関連するレコード データの構造がどのように順序付けられ、構造化されるかを定義する 1 バイトです。レコードの値は、そのレコードに固有のデータのタイプによって異なります。

#### 単純なデータ型構造

次の表は、RPL ストリームのデータ型を定義しています。

|説明|フォーマット|
---|---|
|Char|16 ビット (2 バイト) の数値 (序数) を表します。|
|Byte|8 ビット (1 バイト) の符号なし整数を表します。
|Int16|16 ビット (2 バイト) の符号付き整数を表します。|
|Single|32 ビット (4 バイト) の単精度浮動小数点値を表します。|
|Decimal|128 ビット (16 バイト) のデータ型を表します。|
|DateTime|日付と時刻の値の 64 ビット (8 バイト) エンコードを表します。|
|Int64|64 ビット (8 バイト) の符号付き整数を表します。|
|Int32|32 ビット (4 バイト) の符号付き整数を表します。|
|Float|32 ビット (4 バイト) の単精度浮動小数点値を表します。|
|Boolean|8 ビット (1 バイト) の論理ブール型の値を表します。有効な値は true (1) と false (0) です。|
|Long|64 ビット (8 バイト) 符号付き整数を表します。|
|文字列|プロトコル内のすべての文字列値は UNICODE UTF-16 でなければなりません。デフォルトでは、すべての文字列値は、文字列の長さを定義する整数で始まります。文字列値は、プロトコルではバイト配列として表されます。バイト数は、文字列内の文字数の 2 倍に等しくなければなりません。|

### レポートの構造
レポート構造には、関連する構造と要素の定義とサイズが含まれます。

次のリストは、レポートの構造を示しています。

- 報告
- バージョン
- レポートのプロパティ
- オフセット配列要素
- ページ コンテンツ
- ページ
- ページのプロパティ
- ページレイアウト
- セクション
- 単純なセクション
- 混合セクション
- セクション プロパティ
- ボディエリア要素
- ページヘッダー要素
- ページ フッター要素
- 体の要素
- 要素のプロパティ
- 共有要素のプロパティ
- 共有要素のプロパティを使用
- InlineSharedElementProperties
- NonSharedElementProperties
- スタイル
-SharedStyleProperties
- NonSharedStyleProperties
- アクション情報
- ActionInfoContent
- アクション
- ActionImageMapAreas
- ActionInfoWithMaps
- 動的画像データ
- ImageConsolidationOffsets
- レポートアイテム
- ライン
- 画像
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- 画像データ
- イメージマップエリア
- イメージマップエリア
- チャート
- ゲージパネル
- 地図
- 長方形
- サブレポート
- リッチテキストボックス
- 段落内容
- テキストラン
- 段落
- リッチテキストボックス構造
- タブリックス
- TablixContent
- Tablix構造
- TablixMeasurements
- 列幅
- 列情報
- 行の高さ
- 行情報
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- 測定
- 計測
- ReportElementEnd

＃＃＃ プロパティ
以下は、RPL ストリームで使用できるプロパティのリストです。

- ID
- 列数
- 列間隔
- ユニークな名前
- 名前
- ラベル
- ブックマーク
- ツールチップ
- トグルアイテム
- 説明
- 位置
- ConsumeContainerWhiteSpace (RPL 10.6)
- 言語
- 実行時間
- 著者
- 自動更新
- レポート名
- ページの高さ
- ページ幅
- マージントップ
- マージン左
- マージンライト
- マージンボトム
- 列
- ページ名 (RPL 10.6)
- スラント
- CanGrow
- CanShrink
- 価値
-トグルステート
- 並べ替え可能
-SortState
- 方式
- IsToggleParent
- タイプコード
- 元の値
- IsSimple
-コンテンツオフセット
- ストリーム名
- サイジング
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- イメージMIMEタイプ
- 画像名
- 幅
- 身長
- 水平解像度
- 垂直解像度
-RawFormat
- ハイパーリンク
- ブックマークリンク
- ドリルスルー ID
- ドリルスルー URL
- ボーダの色
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- ボーダースタイル
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- ボーダー幅
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- 右パディング
- パディングトップ
- PaddingBottom
- フォントスタイル
- フォントファミリー
- フォントサイズ
- フォントウェイト
- フォーマット
- テキスト装飾
- テキストアライン
- 垂直整列
- 色
- 行の高さ
- 方向
- 書き込みモード
- UnicodeBiDi
- 背景画像
- 背景色
- バックグラウンドリピート
- NumeralLanguage
- 数値バリアント
- カレンダー
- ColumnHeaderRows
- RowHeaderColumns
-ColsBeforeRowHeader
- レイアウト方向
- 定義パス
- レベル
- MemberCellIndex
- CellItemOffset
-ColSpan
- 行スパン
- DefIndex
- 列インデックス
- 行インデックス
- グループラベル
- RecursiveToggleLevel
- リストスタイル
- リストレベル
- 段落番号
- 右インデント
- 左インデント
- ハンギングインデント
- スペースビフォア
- スペースアフター
- ファーストライン
- マークアップ
- コンテンツトップ
- コンテンツレフト
- コンテンツ幅
- コンテンツの高さ
- 州
- CellItemState
- MemberDefState

### 列挙
次のリストは、RPL ストリームで使用できる列挙を示しています。

- ソートオプション
- サイジング
- 形状タイプ
- ImageRawFormat
- フォントスタイル
- FontWeights
- テキストデコレーション
- TextAlignments
- VerticalAlignments
- 方向
- 書き込みモード
- UnicodeBiDiTypes
- カレンダー
- ボーダースタイル
- BackgroundRepeatTypes
- リストスタイル
- マークアップ スタイル
- タイプコード
- 状態値
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLサイズ





## 参照 ##

- [レポート ページ レイアウト (RPL) バイナリ ストリーム形式](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

