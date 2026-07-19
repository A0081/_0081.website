# _0081 WebSite
 
基于 [Hexo](https://hexo.io/) + [NexT Theme](https://theme-next.js.org/) 搭建的个人文章网站。

本项目用于记录个人成长、技术研究、生活记录以及长期积累的内容。

---

## 环境要求

- Node.js
- npm
- Git
- Hexo CLI

## 一、初始化项目
1. 克隆仓库
```bash
git clone https://github.com/A0081/_0081.website.git
```
进入项目目录：
```bash
cd _0081.website
```
检查项目结构：
```bash
tree -L 1
.
├── _config.yml        # Hexo 主配置
├── package.json       # 项目依赖
├── source             # 博客文章
├── themes             # 主题目录
│   └── next           # NexT主题
├── scaffolds          # 文章模板
└── public             # 生成后的静态文件
```
## 二、安装运行环境
1. 安装 Node.js

Arch Linux：
```bash
sudo pacman -S nodejs npm
```
检查：
```bash
node -v
npm -v
```
2. 安装 Hexo CLI
```
npm install -g hexo-cli
```
检查：
```
hexo -v
```
## 三、安装项目依赖

进入博客目录：
```bash
cd _0081.website
npm install
```
该命令会根据：
```
package.json
```
自动安装 Hexo 以及相关插件。

安装完成后会生成：
```
node_modules/
package-lock.json
```
其中：
```
node_modules/
```
无需提交到 Git。

## 四、配置 NexT 主题

确认主题目录：
```
ls themes
```
应该存在：
```
next
```
如果不存在：
```
git clone https://github.com/next-theme/hexo-theme-next themes/next
```
修改 Hexo 配置：

打开：
```bash
vim _config.yml
```
确认：

theme: next
## 五、本地运行
清理缓存
```bash
hexo clean
```
生成网页
```bash
hexo generate
```
或者：
```bash
hexo g
```
启动本地服务器
```bash
hexo server
```
或者：
```bash
hexo s
```
访问：
```
http://localhost:4000
```
即可查看博客。


## 六、部署

生成静态文件：
```bash
hexo clean
hexo generate
```
部署：
```bash
hexo deploy
```
如果使用 GitHub Pages：
```bash
git push
```
## 七、Git 管理

查看修改：
```bash
git status
```
提交：
```bash
git add .
git commit -m "update blog"
git push
```
## 八、开发环境
当前博客技术栈：
```bash
.
├── Archlinux    # 系统
├── Git          # 版本管理   
├── Hexo        # 建站工具
├── NexT Theme  # 主题
├── Github      # 代码托管
└── Netlify     # 网页部署
```