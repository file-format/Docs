{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 파일",
  "description":"SP3 파일 형식과 SP3 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## .SP3 파일이란?

확장자가 .sp3인 파일은 궤도 정보를 저장하기 위한 NGS(National Geodetic Survey) 궤도 형식입니다. 이것은 NGS의 SP1 및 SP2 형식의 확장이며 궤도와 동시에 계산되는 위성 시계 보정 정보를 포함합니다. 주로 위치와 시계를 기반으로 하며 속도는 포함하지 않습니다. 형식은 1989년 Remondi에서 제안되어 1991년에 채택되었습니다. 위성 시계 보정 정보 외에도 궤도 정확도 지수, 주석 행, GPS 주 및 첫 번째 에포크와 관련된 주의 초와 같은 정보가 포함됩니다. SP3 파일은 Wolfram Research Mathematica로 열 수 있습니다.

## SP3 파일 형식 - 추가 정보

SP3 파일은 ASCII 파일 형식으로 디스크에 저장되며 그 내용은 보기 위해 모든 텍스트 편집기에서 열 수 있습니다. SP3 파일의 구조는 다음 이미지에서 볼 수 있습니다.

{{< figure src="../sp3-file-format.png" title="" >}}

## 참고문헌

* [확장 표준 제품 3 궤도 형식(SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20구조)
* [국가 측지 측량 표준 GPS 궤도 형식 확장](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

