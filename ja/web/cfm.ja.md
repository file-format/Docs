{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "拡張子", "ファイル", "フォーマット", "システム", "Cold Fusion マークアップ言語", "言語", "CFM Web ページ", "CFML エンジン", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - 常温核融合マークアップ",
  "description":"CFM ファイル形式と,CFM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## .CFM オプション番号##

**Cold Fusion Markup Language** で使用される Web ページとファイルには、CFM の拡張機能が含まれており、CFM Web ページと呼ばれています。この Web 開発スクリプト言語は、Google App Engine、.NET フレームワーク、および JVM で実行されます。プログラミング言語または言語のコードを含めることができます。そのページのいずれかにユーザーがアクセスすると、ColdFusion の Web サーバーがそのページを実行します。 CFScript (JavaScript に近い) またはタグを使用して CFML を記述できます。 [CSS](/web/css/)、[JavaScript](/web/js/)、[XML](/web/) など、[HTML](/web/html/) 以外の言語を生成するために CFML を使用できます。 xml/) など。

この言語とそれがサポートするタグの使用は、主に動的 Web アプリケーションの開発に使用されます。アプリケーションの開発プラットフォームのオフライン使用中にエラーが発生した場合、ファイルはブラウザでオンラインで直接実行できます。
 

CFML は、CFML エンジンへの処理用に特定のサーバー ファイル拡張子 (.cfc、.cfm) が与えられるように機能します。エンジンが Java ベースの場合は、Java サーブレットを使用して実現されます。 CFML のエンジンは関数とタグのみを処理し、関数と CFML タグの外側のテキストを変更せずに Web サーバーに返します。


## 簡単な歴史 ##

1995 年に、Allaire という名前の企業によって最初に作成されました。 2005 年に Adobe が買収し、現在も ColdFusion を開発するためのサービスを提供しています。年月を経て、多くの人や企業によって開発およびアップグレードされました。 2012 年に、OpenCFML という名前の財団が発足しました。その後、2015 年に元 Railo がサービスを提供して CFM のパフォーマンスを改善し、リソースを減らして機能を改善しました。最新のアップデートは 2020 年に開始され、2028 年まで継続されることが発表されています。

## CFM ファイル形式 ##

CFM ファイルと Web ページのコードは、ほとんどが HTML のようなタグで構成されていますが、わずかな違いがあります。これらのファイルは、ColdFusion スクリプトが実行できるようにするさまざまな操作の実行を担当します。
* これらのファイルは、任意のオペレーティング システムのブラウザを使用して、Windows と macOS の両方で直接アクセスして実行できます。
* Adobe ColdFusion は、PC 上で Web ページおよび動的アプリケーションを開発するためのプラットフォームを提供します。
* これらのファイルはテキストベースであるため、メモ帳などのテキスト エディタやオペレーティング システムのその他のテキスト エディタを使用してこれらのファイルを開くことができます。
* CFM ファイルをテキスト エディターで開くと、Web 開発者でなければ理解できないタグとスクリプトで構成されるコードが表示されます。

## CFM の使用例 ##

以下に、CFM ファイルの簡単な使用例を示します。

### CFM ドキュメント ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## 参照 ##

- [CFM - ウィキペディア](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

