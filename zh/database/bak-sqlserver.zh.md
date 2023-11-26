{
"date": "2023-06-12",
  "keywords": [
"巴克",
".bak 文件",
"Microsoft SQL Server 数据库备份",
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
"title": "BAK 文件格式 - Microsoft SQL Server 数据库备份",
  "description":"了解 BAK SQL Server 备份格式以及可创建和打开 BAK 文件的 API。",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent": "database"
}
},
"lastmod": "2023-06-12"
}

## 什么是 .bak 文件？

在 Microsoft SQL Server 上下文中,".bak"文件是一种备份文件格式,用于存储 SQL Server 数据库的副本。这些文件包含数据库在特定时间点的快照,包括其架构,数据和其他相关信息。它们是使用 SQL Server 的内置备份和恢复功能生成的,有几个重要的用途：

1. **数据恢复：** .bak 文件提供了一种在数据丢失,损坏或其他问题时恢复数据库的方法。通过从 .bak 文件恢复数据库,您可以将其恢复到之前的状态,从而最大限度地减少停机时间和数据丢失。

2. **迁移和克隆：** 备份文件通常用于在服务器之间迁移数据库或创建数据库副本以用于测试,开发或报告目的。它们提供了在环境之间移动数据库的一致且有效的方法。

3. **时间点恢复：** SQL Server 允许您使用.bak 文件执行时间点恢复。这意味着您可以将数据库恢复到特定时刻,这对于法规遵从性或数据审计至关重要。

4. **灾难恢复：** .bak 文件是灾难恢复规划的关键部分。它们确保您的数据安全,并且在发生硬件故障,自然灾害或其他灾难性事件时可以快速恢复。

## 在 SQL Server 中创建 .BAK 文件

若要在 SQL Server 中创建 .bak 文件,通常使用 SQL Server Management Studio (SSMS) 或 Transact-SQL (T-SQL) 命令,例如 BACKUP DATABASE 或 BACKUP LOG。以下是如何使用 T-SQL 创建数据库备份的简化示例：

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## 在 SQL Server 中还原 .BAK 文件

要从 .bak 文件恢复数据库,您可以使用 RESTORE DATABASE 命令：

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## 如何在SQL Server中打开BAK文件？

要打开并访问".bak"文件中存储的数据,您通常需要将其还原到 Microsoft SQL Server 实例。以下是使用 SQL Server Management Studio (SSMS) 打开".bak"文件的一般步骤：

1. **启动 SQL Server Management Studio**：在计算机上打开 SSMS。您通常可以在"开始"菜单中或通过搜索"SQL Server Management Studio"找到它。

2. **连接到 SQL Server 实例**：在 SSMS 中,连接到要还原数据库的 SQL Server 实例。您需要必要的权限才能执行此操作。

3. **恢复数据库**：

A。在左侧的"对象资源管理器"窗格中,展开 SQL Server 实例。

b.展开"数据库"节点。

C。右键单击"数据库"并选择"恢复数据库"。

4. **指定来源和目的地**：

A。在"恢复数据库"对话框的"常规"页面中,在"至数据库"字段中输入新数据库的名称。这将是恢复的数据库的名称。

b.在"源"部分中,选择"设备"作为备份介质类型。

C。单击"设备"字段旁边的"..."按钮,浏览要恢复的".bak"文件。

d.选择您要打开的".bak"文件,然后单击"确定"。

5. **恢复选项**：根据需要查看并配置恢复选项。您可以指定是否覆盖现有数据库,设置恢复选项等。确保根据您的要求设置这些选项。

6. **启动恢复**：配置恢复选项后,单击"恢复数据库"对话框中的"确定"按钮。 SQL Server 将开始恢复过程。

7. **访问恢复的数据库**：成功恢复后,您可以像访问其他数据库一样在 SQL Server Management Studio 中访问恢复的数据库。您可以运行查询,查看表以及使用数据库中的数据。

## 其他 BAK 文件

以下是使用 **.bak** 文件扩展名的其他文件类型。

**数据库**
- [BAK - 数据库备份文件](/zh/database/bak/)
- [BAK - Swiftpage 行动！数据库备份](/zh/database/bak-act/)

**游戏**
- [BAK - 泰拉瑞亚世界或玩家备份](/zh/game/bak-terraria/)

**杂项**
- [BAK - 备份文件](/zh/misc/bak-backup/)
- [BAK - Chromium 书签备份](/zh/misc/bak-chromium/)
- [BAK - Finale 2012 分数备份](/zh/misc/bak-finale/)
- [BAK - MobileTrans 备份](/zh/misc/bak-mobiletrans/)
- [BAK - VEGAS 视频项目备份](/zh/misc/bak-vegas/)

**设置**
- [BAK - Holo 启动器备份](/zh/settings/bak-holo/)

## 参考
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
