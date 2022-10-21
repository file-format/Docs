{
  "date" : "2022-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BR 文件 - Brotli 压缩文件格式",
  "description":"了解 BR 文件格式和可以创建和打开 BR 文件的 API。",
  "linktitle" : "BR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-20"
}

## 什么是一 .br 文件？

BR 文件是通过应用开源数据压缩算法 **Brotli** 生成的压缩 Web 文件。它用于存储网页资产，例如样式表 ([CSS](/zh/web/css/))、图像 ([SVG](/zh/image/svg/))、[XML](/zh/web/xml/) 和脚本文件（[JS]（/web/js/））。现代网站，如 Chrome 和 Firefox，使用 BR 文件来减少页面加载时间，从而带来更好的用户体验。

## BR 文件格式

BR 文件是使用 Brotli 压缩算法生成的压缩 Web 文件。 Brotli 压缩是一种无损数据压缩算法，是由 Google 开发的 Zopfli 压缩算法。它基于 LZ77 无损压缩算法和 Huffman 编码的组合。

由于其体积小，BR 文件被 Web 服务器和内容交付网络 (CDN) 使用。向这些服务器发出的请求会压缩 HTTP 内容，从而加快网站加载速度。 Brotli 变得更流行并且提供比 gzip 更好的压缩。

## 参考

* [Brotli - 维基百科](https://en.wikipedia.org/wiki/Brotli)

