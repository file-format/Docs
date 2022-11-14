{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "파일", "확장자", "파일 형식", "mrc 구현", "프로그래밍 가이드", "mrc 예제", "mIRC", "mIRC 스크립팅 언어", "INI 파일", " mSL 스크립팅 언어", "mIRC 언어", "mIRC 스크립트", "스크립팅 언어"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC 스크립트 언어 파일",
  "description":"MRC 파일을 만들고 열 수 있는 MRC 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## .MRC 파일이란?

mIRC는 Windows 운영 체제에 IRC 클라이언트(Internet Relay Chat)로 내장된 스크립팅 언어입니다. 개인 및 채널 사용을 위한 스팸 방지 기능을 제공합니다. 사용자 호환성에 대한 더 나은 경험을 제공하기 위해 이 mIRC 스크립팅 언어를 사용하여 대화 창을 만들 수 있습니다. 스크립트가 포함된 파일은 대부분 일반 텍스트 형식으로 MRC 확장자로 저장되거나 [INI](/ko/system/ini/) 파일로 저장됩니다. 이 언어의 기능을 명령 및 식별자(값을 반환할 때)라고 합니다.

mIRC 언어는 한 번에 여러 스크립트 파일을 로드할 수 있습니다. 반면에 한 파일로 인해 동시에 로드될 때 다른 파일이 더 이상 사용되지 않을 수 있습니다. 명령이 저장되고 자동으로 IRC에 존재할 수 있습니다. 이 언어에서 사용되는 명령과 별칭은 문자의 우선 순위를 구성하지 않습니다.

mIRC는 봇이 채널을 자동으로 관리하도록 하는 데 널리 사용되지만 mSL 스크립팅 언어로도 수정할 수 있습니다. 매크로, 음악 재생 기능, 작은 매크로 및 기능, 기본 게임 또는 작은 응용 프로그램 작동과 같은 많은 새로운 기능을 도입할 수 있습니다.


## 간략한 역사 ##

이 스크립팅 언어는 Khaled Adam Bey가 1995년에 처음 개발했습니다. 스크립팅 언어의 디자인도 Khalid에 의해 만들어졌습니다. 이 언어의 목표는 이벤트 중심 프로그래밍이었습니다. 처음에 이 프로그래밍 언어의 파일에 사용된 파일 확장자는 .mrc 및 .ini였습니다. 또한 독점 소프트웨어의 라이선스 하에 개발되었습니다.

## 기술 사양 ##

일부 기능은 이 mIRC 언어를 통해 사용자 지정 스크립팅되며 별칭으로 알려져 있습니다. 이러한 별칭이 값을 반환할 때 맞춤 식별자라고 합니다. 이 mIRC 언어에 포함된 모든 변수는 동적으로 유형이 지정됩니다. 인장은 mIRC 스크립트에서 사용됩니다. 이 스크립팅 언어의 또 다른 기능은 팝업입니다. 사용자는 단순히 팝업을 선택하여 호출할 수 있습니다. 리모컨은 특정 이벤트에 지정됩니다. 상대 이벤트가 발생하면 리모컨이 호출됩니다.

공백으로 구분된 토큰은 이 언어의 각 코드 줄을 구분하는 데 사용됩니다. MDX(mIRC Dialog Extension) 및 DCX(Dialog Control Extension)와 같은 mIRC 파일에 사용되는 다른 인기 있는 확장자가 있습니다. 둘 다 대화 확장이며 비교적 인기가 있습니다. 언어 구성은 이 스크립팅 언어의 명명법에 의해 참조됩니다. mIRC 언어는 지역 및 전역 변수, 이진 변수, 해시 테이블 및 파일 처리와 같은 스크립팅 언어의 다양한 측면을 포함합니다.


## MRC 파일 형식 예 ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/ko/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## 참조 ##

* [MIRC - Wikipedia 제공](https://en.wikipedia.org/wiki/MIRC_scripting_language)



