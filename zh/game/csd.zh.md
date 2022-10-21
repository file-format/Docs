{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 CSD Steam 游戏数据备份文件格式和 API。",
  "title" :"CSD 文件格式 - Steam 游戏数据备份文件",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## 什么是一 .csd 文件？

CSD 文件是游戏服务 **Steam** 生成的游戏备份文件，可让用户下载和管理 **Valve** 游戏。它包含与游戏相关的备份数据，可用于恢复已删除的游戏。只有通过 Steam 完成下载、安装和修补游戏后，Steam 才能从 CSD 文件恢复游戏。要从 CSD 文件恢复游戏，请使用 Steam → 备份和恢复 Gamesteam 选项并选择文件。

## CSD 文件格式 - 更多信息

CSD 文件格式的内部结构不公开，其文件格式规范不供开发者参考。 CSD 文件伴随着 CSM 和 ISS 文件，它们也是 Steam 游戏文件格式。

### 在哪里可以找到 Steam 备份文件？

整个 Steam 备份文件可以在以下位置找到：

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - 自定义配置和配置脚本
* \downloads\ - 多人游戏的自定义内容
* \maps\ - 在多人游戏中安装或下载的自定义地图
* \materials\ - 自定义纹理和皮肤
* \SAVE\ - 单人游戏存档

但是，第三方创建的游戏的位置可能不同，由游戏开发商决定。

### 从 CSD 备份文件恢复

安装 Steam 并登录到正确的 Steam 帐户（有关详细说明，请参阅安装 Steam）
* 启动蒸汽
* 点击 Steam 应用程序左上角的“Steam"
* 选择“备份和恢复游戏..."
* 选择“恢复以前的备份"
* 浏览到游戏备份文件的位置
* 继续通过 Steam 窗口安装必要的游戏。

## 参考

* [使用 Steam 备份功能](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

