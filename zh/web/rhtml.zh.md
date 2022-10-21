{
  "date" : "2021-05-24",
  "keywords" :["rhtml","rhtml文件","rhtml文件格式","rhtml文件类型","文件","类型","什么是rhtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML 页面",
  "description":"了解 RHTML 文件格式和可以创建和打开 RHTML 文件的 API。",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## 什么是 .rhtml 文件？

带有 .rhtml 扩展名的文件是包含 Ruby 代码或脚本的服务器端 [HTML](/zh/web/html/) 文件。代码使用后端运行的 Ruby on Rails 在服务器上执行。对于那些不了解 Ruby on Rails 的人来说，它是一个全栈框架，用于基于 Model-View-Control 模式使用后端数据库开发 Web 应用程序。简单地说，RHTML 是 HTML 和 Ruby 的组合，其中 Ruby 脚本/编程的强大功能可供使用 HTML 标签的 Web 开发人员使用。

## RHTML 文件格式

RHTML 文件像任何其他基于文本的 Web 文件一样以纯文本格式编写。要执行的代码包含在 `<% %>` 中，而对于输出，代码写在 `<%= %>` 语句中。

## RHTML 示例

以下示例使用 HTML 和 Ruby on Rails 的最简单组合从产品列表中输出每个产品的名称。
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## 参考

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

