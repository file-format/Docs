{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Age of Empires 2 Expansion Replay MGX 파일 형식과 MGX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"MII 파일 - Wii 가상 아바타 파일 형식",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## .MII 파일이란?

MII 파일은 Nintendo Wii 게임 콘솔에 가상 아바타를 저장하는 데 사용되는 가상 아바타 파일 형식입니다. 이 파일에는 아바타의 외모, 움직임 및 애니메이션과 같은 정보가 포함되어 있습니다. Wii의 게임, 소셜 네트워킹 애플리케이션 및 기타 소프트웨어에서 사용할 수 있습니다. MII 파일에는 성별, 머리 색깔, 피부색, 얼굴 특징 및 눈 유형과 같은 아바타에 대한 다른 기능도 포함되어 있습니다.

[My Avatar Editor](https://rc24.xyz/goodies/mii/)를 사용하여 MII 파일을 열 수 있습니다.

## MII 파일 형식

MII 파일 형식은 [Wii Brew](https://wiibrew.org/wiki/Mii_data)에 자세히 정의되어 있습니다. MII 파일의 문자열은 유니코드 형식(UTF-16), big-endian으로 저장됩니다.

### MI 블록

MII 파일 데이터는 Wiimote에 두 블록으로 저장됩니다. 각 블록의 길이는 750바이트이고 CRC는 2바이트이므로 총 752바이트입니다. 각 블록은 MII 파일 형식의 마법 같은 숫자인 4바이트 값('RNCD')으로 시작합니다.

## MII 파일을 만드는 방법?

Nintendo Wii용 아바타를 만드는 몇 가지 방법이 있습니다.

1. `Wii에 내장된 Mii 채널 사용:` 이 채널을 사용하면 얼굴 특징, 체형, 의상 등 다양한 도구를 사용하여 사용자 정의 아바타를 만들 수 있습니다. 아바타를 만든 후에는 Mii 파일로 저장하여 Wii의 게임 및 기타 소프트웨어에서 사용할 수 있습니다.

1. `닌텐도 3DS에서 Mii Maker 앱 사용하기:` Mii Maker 앱을 사용하면 Nintendo 3DS의 터치 스크린과 카메라를 사용하여 맞춤형 아바타를 만들 수 있습니다. 아바타를 만든 후에는 Mii 파일로 저장하고 무선 연결을 통해 Wii로 전송할 수 있습니다.

1. `타사 소프트웨어 사용:` 일부 개발자는 Wii용 맞춤형 아바타를 만들 수 있는 소프트웨어를 만들었습니다. 이 소프트웨어는 일반적으로 컴퓨터에서 사용하도록 설계되었으며 아바타를 Wii로 전송하려면 추가 단계가 필요할 수 있습니다.

1. `미리 만들어진 아바타 사용:` Wii의 일부 게임 및 기타 소프트웨어에는 사용할 수 있는 미리 만들어진 아바타가 함께 제공될 수 있습니다.

모든 경우에 Wii에서 아바타를 만들고 저장하려면 Nintendo 계정이 있어야 합니다.

## 참조

* [내 아바타 에디터](https://rc24.xyz/goodies/mii/)
* [Wii Brew](https://wiibrew.org/wiki/Mii_data)

