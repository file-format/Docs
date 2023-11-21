{
"date": "2023-06-12",
  "keywords": [
"巴克",
".bak 文件",
"比克铬书签",
"什么是 bak 文件",
"如何打开.bak文件",
"文件",
".bak 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "BAK 文件格式 - Chromium 书签备份",
  "description":"了解 BAK Chromium 书签格式以及可创建和打开 BAK 文件的 API。",
"linktitle": "比克铬书签",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
"parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## 什么是 .bak 文件？

在基于 Chromium 的 Web 浏览器（例如 Google Chrome 和 Microsoft Edge）中,.bak 文件本质上是书签的备份文件。这些书签保存为纯文本列表,使用的文件格式为 JSON。这些 .bak 文件的目的是通过提供可在意外删除或丢失时恢复的备份来保护您的书签。

基于 Chromium 的浏览器（包括 Google Chrome）通常会创建这些备份文件,并通常将其命名为"Bookmarks.bak"。它们本质上是您的书签在特定时间点的快照。

## 如何使用 .bak 文件恢复书签

1. **查找备份文件：** 它通常位于与您的 Chromium 配置文件关联的特定文件夹中。确切位置可能因您的操作系统而异。

在 Windows 上：查看"C:\Users\"<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`。

在 macOS 上：在"~/Library/Application Support/Chromium/Default/Bookmarks.bak"中搜索。

在 Linux 上：检查 `~/.config/chromium/Default/Bookmarks.bak`。

3. 确保您的 Chromium 浏览器已关闭。
4. 通过删除".bak"扩展名来重命名"Bookmarks.bak"文件,因此它简称为"Bookmarks"。
5.启动铬。

通过将 .bak 文件重命名为"书签",Chromium 会将其用作当前书签文件,并且您以前的书签应该会恢复。

## Chromium 书签备份

备份 Chromium 书签是一项明智的预防措施,可确保您不会丢失已保存的重要网页和 URL。 Chromium 是一款开源浏览器,是 Google Chrome 和 Microsoft Edge 等其他浏览器的基础。要备份您的 Chromium 书签,请按照以下步骤操作：

## 方法一：手动备份

1. **打开 Chromium**：在计算机上启动 Chromium 浏览器。

2. **访问书签**：单击浏览器窗口右上角的三个垂直点（菜单图标）。从下拉菜单中,将鼠标悬停在"书签"上以显示书签子菜单。

3. **导出书签**：在书签子菜单中,单击"书签管理器"。这将打开一个显示您的书签的新选项卡。

4. **导出书签**：在书签管理器选项卡中,再次单击三个垂直点（通常位于右上角）以打开书签管理器菜单。从此菜单中选择"导出书签"。

5. **选择位置**：选择要在计算机上保存导出的书签文件的位置。默认文件名是"bookmarks.html",但您可以根据需要更改它。将其保存到您会记住的位置。

6. **保存**：单击"保存"或"导出"按钮将书签保存为 HTML 文件。

您的书签现已备份为 HTML 文件。您可以将此文件复制到外部驱动器或云存储以妥善保管。

## 方法 2：与 Google 帐户同步（如果适用）

如果您在 Chromium 中登录 Google 帐户,您还可以使用内置同步功能来保证您的书签安全并在设备之间同步。这样,您的书签就会自动备份到您的 Google 帐户。

1. **打开 Chromium**：启动 Chromium 浏览器并确保您已登录 Google 帐户。

2. **启用同步**：单击浏览器窗口右上角的三个垂直点（菜单图标）,然后转到"设置"。

3. **同步和 Google 服务**：在"设置"选项卡中,单击左侧边栏上的"同步和 Google 服务"。

4. **同步您的数据**：在"同步"下,确保"书签"已打开。这会将您的书签与您的 Google 帐户同步。

您的书签现在将自动备份并与您的 Google 帐户同步。您可以通过在装有 Chromium 或其他支持 Google 同步的浏览器的任何设备上登录 Google 帐户来访问它们。

请记住还要定期手动备份书签,特别是如果您想要一个不仅仅依赖于 Google 帐户同步的本地副本。

## 如何打开 .BAK 文件

如果您想探索书签备份的原始数据,可以使用各种文本编辑器打开"Bookmarks.bak"文件,例如 Microsoft Visual Studio Code（在多个平台上可用）,Microsoft Notepad（适用于 Windows 用户）,Apple TextEdit （适用于 Mac 用户）,或您选择的任何其他文本编辑器。这样做将允许您查看文件中包含的书签和元数据。

您可以使用各种文本编辑软件和代码编辑器打开"Bookmarks.bak"文件并查看其内容。以下是一些常用的选项：

1.Visual Studio 代码（VS 代码）
2.记事本（Windows）
3. 文本编辑（Mac）
4. 崇高文本
5.记事本++
6. 原子
7.nano 和 Vim (Linux)
8.写字板（Windows）

## 其他 BAK 文件

以下是使用 **.bak** 文件扩展名的其他文件类型。

**数据库**
- [BAK - 数据库备份文件](/zh/database/bak/)
- [BAK - Swiftpage 行动！数据库备份](/zh/database/bak-act/)
- [BAK - Microsoft SQL Server 数据库备份](/zh/database/bak-sqlserver/)

**游戏**
- [BAK - 泰拉瑞亚世界或玩家备份](/zh/game/bak-terraria/)

**杂项**
- [BAK - 备份文件](/zh/misc/bak-backup/)
- [BAK - Finale 2012 分数备份](/zh/misc/bak-finale/)
- [BAK - MobileTrans 备份](/zh/misc/bak-mobiletrans/)
- [BAK - VEGAS 视频项目备份](/zh/misc/bak-vegas/)

**设置**
- [BAK - Holo 启动器备份](/zh/settings/bak-holo/)

## 参考
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
