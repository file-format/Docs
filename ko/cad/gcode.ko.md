{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE 파일 - .gcode 파일은 무엇이며 어떻게 열 수 있나요?",
   "description":"GCODE 파일 형식과 GCODE 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-ko",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## .GCODE 파일이란?

**GCODE 파일**은 컴퓨터 공작 기계 및 3D 프린터를 제어하기 위한 지침이 포함된 일반 텍스트 파일입니다. G 코드 또는 기하학적 코드는 **CNC(컴퓨터 수치 제어)** 기계의 움직임과 동작을 제어하는 데 사용되는 언어입니다. CNC 기계에는 밀링 머신, 선반, 라우터 및 3D 프린터가 포함됩니다.

G 코드 명령은 일반적으로 문자와 숫자로 구성된 특정 구문으로 작성됩니다. 각 명령은 도구를 특정 위치로 이동하거나 도구를 변경하거나 속도를 조정하는 등의 특정 작업을 수행하도록 기계에 지시합니다.

G 코드는 **CAM(Computer-Aided Manufacturing)** 소프트웨어에 의해 생성되는 경우가 많습니다. CAM 소프트웨어는 3D 모델 또는 2D 설계를 가져와 해당 도구 경로 및 G 코드 지침을 생성합니다. 그런 다음 G 코드 파일은 실행을 위해 CNC 기계 또는 3D 프린터에 로드됩니다.

G 코드 파일은 일반적으로 program.nc 또는 print.gcode와 같이 .nc 또는 .gcode 파일 확장자를 갖습니다.

## GCODE 파일 구조:

GCODE 파일은 각 줄에 특정 명령이 포함된 일반 텍스트 파일입니다. 이러한 명령은 기계의 움직임 제어부터 물체 제작에 중요한 온도, 속도 및 기타 매개 변수 조정에 이르기까지 다양합니다.

GCODE의 구문에는 문자와 숫자의 조합이 포함됩니다. 각각은 고유한 작업이나 매개변수를 나타냅니다. 일반적인 명령에는 이동을 위한 G0 및 G1, 스핀들 제어를 위한 M3 및 M5, 속도 및 이송 속도 조정을 위한 S 및 F가 각각 포함됩니다.

## GCODE 생성:

**Simplify3D** 및 **Slic3r**과 같은 슬라이싱 소프트웨어는 CAD(Computer-Aided Design) 도면을 GCODE로 변환합니다. CAD 소프트웨어는 3D 모델을 생성하는 데 사용되며, 이 모델은 STL과 같은 형식으로 내보내집니다. 슬라이싱 소프트웨어는 이러한 모델을 가져와 레이어 높이, 인쇄 속도 및 온도 설정과 같은 세부 사항을 지정하는 GCODE 파일을 생성합니다.

## GCODE 예

다음은 CNC 기계 이동을 위한 G 코드의 간단한 예입니다.

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## GCODE 파일을 여는 방법? .

G 코드 파일을 열려면 필요에 따라 다양한 유형의 소프트웨어를 사용할 수 있습니다.

3D 프린터용 G-코드를 생성한 경우 3D 프린터와 함께 제공되는 소프트웨어나 전용 슬라이싱 소프트웨어를 사용하여 열 수 있습니다. 예를 들면 **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** 또는 **Repetier-Host**가 있습니다. 이러한 프로그램에는 G 코드를 로드하고 시각화할 수 있는 사용자 친화적인 인터페이스가 있는 경우가 많습니다.

GCODE 파일은 일반 텍스트이므로 텍스트 편집기로 열 수 있습니다. 일반적인 텍스트 편집기에는 **메모장(Windows)**, **TextEdit(macOS)** 또는 **Gedit(Linux)**이 포함됩니다. G 코드 파일을 **마우스 오른쪽 버튼으로 클릭**하고 **다음으로 열기**를 선택한 다음 텍스트 편집기를 선택하세요.

