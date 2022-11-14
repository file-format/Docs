---
date: 2019-10-11
keywords: prc, .prc, prc 파일 형식, prc 파일을 여는 방법, .prc 확장자, prc 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC 파일 형식
linktitle: PRC
description: "PRC 파일 형식 및 PRC 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC 파일 형식
".prc" 확장자는 제품 표현 컴팩트 3D 파일 형식과 MobiPocket의 전자책 파일 형식에 사용됩니다.

## PRC(Product Representation Compact) 파일이란 무엇입니까?

PRC(Product Representation Compact)는 특히 CAD(Computer-Aided Design) 시스템에서 가져온 3D 데이터를 저장, 로드 및 표시하는 데 최적화된 3D 파일 형식입니다. 이식 가능한 방식으로 작성된 순차 바이너리 파일입니다. PRC를 사용하여 PDF 파일에 3D 데이터를 포함할 수 있습니다. PRC는 어셈블리 및 부품, 3D 엔티티의 트리, 정확한 지오메트리 표현, 삼각형 표현 및 마크업과 같은 대부분의 CAD 주요 구성을 지원합니다. PRC는 .prc 확장자를 사용하며 사용된 인터넷 미디어 유형은 *model/prc*입니다.

PRC는 용도에 따라 CAD 데이터를 직접 나타내기 위해 일반 압축을 사용하여 저장하거나 파일 크기를 줄이기 위해 고압축을 사용하여 저장할 수 있는 다목적 파일 형식입니다. PRC 형식을 사용하여 PDF에 저장된 3D 데이터는 CAM 및 CAE 응용 프로그램과 상호 운용 가능합니다.

### PRC(Product Representation Compact) 파일 형식 사양

PRC 파일은 하나의 메인 헤더 섹션과 하나 이상의 파일 구조, 마지막에 하나의 모델 파일을 가지고 있습니다. 파일 구조에는 하나의 헤더와 다음 데이터 섹션이 있습니다.

- **Globals**: 파일 구조의 각 트리 개체에 대한 참조된 파일 구조 및 색상, 선 스타일 및 좌표계를 포함합니다.
- **트리**: 제품 발생, 부품 정의, 표현 항목 및 마크업과 같은 항목의 트리에 대한 설명을 포함합니다.
- **테셀레이션**: 트리의 리프 엔터티(표현 항목 및 마크업)에 있는 테셀레이션된(삼각형) 모든 데이터를 포함합니다.
- **Geometry**: 트리의 리프 엔터티(표현 항목)의 모든 정확한 기하학 및 토폴로지 데이터를 포함합니다.
- **추가 기하학**: 기하학의 요약 데이터를 포함합니다. 이렇게 하면 전체 지오메트리를 로드하지 않고 파일을 부분적으로 로드할 수 있습니다.

다음은 일반적인 PRC 파일의 구조입니다.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## PRC 확장자를 가진 MobiPocket 전자 책 파일이란 무엇입니까?
**Mobipocket**이라는 프랑스 회사에서 도입한 전자책 파일 형식도 ".prc" 확장자를 사용하고 있습니다. 처음에 Mobipocket은 태블릿 PC, PDA 및 스마트폰과 같은 여러 스마트 장치를 위한 무료 응용 프로그램을 출시했습니다. ".prc" 확장자는 실제로 .mobi와 동일하지만 **.prc** 또는 **.pdb** 확장자만 지원하는 PDA에 특히 사용됩니다.

### Mobipocket PRC 파일 형식 사양
MobiPocket PRC 파일 형식은 XHTML을 사용하는 Open eBook 표준을 기반으로 하며 JavaScript 및 프레임을 포함할 수도 있습니다. 내장 데이터베이스와 함께 사용할 기본 SQL 쿼리에 대한 지원도 제공됩니다.

Mobipocket Reader에는 홈페이지 라이브러리가 있습니다. 독자는 책의 어느 부분에나 빈 페이지를 삽입하고 다양한 그림을 추가할 수 있습니다. 주석, 책갈피, 수정, 메모 및 그림과 같은 개체를 한 곳에서 관리할 수 있습니다. 이미지는 GIF 형식으로 변환되며 최대 크기는 64K로 화면이 작은 휴대폰에 충분합니다. Mobipocket Reader에는 전자 책갈피와 사전이 내장되어 있습니다.

리더에는 많은 PDA, 커뮤니케이터 및 스마트폰에 대한 읽기 및 지원을 위한 전체 화면 모드가 있습니다. Mobipocket 제품은 대부분의 Palm 운영 체제, Windows, Symbian, BlackBerry를 지원하지만 Android는 지원하지 않습니다. 리더는 WINE을 사용하는 Linux 또는 Mac OS X에서 작동합니다.

## 참고문헌

- [중국 - 위키백과](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC 형식 사양](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [전자책 형식 비교 - 위키피디아 제공](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

