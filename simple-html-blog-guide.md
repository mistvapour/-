# 简单HTML博客指南

## 方案概述
直接使用HTML文件创建博客，无需复杂的构建工具。

## 文件结构
```
your-blog/
├── index.html          # 主页
├── about.html          # 关于页面
├── contact.html        # 联系页面
├── posts/              # 文章目录
│   ├── post1.html
│   ├── post2.html
│   └── post3.html
├── css/                # 样式文件
│   └── style.css
├── js/                 # JavaScript文件
│   └── main.js
└── images/             # 图片资源
    └── logo.png
```

## 创建步骤

### 1. 创建基础HTML结构
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的博客</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <a href="index.html">首页</a>
            <a href="about.html">关于</a>
            <a href="contact.html">联系</a>
        </nav>
    </header>
    
    <main>
        <h1>欢迎来到我的博客</h1>
        <p>这里是我的博客内容...</p>
    </main>
    
    <footer>
        <p>&copy; 2024 我的博客</p>
    </footer>
</body>
</html>
```

### 2. 添加CSS样式
```css
/* css/style.css */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

header {
    background: #333;
    color: white;
    padding: 1rem;
}

nav a {
    color: white;
    text-decoration: none;
    margin-right: 1rem;
}

main {
    max-width: 800px;
    margin: 2rem auto;
    padding: 0 1rem;
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
}
```

### 3. 部署到GitHub Pages
1. 创建GitHub仓库
2. 上传所有文件
3. 在仓库设置中启用GitHub Pages
4. 选择源分支
5. 访问您的博客

## 优势
- ✅ 简单直接
- ✅ 无需构建工具
- ✅ 完全控制
- ✅ 快速部署
- ✅ 易于维护

## 劣势
- ❌ 手动管理内容
- ❌ 无自动化功能
- ❌ 需要手动更新导航
- ❌ 无搜索功能
