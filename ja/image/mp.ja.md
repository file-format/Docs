{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP ファイル - LaTeX MetaPost ファイル",
  "description":"MP ファイル形式と,MP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## .MP ファイルとは何ですか?

MP ファイルは、MetaPost プログラミング言語によって画像を作成するために生成されるベクター画像ファイルです。 MP ファイル形式を使用して作成されたベクター画像は、[EPS](/image/eps/) (Encapsulated PostScript) ファイルとして保存されます。さらに、MetaPost は TeX および Metafont フレームワークと共に配布され、これらのアプリケーションで使用される TEX および LTX ファイル内から MP ファイルを生成できます。 MP ファイルには、出力 EPS ファイルをレンダリングするための描画ステートメントと数学的アルゴリズム描画が含まれています。 PDFTex エンジンは、作成された EPS を使用して [PDF](/pdf/) ファイルを直接生成できます。

## MP ファイル形式

MP ファイルはバイナリ ファイルとしてディスクに保存され、出力ベクター イメージ ファイル形式にエクスポートすると EPS 出力が生成されます。 MetaPost を使用して作成された図面は、LaTex で作成された技術文書や雑誌の出版物内にフォーマットされた形式で含まれています。

### MetaPost MP ファイルの例

以下は、[Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) から参照された例で、矢印の中央のすぐ上に矢印と文字「A」が含まれています。矢印。

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## 参照 ##

* [ウィキペディアによる MetaPost](https://en.wikipedia.org/wiki/MetaPost)
* [Berkeley Educational Wiki による Latex サンプル メタポスト](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

