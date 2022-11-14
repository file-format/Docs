{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "확장자", "파일", "형식", "시스템", "Cold Fusion 마크업 언어", "언어", "CFM 웹 페이지", "CFML 엔진", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - 콜드 퓨전 마크업",
  "description":"CFM 파일 형식과 CFM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## .CFM 파일이란? ##

**Cold Fusion Markup Language**에서 사용되는 웹 페이지 및 파일은 CFM의 확장자를 포함하며 CFM 웹 페이지로 명명됩니다. 이 웹 개발 스크립팅 언어는 Google App Engine, .NET 프레임워크 및 JVM에서 실행됩니다. 프로그래밍 언어 또는 언어 코드를 포함할 수 있습니다. 사용자가 페이지에 액세스하면 ColdFusion의 웹 서버가 이를 실행합니다. JavaScript에 가까운 CFScript 또는 태그를 사용하여 CFML을 작성할 수 있습니다. CFML은 [CSS](/ko/web/css/), [JavaScript](/ko/web/js/), [XML](/ko/web/)과 같이 [HTML](/ko/web/html/) 이외의 다른 언어를 생성하는 데 사용할 수 있습니다. xml/) 등이 있습니다.

이 언어와 지원하는 태그의 사용은 주로 동적 웹 응용 프로그램 개발에 있습니다. 응용 프로그램 개발 플랫폼의 오프라인 사용 중 오류가 발생하면 파일을 브라우저에서 온라인으로 직접 실행할 수 있습니다.
 

CFML은 CFML 엔진에 대한 처리를 위해 특정 서버 파일 확장자(.cfc, .cfm)가 제공되는 방식으로 작동합니다. 엔진이 Java를 기반으로 하는 경우 Java 서블릿을 사용하여 달성됩니다. CFML의 엔진은 기능과 태그만 처리하며 CFML 태그 외부의 기능과 텍스트를 변경 없이 웹서버에 반환한다.


## 간략한 역사 ##

1995년에 Allaire라는 회사에서 처음 만들었습니다. 2005년 Adobe가 인수하여 현재까지도 ColdFusion 개발 서비스를 제공하고 있습니다. 시간이 지남에 따라 많은 사람들과 회사에 의해 개발되고 업그레이드되었습니다. 2012년에는 OpenCFML이라는 재단이 출범했습니다. 나중에 2015년에 이전 Railo는 CFM의 성능을 개선하기 위해 서비스를 제공했으며 더 나은 기능을 위해 리소스를 줄였습니다. 최신 업데이트는 2020년에 출시되었으며 2028년까지 계속될 예정입니다.

## CFM 파일 형식 ##

CFM 파일 및 웹 페이지의 코드는 대부분 HTML과 같은 태그로 구성되지만 약간의 차이가 있습니다. 이러한 파일은 ColdFusion 스크립트에서 실행할 수 있는 다양한 작업을 수행하는 역할을 합니다.
* 이 파일은 모든 운영 체제의 브라우저를 사용하여 Windows 및 macOS에서 직접 액세스하고 실행할 수 있습니다.
* Adobe ColdFusion은 PC에서 웹 페이지 및 동적 응용 프로그램 개발을 위한 플랫폼을 제공합니다.
* 이러한 파일은 텍스트 기반이므로 메모장이나 운영 체제의 다른 텍스트 편집기와 같은 텍스트 편집기를 사용하여 이러한 파일을 열 수 있습니다.
* 텍스트 편집기에서 CFM 파일을 열면 웹 개발자가 아니면 이해할 수 없는 태그와 스크립트로 구성된 코드가 표시됩니다.

## CFM 사용 예 ##

다음은 간단한 사용 예 CFM 파일을 보여줍니다.

### CFM 문서 ###

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

## 참조 ##

- [CFM - 위키백과](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

