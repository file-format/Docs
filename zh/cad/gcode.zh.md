{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE 文件 - 什么是 .gcode 文件以及如何打开它？",
   "description":"了解 GCODE 文件格式以及可创建和打开 GCODE 文件的 API。",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-zh",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## 什么是一 .gcode 文件？

**GCODE 文件** 是一种纯文本文件，其中包含用于控制计算机化机床和 3D 打印机的指令； G 代码，或几何代码”，是一种用于控制 **CNC（计算机数控）** 机器的运动和动作的语言； CNC 机床包括铣床、车床、铣床和 3D 打印机。

G代码命令以特定语法编写，通常由字母和数字组成；每个命令指示机器执行特定操作，例如将工具移动到特定位置、更换工具或调整速度。

G代码通常由**CAM（计算机辅助制造）**软件生成； CAM软件采用3D模型或2D设计并生成相应的刀具路径和G代码指令；然后将 G 代码文件加载到 CNC 机床或 3D 打印机中执行。

G 代码文件通常具有.nc”或.gcode”文件扩展名，例如program.nc”或print.gcode”。

## GCODE 文件结构：

GCODE 文件是纯文本文件，每行包含特定命令；这些命令的范围从控制机器的运动到调整温度、速度和其他对物体制造至关重要的参数。

GCODE的语法涉及字母和数字的组合；每个代表不同的动作或参数；常用指令包括用于移动的 G0 和 G1，用于主轴控制的 M3 和 M5，以及分别用于速度和进给速度调整的 S 和 F。

## G代码生成：

**Simplify3D** 和 **Slic3r** 等切片软件可将计算机辅助设计 (CAD) 绘图转换为 GCODE； CAD 软件用于创建 3D 模型，然后以 STL 等格式导出；切片软件采用这些模型并生成 GCODE 文件，指定层高、打印速度和温度设置等详细信息。

## G代码示例

以下是用于移动 CNC 机床的 G 代码的简单示例：

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## 如何打开 .gcode 文件？

要打开 G 代码文件，您可以根据需要使用不同类型的软件。

如果您为 3D 打印机生成了 G 代码；您可以使用3D打印机附带的软件或专用切片软件打开它；示例包括 **PrusaSlicer**、**Cura**、**Simplify3D**、**MatterControl** 或 **Repetier-Host**；这些程序通常具有用户友好的界面，允许您加载和可视化 G 代码。

GCODE 文件是纯文本，因此您可以使用任何文本编辑器打开它们；常见的文本编辑器包括 **Notepad（在 Windows 上）**、**TextEdit（在 macOS 上）** 或 **Gedit（在 Linux 上）**；只需**右键单击** G 代码文件，选择**打开方式”**，然后选择文本编辑器。

