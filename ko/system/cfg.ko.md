{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "확장", "파일", "형식", "시스템", "구성", "설정", "프로그램", "컴퓨터", "응용 프로그램"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - 파일 형식",
  "description":"CFG 파일 형식과 CFG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .CFG 파일이란? ##

확장자가 .cfg인 파일은 일종의 "설정" 파일입니다. 널리 사용되는 파일 형식이며 컴퓨터 프로그램의 구성 및 설정에 관한 정보를 저장하는 데 사용됩니다. 대부분의 CFG 파일 유형은 텍스트 형식으로 저장되며 수동으로 열지 말고 텍스트 편집기를 사용하여 열어야 합니다. 그러나 정보가 저장되는 형식이 다른 여러 유형의 CFG 파일이 있습니다. CFG 파일이 제공하는 기능은 응용 프로그램마다 다릅니다. 일부 컴퓨터 응용 프로그램은 사용자가 그래픽 간섭을 사용하여 구성 파일 구문을 수정하거나 개발할 수 있도록 하는 반면, 다른 응용 프로그램은 텍스트 편집기를 사용한 수정만 허용합니다. 이러한 파일을 수정한 후 사용자는 응용 프로그램에 이 파일을 다시 읽고 수정 사항을 시스템에 적용하도록 지시할 수 있습니다.


## CFG 파일 형식 ##

CFG 파일은 Unix 및 Unix 계열 운영 체제, MS-DOS, macOS, Microsoft Windows 및 IBM OS/2와 같은 다양한 운영 체제에서 지원됩니다. 이러한 파일이 저장되고 각 운영 체제에서 사용되는 형식은 다릅니다. 대부분의 시스템은 이러한 파일을 사람이 읽을 수 있고 편집 가능한 일반 텍스트 형식으로 사용하고 저장하는 반면, 다른 시스템은 파일 사용 및 운영 체제의 요구 사항에 따라 더 복잡한 형식으로 저장합니다.

Unix 및 Unix 계열 운영 체제에서 대부분의 CFG 파일은 CFG 파일에 대해 여러 가지 다른 형식 스타일이 사용되지만 가장 일반적인 형식은 쉽게 읽을 수 있는 일반 텍스트 형식이며 거의 모든 형식에서 주석을 만들고 편집할 수 있습니다. 이러한 운영 체제에서 CFG 파일의 가장 일반적인 파일 확장자는 CNF, CONF, CF 및 INI입니다.

MS-DOS 운영 체제에는 처음에 하나의 구성 파일 형식, 즉 일반 텍스트만 있었지만 MS-DOS 6과 함께 INI 구성 파일 형식이 도입되었습니다.

macOS는 표준 속성 목록 형식 스타일 구성 파일을 사용합니다.

Microsoft Windows에서 일반 텍스트 INI 스타일 구성 파일은 정보를 저장하고 편집하는 중요한 소스였으나 1993년에 새로운 데이터베이스 시스템이 도입되어 1993년 이후 Microsoft Windows에서 구성 파일 사용이 감소했습니다.


## CFG 예 ##

샘플 CFG 파일은 아래에서 볼 수 있습니다.

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
