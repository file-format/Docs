{
  "date" : "2021-07-29",
  "keywords" :["md5 文件","md5 文件格式","什么是 md5 文件","文件","md5 示例","md5 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 校验和文件",
  "description":"了解 MD5 文件和可以创建和打开 MD5 文件的 API。",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## 什么是 MD5 文件？

MD5 文件是用于验证文件完整性的校验和文件。它类似于关联文件的指纹，并且是使用使用文件中位数的算法唯一生成的。用于通过[md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html)等软件验证文件。使用 MD5 文件的优点之一是验证下载的文件没有损坏。

## MD5 文件格式 - 更多信息

通常，MD5 文件以与原始文件名相同的名称保存，但扩展名为 .md5。例如，如果关联的文件名为 `abc_987_123456.grb`，则对应的 MD5 文件名将是 `abc_987_123456.grb.md5`。 MD5 文件有助于识别接收或下载的文件没有损坏或受到恶意内容的影响。简而言之，MD5 文件保证了文件的完整性。


## 如何检查 MD5 校验和？

可以使用 [md5sum](https://en.wikipedia.org/wiki/Md5sum) 工具检查/验证单个文件的 MD5，如下所示。

```
md5sum -c abc_987_123456.grb.md5
```

## 参考

* [md5sum - 维基百科](https://en.wikipedia.org/wiki/Md5sum)

