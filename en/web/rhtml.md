{
  "date" : "2021-05-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RHTML - Ruby HTML Page",
  "description":"Learn about RHTML file format and APIs that can create and open RHTML files.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-24"
}

## What is an RHTML file?

A file with .rhtml extension is a server side [HTML](/web/html/) file that contains Ruby code or scripts. The code is executed on the server using the Ruby on Rails running at the backend. For those who don't know about Ruby on Rails, it is a full-stack framework for developing web applications with backend databases based on the Model-View-Control pattern. Simply said, RHTML is a combination of HTML and Ruby where the power of Ruby scripting/programming is available to web developers using HTML tags.

## RHTML File Format

RHTML files are written in plain text format like any other text-based web files. Code to be executed is enclosed within `<% %>` while for output, the code is written inside `<%= %>` statements.

## RHTML Example

The following example uses the simplest combination of HTML and Ruby on Rails to output the name of each product from a products list.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## References

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)
