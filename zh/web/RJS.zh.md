{
  "date" : "2021-05-24",
  "keywords" :["rjs","文件","扩展名","文件格式","文件扩展名","RJS","Ruby Javascript文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript 文件",
  "description":"了解什么是 RJS 文件格式以及可以创建和打开 RJS 文件的 API。",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## 什么是一 .rjs 文件？

带有 .rjs 扩展名的文件是 Ruby 代码和 JavsScript 的组合，它允许 Rails 开发人员使用 Ruby 生成动态 JavaScript 代码。 Ruby 代码嵌入在 Java 函数中，并在需要 Ruby 引擎在服务器上运行的 Web 服务器上编译。 RJS 类似于 [RHTML](/zh/web/rhtml/)；唯一的区别是横向包含 [HTML](/zh/web/html/) 中的 Ruby 代码，而它包含 Javascript 函数中的 Ruby 代码。

## RJS 文件格式

RJS 文件像任何其他脚本或编程语言一样以纯文本编码。当客户端请求这样的页面时，Ruby 代码在服务器上执行，只有 HTML 和 Javascript 代码返回到客户端的浏览器。 RJS 文件的语法类似于 Ruby 和 JavaScript 语法的组合，只有 Ruby 代码嵌入在 JavaScript 函数中。

### RJS 示例

下面的例子展示了一个独立的简单 Ruby 代码，然后嵌入到一个 JavaScript 函数中。

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
以下是RubyJS：
```Ruby
# here you go!

foo = -> { "bar" }
```
## 参考

* [RJS](https://github.com/makevoid/rjs)

