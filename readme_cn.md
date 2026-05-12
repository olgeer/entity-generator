# entity-generator

![Build](https://github.com/olgeer/entity-generator/workflows/Build/badge.svg)
[![Version](https://img.shields.io/jetbrains/plugin/v/MARKETPLACE_ID.svg)](https://plugins.jetbrains.com/plugin/MARKETPLACE_ID)
[![Downloads](https://img.shields.io/jetbrains/plugin/d/MARKETPLACE_ID.svg)](https://plugins.jetbrains.com/plugin/MARKETPLACE_ID)

## 模板待办事项清单
- [x] 创建新的 [IntelliJ Platform Plugin Template][template] 项目。
- [ ] 熟悉 [模板文档][template]。
- [ ] 调整 [pluginGroup](./gradle.properties)、[pluginName](./gradle.properties)，以及 [id](./src/main/resources/META-INF/plugin.xml) 和 [源代码包](./src/main/kotlin)。
- [ ] 在 `README` 中调整插件描述（参见 [提示][docs:plugin-description]）
- [ ] 查看 [法律协议](https://plugins.jetbrains.com/docs/marketplace/legal-agreements.html?from=IJPluginTemplate)。
- [ ] [手动发布插件](https://plugins.jetbrains.com/docs/intellij/publishing-plugin.html?from=IJPluginTemplate) 首次发布。
- [ ] 在上述 README 徽章中设置 `MARKETPLACE_ID`。插件发布到 JetBrains Marketplace 后可获取该 ID。
- [ ] 设置 [插件签名](https://plugins.jetbrains.com/docs/intellij/plugin-signing.html?from=IJPluginTemplate) 相关的 [密钥](https://github.com/JetBrains/intellij-platform-plugin-template#environment-variables)。
- [ ] 设置 [部署令牌](https://plugins.jetbrains.com/docs/marketplace/plugin-upload.html?from=IJPluginTemplate)。
- [ ] 点击 [IntelliJ Platform Plugin Template][template] 顶部的 <kbd>Watch</kbd> 按钮，以便收到包含新功能和修复的发布通知。

<!-- Plugin description -->
这个精美的 IntelliJ 平台插件将实现您绝妙的创意。

本部分内容将作为 [plugin.xml](/src/main/resources/META-INF/plugin.xml) 文件的源码，在构建过程中由 [Gradle](/build.gradle.kts) 提取。

为保持一切正常工作，请勿移除 `<!-- ... -->` 部分。
<!-- Plugin description end -->

## 功能特性

- **工具窗口**：提供自定义工具窗口（MyToolWindow）
- **应用激活监听**：监听应用激活事件
- **项目服务**：提供项目级别的服务支持
- **国际化支持**：支持资源束国际化

## 安装方式

- **使用 IDE 内置插件系统**：
  
  <kbd>设置/首选项</kbd> > <kbd>插件</kbd> > <kbd>市场</kbd> > <kbd>搜索 "entity-generator"</kbd> >
  <kbd>安装</kbd>
  
- **通过 JetBrains Marketplace**：

  访问 [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/MARKETPLACE_ID) 并点击 <kbd>Install to ...</kbd> 按钮（如果您的 IDE 正在运行）。

  您也可以从 [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/MARKETPLACE_ID/versions) 下载 [最新版本](https://plugins.jetbrains.com/plugin/MARKETPLACE_ID/versions)，然后手动安装：
  <kbd>设置/首选项</kbd> > <kbd>插件</kbd> > <kbd>⚙️</kbd> > <kbd>从磁盘安装插件...</kbd>

- **手动安装**：

  下载 [最新版本](https://github.com/olgeer/entity-generator/releases/latest) 并手动安装：
  <kbd>设置/首选项</kbd> > <kbd>插件</kbd> > <kbd>⚙️</kbd> > <kbd>从磁盘安装插件...</kbd>

## 构建与开发

### 环境要求
- JDK 17 或更高版本
- IntelliJ IDEA（建议使用最新版本）

### 构建命令
```bash
# 构建插件
./gradlew buildPlugin

# 运行 IDE 进行调试
./gradlew runIde

# 运行测试
./gradlew test

# 验证插件
./gradlew verifyPlugin
```

## 项目结构

```
entity-generator/
├── src/
│   ├── main/
│   │   ├── kotlin/          # Kotlin 源代码
│   │   └── resources/       # 资源文件（包括 plugin.xml）
│   └── test/
│       └── kotlin/          # 测试代码
├── build.gradle.kts         # Gradle 构建配置
├── gradle.properties        # Gradle 属性配置
└── README.md                # 英文文档
```

## 技术栈

- **语言**：Kotlin
- **平台**：IntelliJ Platform
- **构建工具**：Gradle (Kotlin DSL)
- **最低 IDE 版本**：参见 [build.gradle.kts](./build.gradle.kts)

## 贡献指南

欢迎贡献！请遵循以下步骤：

1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 许可证

本项目基于 [IntelliJ Platform Plugin Template][template] 创建。

## 相关链接

- [IntelliJ 平台插件开发文档](https://plugins.jetbrains.com/docs/intellij/welcome.html)
- [IntelliJ Platform Plugin Template][template]
- [JetBrains Marketplace](https://plugins.jetbrains.com/)

---
插件基于 [IntelliJ Platform Plugin Template][template] 构建。

[template]: https://github.com/JetBrains/intellij-platform-plugin-template
[docs:plugin-description]: https://plugins.jetbrains.com/docs/intellij/plugin-user-experience.html#plugin-description-and-presentation
