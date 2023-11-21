{
"日期":"2023-07-18",
   "keywords":[
"PAR",
"PAR 文件",
"如何打开 par 文件",
"文件",
"PAR 文件扩展名",
"扩大",
"文件"
],
   "author":{
"display_name":"沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title":"PAR 文件格式 - Parchive 索引文件",
   "description":"了解 PAR 格式以及可以创建和打开 PAR 文件的 API。",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent": "compression"
}
},
"lastmod": "2023-07-18"
}

## 什么是 .PAR 文件？

在 Parchive (PAR) 归档中，.par 文件是指包含一组奇偶校验卷或奇偶校验块的索引文件。当存档中的一个或多个文件丢失或损坏时，该索引文件用于错误检测和恢复目的。

Parchive 存档通常由原始数据文件和相应的奇偶校验卷组成。奇偶校验卷是使用 Reed-Solomon 纠错算法创建的。这些奇偶校验卷包含可用于恢复原始数据文件的冗余信息。

.par 文件也称为奇偶校验卷集，包含有关存档中奇偶校验卷的结构和位置的信息。它充当恢复过程的索引或映射。通过使用 .par 文件，专用 PAR 软件可以确定需要哪些奇偶校验卷以及如何使用它们来重建丢失或损坏的文件。

当 Parchive 存档中的一个或多个文件无法访问或损坏时，.par 文件可以与可用的奇偶校验卷结合使用来恢复丢失的数据。 PAR 软件读取 .par 文件，识别丢失或损坏的文件，并使用奇偶校验卷来重建它们。

## 如何打开 .PAR 文件？

要打开和使用 .par 文件，您需要专门的 PAR 软件。以下是一些可以处理 .par 文件的流行软件选项：

- **QuickPar：** QuickPar 是一款广泛使用的 Windows PAR 软件。它允许您创建、验证和修复 PAR 文件。您可以在 QuickPar 中打开 .par 文件来验证其完整性，或使用它来修复 Parchive 存档中损坏或丢失的文件。

- **MultiPar：** MultiPar 是另一种适用于 Windows 的流行 PAR 软件。它支持 PAR 和 PAR2 文件格式，并提供创建、验证和修复存档的高级功能。 MultiPar 可以打开 .par 文件并根据提供的奇偶校验卷执行错误检测和恢复操作。

- **MacPAR deLuxe：** MacPAR deLuxe 是专为 macOS 设计的 PAR 软件。它支持 PAR 和 PAR2 文件格式，并提供与 QuickPar 和 MultiPar 类似的功能。 MacPAR deLuxe 可以打开 .par 文件并协助验证存档并恢复损坏或丢失的文件。

## PAR 文件格式 - 更多信息

PAR 文件格式通常称为 Parchive，是一种用于创建奇偶校验数据以及在文件存档中执行错误检测和恢复的特定文件格式。 PAR 文件格式通常由三种类型组成：PAR、PAR2 和 PAR3。

- **PAR：** 原始 PAR 文件格式，也称为 PAR1，由 Parchive 项目开发。它包括从原始数据文件生成的奇偶校验数据。 PAR 文件提供基本级别的错误检测和恢复，但在纠错能力方面存在限制。

- **PAR2：** PAR2 是 PAR 文件格式的改进版本。它提供了更先进的纠错功能和增强的恢复功能。 PAR2 文件通常用于创建奇偶校验数据，可以恢复存档中丢失或损坏的文件。 PAR2 文件可以更好地防止数据损坏，并广泛用于文件归档目的。

- **PAR3：** PAR3 是 PAR 文件格式的最新版本，在纠错和恢复方面提供了进一步的改进。与 PAR2 相比，它提供了更高级别的冗余和纠错能力。 PAR3 文件旨在为存档中存储的数据提供更强大的保护和恢复选项。

PAR 软件广泛支持 PAR2 和 PAR3 文件格式，并且能够验证存档中文件的完整性并恢复丢失或损坏的数据。 PAR 和 PAR2 文件仍然常用，而 PAR3 文件由于其增强的纠错功能而逐渐被采用。

## 参考
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

