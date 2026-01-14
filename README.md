# ImAlive-Page

静态 HTML 资源页面项目，包含隐私协议、用户协议等多语言文档，通过 GitHub Pages 提供访问。

## 📁 项目结构

```
docs/
├── index.html                    # 根目录首页（语言选择/跳转）
├── privacy/                      # 隐私政策
│   ├── index.html               # 隐私政策语言选择页
│   ├── en/
│   │   ├── index.html          # 英文隐私政策
│   │   └── privacy_en.html     # （保留的原文件）
│   ├── zh/
│   │   ├── index.html          # 简体中文隐私政策
│   │   └── privacy_zh.html     # （保留的原文件）
│   ├── zh-tc/
│   │   ├── index.html          # 繁体中文隐私政策
│   │   └── privacy_tc.html     # （保留的原文件）
│   └── ja/
│       ├── index.html          # 日文隐私政策
│       └── privacy_ja.html     # （保留的原文件）
└── keep                         # （保留文件）
```

## 🌐 访问方式

### GitHub Pages URL 结构

GitHub Pages 访问地址：https://codexbx.github.io/ImAlive-Page/

| 页面 | URL | 说明 |
|------|-----|------|
| 首页 | https://codexbx.github.io/ImAlive-Page/ | 自动根据浏览器语言跳转 |
| 隐私政策（自动跳转） | https://codexbx.github.io/ImAlive-Page/privacy/ | 自动识别语言并跳转 |
| 英文隐私政策 | https://codexbx.github.io/ImAlive-Page/privacy/en/ | 直接访问英文版 |
| 简体中文隐私政策 | https://codexbx.github.io/ImAlive-Page/privacy/zh/ | 直接访问简体中文版 |
| 繁体中文隐私政策 | https://codexbx.github.io/ImAlive-Page/privacy/zh-tc/ | 直接访问繁体中文版 |
| 日文隐私政策 | https://codexbx.github.io/ImAlive-Page/privacy/ja/ | 直接访问日文版 |

## ✨ 功能特点

1. **自动语言检测**：根据浏览器语言自动跳转到对应语言版本
2. **多语言支持**：支持英文、简体中文、繁体中文、日文
3. **响应式设计**：适配移动端和桌面端
4. **深色模式**：自动适配系统深色模式
5. **语言切换**：每个页面都提供便捷的语言切换导航

## 🚀 本地预览

```bash
# 方法1: 使用 Python 简单服务器
cd docs
python3 -m http.server 8000

# 方法2: 使用 Node.js 的 http-server
npx http-server docs -p 8000

# 然后在浏览器访问: http://localhost:8000
```

## 📝 添加新内容

### 添加新的协议页面（如用户协议）

1. 在 `docs/` 下创建新目录：
```bash
mkdir -p docs/terms/{en,zh,zh-tc,ja}
```

2. 为每个语言创建 `index.html`，参考 `docs/privacy/` 的结构

3. 创建语言选择页 `docs/terms/index.html`

### 添加新语言

1. 在相应功能目录下创建新语言目录，如 `docs/privacy/ko/`
2. 创建该语言的 `index.html`
3. 更新对应的语言选择页面，添加新语言选项
4. 更新其他语言页面的导航栏

## 🔧 GitHub Pages 配置

1. 进入仓库 Settings → Pages
2. Source 选择：`Deploy from a branch`
3. Branch 选择：`main`（或你的默认分支）
4. Folder 选择：`/docs`
5. 保存后等待部署完成

## 📱 应用集成

在你的移动应用中，可以使用以下 URL 展示隐私政策：

```swift
// iOS Swift 示例
let privacyURL = "https://codexbx.github.io/ImAlive-Page/privacy/"

// Android Kotlin 示例
val privacyURL = "https://codexbx.github.io/ImAlive-Page/privacy/"
```

浏览器会自动根据用户的语言设置显示对应版本。

## 🎨 自定义样式

所有页面的样式都内嵌在 HTML 文件的 `<style>` 标签中，你可以根据需要修改：

- 字体：修改 `font-family`
- 颜色：修改 CSS 变量或具体颜色值
- 布局：修改 `max-width`、`padding` 等属性
- 深色模式：修改 `@media (prefers-color-scheme: dark)` 中的样式

## 📄 许可证

请根据你的项目需要添加适当的许可证。

## 🤝 贡献

欢迎提交 Issue 或 Pull Request 来改进本项目。
