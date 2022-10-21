{
  "date" : "2019-10-11",
  "keywords" :["vcxproj","文件","扩展","文件格式","Visual C++ 项目","编程指南"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"了解 VCXPROJ 文件格式和可以创建和打开 VCXPROJ 文件的 API。",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .vcxproj 文件？

扩展名为 .vcxproj 的文件是 Microsoft Visual C++ 项目文件，用于存储 [C++](/zh/programming/cpp/) 项目信息。它包含 MSBuild 项目系统用于编译和构建最终输出的信息。 Visual C++ 项目的 VCXPROJ 与 .NET 项目的 [CSPROJ](/zh/programming/csproj/) 相同。 VCXPROJ 文件不包含任何代码，而是引用为项目定义的所有类、目标和属性以构建项目。这些可以在纯文本编辑器中打开，或者最好在 Microsoft Visual Studio IDE 中打开。


## VCXPROJ 文件格式 - 更多信息

VCXPROJ 文件是以 [XML](/zh/web/xml/) 文件格式创建的文本文件。这些可以在任何文本编辑器中打开，但强烈建议使用 Microsoft Visual Studio IDE 打开和编辑这些文件。这些不是为手动编辑而设计的。错误可能会导致 IDE 崩溃或以意想不到的方式运行。

示例 VCXPROJ 文件的内容如下。

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ 文件元素

一个典型的 VCXPROJ 文件包含许多元素，如上面的示例 XML 所示。微软的【VCXPROJ结构】(https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)对每个文件元素进行了详细解释，可以参考从开发者的角度来看。

#### 项目元素

这是 VCXPROJ 文件的根节点。 MSBuild 使用此元素读取构建版本和默认编译目标。

#### ProjectConfigurations 项目组元素

它包含项目配置信息，可以包括构建方法（调试或发布）、32 位或 64 位编译、优化选项等。 IDE 使用该组中的信息来加载项目。

#### 项目配置元素

VCXPROJ 文件中的 ProjectConfiguration 元素包含有关加载项目的构建和平台的信息。它的名称应该遵循 `$(Configuration)|$(Platform)` 的格式。

#### 全局属性组元素

此部分包含提供项目级别信息的设置，例如：

* 项目向导
* 根命名空间
* ApplicationType 或 ApplicationTypeRevision


## 参考

* [VCXPROJ 结构 - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ 项目文件](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

