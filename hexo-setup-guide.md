# Hexo博客设置指南

## 什么是Hexo？
Hexo是一个快速、简洁且高效的博客框架，特别适合中文用户。

## 安装步骤

### 1. 安装Node.js
- 访问 [nodejs.org](https://nodejs.org)
- 下载并安装LTS版本

### 2. 安装Hexo
```bash
npm install -g hexo-cli
```

### 3. 创建博客
```bash
hexo init my-blog
cd my-blog
npm install
```

### 4. 安装主题（推荐）
```bash
# 安装NexT主题
git clone https://github.com/theme-next/hexo-theme-next themes/next

# 配置主题
# 编辑 _config.yml
theme: next
```

### 5. 创建文章
```bash
hexo new "我的第一篇博客"
```

### 6. 本地预览
```bash
hexo server
```

### 7. 部署到GitHub Pages
```bash
# 安装部署插件
npm install hexo-deployer-git --save

# 配置 _config.yml
deploy:
  type: git
  repo: https://github.com/用户名/用户名.github.io.git
  branch: master

# 部署
hexo clean
hexo generate
hexo deploy
```

## 优势
- 🚀 生成速度快
- 🎨 主题丰富
- 📱 移动端友好
- 🔍 SEO优化
- 📝 Markdown支持
- 🌍 多语言支持

## 常用命令
```bash
hexo new "文章标题"    # 创建新文章
hexo generate          # 生成静态文件
hexo server            # 启动本地服务器
hexo deploy            # 部署到远程仓库
hexo clean             # 清理缓存
```
