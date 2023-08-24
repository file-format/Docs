{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple 메일 파일 형식",
  "description":"EMLX 파일을 만들고 열 수 있는 EMLX 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .EMLX 파일이란?

EMLX 파일 형식은 Apple에서 구현 및 개발했습니다. Apple Mail 응용 프로그램은 이메일 내보내기에 EMLX 파일 형식을 사용합니다. EMLX 파일을 열고 다른 파일 형식으로 변환할 수 있는 다른 응용 프로그램도 있습니다.

## EMLX 파일 형식의 간략한 역사

Mac OS X 운영 체제는 NeXT가 NeXTSTEP 운영 체제의 일부로 만든 기존 이메일 프로그램인 NeXTMail을 채택했습니다. Apple은 NeXT를 인수한 후 기능을 향상시켰고 이제 기본 메일 클라이언트로 사용되는 Apple Mail 이메일 애플리케이션이 되었습니다. Apple Mail을 통해 내보낸 이메일은 EMLX 파일로 직접 저장됩니다. 또한 누군가 Mac OS를 두 번 클릭하여 EMLX 파일을 열 때 EMLX 파일의 기본 메일 클라이언트입니다.

## EMLX 파일 형식

EMLx 파일은 메모장과 같은 모든 텍스트 편집기에서 열 수 있는 간단한 텍스트 기반 파일입니다. EMLX 파일 구조는 세 부분으로 구성됩니다.

* 메시지의 바이트 수 - 0x0a로 끝나는 10진수로 ASCII로 작성된 메시지 자체의 길이
* 메시지 자체
* XML plist 형식의 메시지 메타데이터

Apple Mail에서 EMLX로 추출한 샘플 이메일을 따르고 텍스트 편집기에서 열면 이러한 내용을 더 잘 설명할 수 있습니다.

### EMLX 예제

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

이 예에서 875는 메시지의 총 길이를 보여줍니다. 메시지 메타데이터는<plist> 태그 및 플래그는 다음과 같이 설명됩니다.

|필드|설명|값
---|---|---|
|0|읽기|1 << 0
|1|삭제됨|1 << 1
|2|답변|1 << 2
|3|암호화|1 << 3
|4|플래그|1 << 4
|5|최근|1 << 5
|6|초안|1 << 6
|7|초기(더 이상 사용되지 않음)|1 << 7
|8|전달|1 << 8
|9|리디렉트|1 << 9
|10-15|첨부 개수|3F << 10(6비트)
|16-22|우선순위|7F << 16(7비트)
|23|서명|1 << 23
|24|정크입니다|1 << 24
|25|정크가 아님|1 << 25
|26-28|글꼴 크기 델타|7 << 26(3비트)
|29|정크 메일 수준 기록|1 << 29
|30|목차의 텍스트 강조|1 << 30
|31|(미사용)|

## 또한보십시오 ##

* [EML](/ko/email/eml/)
* [MSG](/ko/email/msg/)