# Whiteboard 免登录 · 本地优先的个人与课堂白板

- **生产域名**: `https://whiteboard.eazyopc.com`
- **功能定位**: 免登录、隐私、本地优先的个人与课堂白板（无账号、无云端、无多人实时协作）。便签、矩形/椭圆/菱形等图形、会跟随元素移动的连接箭头、多页与双板并排、模板（Pro）、本机多白板管理（免费 3 块，Pro 不限）。作品自动保存在浏览器 localStorage，可「保存作品 / 打开作品」为 `.eazyopc` 文件；导出 PNG（1080P / 4K）、SVG、300 DPI 打印 PDF。

---

## 🌟 核心特性
- **7 国全球语言 (i18n)**: 中、英、日、韩、德、西、法一键切换；
- **Cloudflare 边缘中间件 (`functions/_middleware.ts`)**: 自动检测 IP 国家无缝分流，保护爬虫正常索引；
- **10 种专业画笔**: 铅笔、钢笔、毛笔、荧光笔、粉笔、喷枪、激光笔、橡皮擦等；
- **7 种纸张底纹**: 点阵、纯白、5mm 方格、墨绿黑板、碳黑黑板、米黄纸、四线三格；
- **全矩阵站群互联**: 导航与页脚常驻链接到 EazyOPC 主站、VideoTools 视频工具及其他画板矩阵；
- **商业变现与合规**: 内置 Google AdSense `ca-pub-6499357447763670`、ads.txt、GSC 验证与 Creem $4.99 终身买断。

---

## 🚀 部署指南 (Cloudflare Pages)

1. 在 GitHub 建立公开仓库并推送：
   ```bash
   cd /Users/huafire777/Desktop/program/whiteboard
   git init
   git add .
   git commit -m "feat: initial commit for whiteboard"
   gh repo create whiteboard --public --source=. --remote=origin --push
   ```
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)：
   - **Workers 和 Pages** $	o$ **创建应用程序** $	o$ **Pages** $	o$ **连接到 Git**；
   - 选中 `whiteboard` 仓库；
   - **构建预设**: `None`（纯静态项目）；
   - 点击 **保存并部署**。
3. 在自定义域绑定 `whiteboard.eazyopc.com`，并在 Namecheap 加一条 CNAME 记录即可！
