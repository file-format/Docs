{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - 확장 가능한 아카이브 파일 형식",
  "description":"XAR 파일을 만들고 열 수 있는 XAR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## .XAR 파일이란?

.xar(Extensible Archive Format) 확장자를 가진 파일은 압축되거나 압축되지 않은 형식일 수 있는 UNIX 아카이브입니다. 패키지 설치를 위해 Mac OS에서도 사용됩니다. XAR은 오픈 소스이며 Safari 브라우저와 함께 사용하기 위해 Mac OS X 10.5의 일부입니다.

## XAR 파일 형식

[XAR](https://github.com/mackyle/xar/wiki/xarformat) 파일에는 세 가지 주요 영역이 있습니다.

* 헤더
* 목차
* 힙

### XAR 헤더

XAR 헤더는 다음과 같이 구성됩니다.

|필드|데이터 유형|바이트 단위 크기|
---|---|---|
|Magic|부호 없는 Int 32|4|
|크기|부호 없는 정수 16|2|
|버전|부호 없는 정수 16|2|
|TOC 길이 압축|부호 없는 Int 64|8|
|압축되지 않은 TOC 길이|부호 없는 Int 64|8|
|체크섬|부호 없는 정수 32|4|
|메시지 다이제스트 이름 |널 종료됨||

XAR 헤더의 C 구조는 다음과 같이 정의할 수 있습니다.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
헤더의 모든 필드(magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg)는 항상 네트워크 바이트(빅 엔디안) 순서로 XAR 파일에 저장됩니다.

### XAR 목차(TOC)

목차는 UTF-8로 인코딩되어야 하는 XML 문서입니다. 파일 시작 부분에 저장되므로 아카이브를 스캔하여 개별 파일을 쉽게 추출할 수 있습니다. XAR 아카이브를 사용하면 [GZIP](/ko/compression/gz/), [BZIP2](/ko/compression/bz2/) 및 기타 유사한 압축 체계를 사용하여 아카이브의 개별 파일을 독립적으로 압축/인코딩할 수 있습니다.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### 힙

힙은 압축된 toc 직후에 시작됩니다. TOC에서 참조하는 구조화되지 않은 데이터 힙입니다. TOC에 나열된 오프셋 값은 힙의 시작 부분에서 시작합니다. toc의 길이 값은 힙에 저장된 실제 바이트 수(압축 여부)를 나타내는 반면 크기 값은 항목의 추출된 크기(필요한 경우 압축 해제 후)를 나타냅니다.

## 참고문헌

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - 위키백과](https://en.wikipedia.org/wiki/Xar_(archiver))

