{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "파일", "확장자", "파일 형식", "NUT рrоgrаmming 언어", "프로그래밍 가이드", "NUT 예제", "NUT 파일 형식", "다람쥐 언어", ".nut 확장자 파일 ", "NUT 파일"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - 다람쥐 언어 파일",
  "description":"NUT 파일 형식과 NUT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## .NUT 파일이란?

NUT는 NUT Open Container Format 파일을 나타냅니다. 이 NUT 파일 형식은 Squirrel로 알려진 프로그래밍 언어에 속합니다. 임베디드 시스템 및 비디오 게임에서 주로 사용되는 객체 지향, 고급 및 명령형 프로그래밍 언어입니다.

다람쥐 언어는 크기와 대역폭에 따라 쉽게 조정할 수 있는 경량 스크립팅 언어로 간주됩니다. 여기에는 자동 참조 카운팅 및 메모리의 가비지 관리의 이점이 포함됩니다.

다람쥐 언어의 구문은 C와 유사하고 스크립팅 언어의 기능을 포함하기 때문에 개발자를 끌어들입니다. 그러나 여전히 이러한 목적을 위해 널리 사용되는 다른 프로그래밍 언어에 비해 이점이 훨씬 적습니다.



## 간략한 역사 ##

2003년에 Alberto Demicelis에 의해 설계되었습니다. 그러나 이 언어의 안정적인 버전이 2016년에 릴리스되었습니다. zlib/libpng의 라이센스 하에 설계되었습니다. 2010년에 라이선스가 변경되어 MIT로 이전되었습니다. 이 언어는 [LUA](/ko/programming/lua/)(프로그래밍 언어)의 영감을 받은 버전으로 간주됩니다. Alberto가 더 유리하게 만들기 위해 디자인한 웹사이트에 이전 언어에 대한 제안 목록이 있습니다.


## 기술 사양 ##

다람쥐 언어의 기능과 사양은 여러 가지입니다. 동적 타이핑 기능, 위임 속성, 클래스 및 인터페이스의 여러 사용을 제공합니다. 이 언어의 구문은 C 언어의 구문과 유사합니다. Enduro/X(클러스터 응용 프로그램 서버)와 같은 응용 프로그램은 이 언어를 사용합니다. Squirrel은 비디오 게임에도 사용되기 때문에 OpenTTD, GTA IV 등이 있습니다.

언어의 안정적인 릴리스는 3.0.7입니다. MirthKit으로 알려진 툴킷은 Squirrel 프로그래밍 언어를 사용하여 2차원 게임을 위한 오픈 소스 및 교차 플랫폼을 제공합니다. 이 언어의 특성은 동적이며 [Python](/ko/programming/py/), LUA 등과 유사한 대부분의 기능이 있습니다. 여기에는 레지스터 기반 VM의 구현도 포함됩니다. Squirrel의 성능은 LUA에 비해 느립니다.

또 다른 ".nut" 확장자 파일 유형이 있으므로 파일 크기를 확인하여 어떤 NUT 파일이 있는지 확인해야 합니다. Squirrel 스크립트 NUT 파일은 대부분 1MB보다 작은 반면 비디오 NUT 파일은 일반적으로 크기가 1MB보다 큽니다.


## NUT 파일 형식 예 ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## 참조 ##

* [NUT - 위키피디아 제공](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



