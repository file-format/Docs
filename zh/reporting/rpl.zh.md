{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - 报告页面布局",
  "keywords" :[ "rpl", "报表页面布局", "XSD", "SQL Server", "reporting"],
  "description":"了解 RPL 流格式,这是 Microsoft SQL Server Reporting Services 在与查看器控件联系时使用的内部二进制格式。",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## 什么是一 .rpl 文件？ ##

RPL（报表页面布局）流格式是 MS SQL Server Reporting Services 在与查看器控件联系时使用的内部二进制格式，以减少从服务器到客户端查看器控件的一些呈现工作。开发人员可以使用 RPL 创建自定义报告设计器，这将生成 RPL 以及处理和显示 RPL 文件以显示报告的自定义报告呈现器。

## RPL 结构

RPL 流包括流结构、报告结构、报告属性和枚举。每个结构包括以下内容：

- 结构的定义。

- 结构的增强巴科斯-瑙尔形式 (ABNF) 语法。

- 结构的位图。

- 结构中包含的所有字段的定义。

以下是关于一些 RPL 结构的简要说明：

### 流结构
流结构由一系列记录组成。一条记录包含零个或多个包含报表布局的结构化字段。

#### RPL 流
RPL 流必须只有一个报告记录，并且流必须是一系列保持报告层次结构的二进制记录。

＃＃＃＃ 记录
记录是用于保存有关报告的信息的基本构建块。记录由可变长度的字节序列组成。记录由两部分组成：
- 记录类型
- 特定于该记录类型的记录数据。
记录类型是一个字节，它定义记录指定什么类型的信息以及与记录有关的记录数据的结构如何排序和结构化。记录值取决于特定于该记录的数据类型。

#### 简单数据类型结构

下表定义了 RPL 流中的数据类型。

|说明|格式|
---|---|
|Char|表示 16 位（2 字节）数字（序数）值。|
|字节|表示一个 8 位（1 字节）无符号整数。|
|Int16|表示一个 16 位（2 字节）有符号整数。|
|Single|表示 32 位（4 字节）单精度浮点值。|
|十进制|表示 128 位（16 字节）数据类型。|
|DateTime|表示日期和时间值的 64 位（8 字节）编码。|
|Int64|表示一个 64 位（8 字节）有符号整数。|
|Int32|表示 32 位（4 字节）有符号整数。|
|Float|表示 32 位（4 字节）单精度浮点值。|
|Boolean|表示 8 位（1 字节）逻辑布尔类型值。有效值为真 (1) 和假 (0)。|
|Long|表示一个 64 位（8 字节）有符号整数。|
|String|协议中的所有字符串值必须是 UNICODE UTF-16。默认情况下，所有字符串值都以定义字符串长度的整数开头。字符串值在协议中表示为字节数组；字节数必须等于字符串中的字符数乘以 2。|

### 报告结构
报告结构包括其相关结构和元素的定义和大小。

以下列表指定了报告结构：

- 报告
- 版本
- 报告属性
- 偏移数组元素
- 页面内容
- 页
- 页面属性
- 页面布局
- 部分
- 简单部分
- 混合部分
- 截面属性
- 身体区域元素
- 页眉元素
- 页脚元素
- 身体元素
- 元素属性
- 共享元素属性
- 使用共享元素属性
- 内联共享元素属性
- 非共享元素属性
- 风格
- 共享样式属性
- 非共享样式属性
- 动作信息
- 动作信息内容
- 行动
- ActionImageMapAreas
- ActionInfoWithMaps
- 动态图像数据
- ImageConsolidationOffsets
- 报告项目
- 线
- 图片
- 图像数据属性
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- 非共享图像数据属性
- 图像数据
- ImageMapAreas
- 图像地图区域
- 图表
- 仪表板
- 地图
- 长方形
- 子报告
- 富文本框
- 段落内容
- 文本运行
- 段落
- RichTextBox结构
- Tablix
- Tablix内容
- Tablix结构
- TablixMeasurements
- 列宽
- 列信息
- 行高
- 行信息
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- 测量
- 测量
- 报告元素结束

＃＃＃ 特性
以下是可在 RPL 流中使用的属性列表：

- ID
- 列数
- 列间距
- 唯一名称
- 姓名
- 标签
- 书签
- 工具提示
- 切换项目
- 描述
- 地点
- 消费容器白色空间 (RPL 10.6)
- 语
- 执行时间处理时间
- 作者
- 自动刷新
- 报告名称
- 页面高度
- 页面宽度
- 边距顶部
- 左边距
- MarginRight
- 边距底部
- 列
- 页面名称 (RPL 10.6)
- 倾斜
- 可以成长
- 收缩
- 价值
- 切换状态
- 可以排序
- 排序状态
- 公式
- IsToggleParent
- 类型代码
- 原始值
- 简单
- 内容偏移
- 流名称
- 尺码
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- 处理错误
- 图像MIMEType
- 图像名称
- 宽度
- 高度
- 水平分辨率
- 垂直分辨率
- 原始格式
- 超链接
- 书签链接
- DrillthroughId
- 钻取网址
- 边框颜色
- 边框颜色左
- BorderColorRight
- 边框颜色顶部
- 边框颜色底部
- 边框样式
- BorderStyleLeft
- BorderStyleRight
- 边框样式顶部
- 边框样式底部
- 边框宽度
- 左边框宽度
- BorderWidthRight
- 边框宽度顶部
- 边框宽度底部
- 填充左
- PaddingRight
- 填充顶部
- 填充底部
- 字体样式
- 字体系列
- 字体大小
- 字体粗细
- 格式
- 文字装饰
- 文本对齐
- 垂直对齐
- 颜色
- 线高
- 方向
- 写作模式
- UnicodeBiDi
- 背景图片
- 背景颜色
- 背景重复
- 数字语言
- 数字变体
- 日历
- 列标题行
- RowHeaderColumns
- ColsBeforeRowHeader
- 布局方向
- 定义路径
- 等级
- 成员细胞索引
- CellItemOffset
- 科尔跨度
- 行跨度
- DefIndex
- 列索引
- 行索引
- 组标签
- 递归切换级别
- 列表样式
- 列表级别
- 段落编号
- 右缩进
- 左缩进
- 悬挂缩进
- 空间之前
- 太空之后
- 第一行
- 标记
- 内容顶部
- 内容左
- 内容宽度
- 内容高度
- 状态
- 细胞项目状态
- MemberDefState

### 枚举
以下列表显示了可以在 RPL 流中使用的枚举：

- 排序选项
- 尺码
- 形状类型
- 图像原始格式
- 字体样式
- 字体重量
- 文字装饰
- 文本对齐
- 垂直对齐
- 方向
- 写作模式
- UnicodeBiDiTypes
- 日历
- 边框样式
- 背景重复类型
- 列表样式
- 标记样式
- 类型代码
- 状态值
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize





## 参考 ＃＃

- [报告页面布局 (RPL) 二进制流格式](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

