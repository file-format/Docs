{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml 파일", "rhtml 파일 형식", "rhtml 파일 형식", "파일", "유형", "rhtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - 루비 HTML 페이지",
  "description":"RHTML 파일을 만들고 열 수 있는 RHTML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .RHTML 파일이란?

확장자가 .rhtml인 파일은 Ruby 코드 또는 스크립트가 포함된 서버측 [HTML](/ko/web/html/) 파일입니다. 코드는 백엔드에서 실행되는 Ruby on Rails를 사용하여 서버에서 실행됩니다. Ruby on Rails에 대해 모르는 사람들을 위해 Model-View-Control 패턴을 기반으로 하는 백엔드 데이터베이스로 웹 애플리케이션을 개발하기 위한 풀 스택 프레임워크입니다. 간단히 말해서, RHTML은 HTML 태그를 사용하여 웹 개발자가 Ruby 스크립팅/프로그래밍의 기능을 사용할 수 있는 HTML과 Ruby의 조합입니다.

## RHTML 파일 형식

RHTML 파일은 다른 텍스트 기반 웹 파일과 마찬가지로 일반 텍스트 형식으로 작성됩니다. 실행할 코드는 `<% %>`로 묶고, 출력을 위해서는 `<%= %>` 문 안에 코드를 작성한다.

## RHTML 예제

다음 예제에서는 HTML과 Ruby on Rails의 가장 간단한 조합을 사용하여 제품 목록에서 각 제품의 이름을 출력합니다.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## 참고문헌

* [튜토리얼 포인트 - 루비 온 레일즈](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

