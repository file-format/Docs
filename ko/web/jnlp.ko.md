---
date: 2022-07-30
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP 파일 형식 - JNP 파일이란 무엇입니까?
linktitle: JNLP
description: "JNLP 파일 형식과 JNLP 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## .JNLP 파일이란?

JNLP 파일은 네트워크를 통해 Java 프로그램을 시작하기 위한 XML 정보가 포함된 JWS(Java Web Start) 파일입니다. JNLP(Java Network Launching Protocol) 형식으로 저장됩니다. 응용 프로그램을 다운로드하고 실행하기 위한 응용 프로그램 배포 기술인 JWS(Java Web Start) 기술에서 사용합니다. JNLP 파일에는 프로그램이 다운로드되고 로컬 시스템에서 실행되는 서버의 원격 주소가 포함됩니다.

## JNLP 파일 형식 - 추가 정보

JNLP 파일은 사람이 읽을 수 있는 텍스트 형식으로 저장된 **[XML](/ko/web/xml/)** 파일로 저장됩니다. XML 파일에는 네트워크를 통해 Java 응용 프로그램을 시작하고 실행하는 데 사용되는 정보가 있습니다. JWS를 사용하면 웹 페이지 링크를 클릭하여 응용 프로그램을 시작할 수 있습니다. 응용 프로그램이 사용자 컴퓨터에 아직 다운로드되지 않은 경우 다운로드됩니다.

Oracle은 JSE(Java Platform Standard Edition) 9 릴리스와 함께 JWS를 더 이상 사용하지 않습니다. 이에 따라 JNLP 파일은 더 이상 지원되지 않습니다.

### JNLP 파일을 여는 방법?

**JNLP 파일을 열 수 있는** 응용 프로그램은 **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** 및 *를 포함합니다. *깃허브 아톰**.

### JNLP 파일 예

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**용법**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## JNLP 파일을 실행하는 방법?

JWS의 사용 중단으로 인해 JWS 기술을 기반으로 개발된 애플리케이션은 최신 버전의 Java에서 실행할 수 없습니다. 그러나 이러한 JNLP 기반 프로그램은 Java Web Start 기술의 오픈 소스 재구현인 OpenWebStart를 사용하여 실행할 수 있습니다. 최신 버전의 Java와 병렬로 설치되며 Java Web Start 및 JNLP 표준에서 가장 일반적으로 사용되는 기능을 제공합니다.

## 참조 ##

* [자바 웹스타트란 무엇이며 어떻게 시작하나요?](https://www.java.com/en/download/help/java_webstart.html)
* [최신 자바 버전으로 JNLP 실행](https://openwebstart.com/)
* [자바 웹 스타트 - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

