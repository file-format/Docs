{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"B3D 파일 형식에 대해 알아보세요. B3D 파일을 열고 생성할 수 있는 blitz3d 게임 및 API에 사용됩니다.",
  "title" :"B3D - Blitz3D 엔티티 모델 파일",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## .B3D 파일이란?

확장자가 .b3d인 파일은 캐릭터, 건물, 지형 및 기타 개체에 대한 비디오 게임 모델을 포함할 수 있는 Blitz3D에서 사용하는 모델 파일입니다. Blitz3D는 **blitz3d 게임**을 만드는 데 사용되는 프로그래밍 언어입니다. Blitz3D는 비디오 게임 작성만을 목적으로 설계된 강력하고 유연하며 사용하기 쉬운 프로그래밍 언어입니다. 개발자는 Blitz3D를 사용하여 액션으로 가득 찬 3D 게임, 2D 퍼즐, 모험, RPG 등 무엇이든 만들 수 있습니다.

Blitz3D는 BASIC 프로그래밍 언어를 기반으로 합니다. 또한 배우고 사용하기 쉽습니다. 이러한 모든 사실은 Blitz를 초보자와 숙련된 프로그래머 모두에게 이상적으로 만듭니다. 이 기능은 대부분의 최신 3D 엔진에서 볼 수 있는 것보다 다소 구식으로 간주되지만 Blitz3D는 전 세계적으로 많은 게임 프로그래머가 계속 사용하고 있습니다.

## Blitz3D의 간략한 역사

Blitz3D는 기본적으로 다른 유사한 게임 개발 언어와 경쟁하기 위해 2001년 9월 Microsoft Windows 운영 체제용으로 출시되었습니다. Blitz3D는 DirectX 7 기반 3D 엔진용 API를 추가하여 명령 집합을 확장한 이전 2D 엔진 BlitzBasic보다 업그레이드된 버전입니다. Blitz3D 사용자는 BlitzBasic의 최신 엔진인 BlitzMax도 비교해야 합니다. BlitzMax는 객체 지향 프로그래밍 언어를 지원하는 Blitz3D의 복잡하지만 더 강력한 버전입니다. 유니코드 문자, OpenGL, Windows 대신 OSX 및 Linux로 내보내기에 더 적합하도록 업데이트된 그래픽 API입니다.

## B3D 예
1개의 TEXS 청크, 1개의 BRUS 청크 및 1개의 NODE 청크를 포함하는 b3d 파일은 다음과 같습니다.

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
단순하고 애니메이션이 없고 질감이 없는 메시는 다음과 같습니다.

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## 참고문헌
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [블리츠 베이직](https://en.wikipedia.org/wiki/Blitz_BASIC)

