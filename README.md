# 李伟华个人学术主页 | Weihua Li's Academic Homepage

这是一个**中英双语**、响应式的个人学术主页，专为学者、研究人员设计。

**在线预览**：待部署到 GitHub Pages

---

## ✨ 主要特性

- 🌐 **中英双语** - 一键切换语言，国际化友好
- 📱 **响应式设计** - 完美适配桌面、平板和手机
- 🎨 **现代化UI** - 简洁优雅的学术风格
- 🚀 **轻量级** - 纯 HTML/CSS/JS，无需构建
- 📊 **数据展示** - 论文数、引用数统计
- 🔗 **学术链接** - 集成 ResearchGate、ORCID、Google Scholar

---

## 📸 预览

### 个人信息
- **姓名**：李伟华（Weihua Li）
- **职位**：香港大学地理系 博士后研究员
- **合作导师**：宫鹏 教授
- **研究方向**：多源数据融合的辐射传输智慧建模以及全球智慧制图
- **GitHub**：https://github.com/BNUL
- **ORCID**：0000-0003-1529-5967

### 教育背景
- **博士**（2020-2025）：北京师范大学，导师：阎广建教授，研究方向：几何光学模型，植被辐射传输机理，路径长度分布
- **联合培养博士**（2023-2024）：法国图卢兹第三大学 CESBIO实验室，导师：Jean-Philippe Gastellu-Etchegorry教授
- **硕士**（2018-2020）：北京师范大学，导师：穆西晗副教授，研究方向：分形理论，间隙率模型，LAI地面测量
- **学士**（2014-2018）：电子科技大学，资源与环境学院

### 桌面版
- 渐变背景头部横幅
- 清晰的研究方向展示
- 独立的工作经历和教育背景时间线
- 代表作品卡片网格布局
- 详细的论文列表（链接至ResearchGate）

### 移动版  
- 汉堡菜单导航
- 流式布局自适应
- 触摸友好的交互

---

## 📁 文件结构

```
CV/
├── index.html          # 主页面（双语）
├── style.css           # 样式表
├── README.md           # 本文件
├── DEPLOY.md           # 部署指南
└── index-old.html      # 原始版本备份
```

---

## 🌐 语言切换功能

点击右上角的 **🌐 EN/中文** 按钮即可在中英文之间切换。

**实现原理：**
- 使用 `.lang-zh` 和 `.lang-en` 类标记不同语言的内容
- JavaScript 动态切换 `display` 属性
- 无需重新加载页面，切换流畅

---

## 🎯 快速部署到 GitHub Pages

### 方法1：网页界面（推荐，最简单）

1. **创建 GitHub 仓库**
   - 访问 [GitHub](https://github.com)
   - 点击右上角 "+" → "New repository"
   - 仓库名必须是：`你的用户名.github.io`
     - 例如：`weihualihk.github.io`
   - 设置为 **Public**
   - 点击 "Create repository"

2. **上传文件**
   - 在仓库页面点击 "uploading an existing file"
   - 拖拽 `index.html` 和 `style.css` 到页面
   - 填写 Commit message：`Initial commit - Bilingual homepage`
   - 点击 "Commit changes"

3. **启用 GitHub Pages**
   - 进入仓库的 **Settings**
   - 左侧菜单选择 **Pages**
   - Source 选择 **main** 分支
   - 点击 **Save**

4. **访问网站**
   - 等待 1-2 分钟（首次部署需要时间）
   - 访问 `https://你的用户名.github.io`

### 方法2：Git 命令行

```bash
# 1. 进入项目目录
cd d:/PhD/CV

# 2. 初始化仓库
git init
git add index.html style.css
git commit -m "Initial commit - Bilingual academic homepage"

# 3. 连接到 GitHub（先在网页创建仓库）
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git

# 4. 推送代码
git branch -M main
git push -u origin main

# 5. 在 GitHub 仓库设置中启用 Pages
```

---

## 📝 内容更新指南

### 更新个人信息

打开 `index.html`，搜索关键词并修改：

1. **照片**（第43行）
   ```html
   <img src="你的照片URL" alt="Weihua Li">
   ```

2. **社交链接**（第56-62行）
   ```html
   <a href="mailto:你的邮箱@hku.hk">
   <a href="https://github.com/你的用户名">
   <a href="https://www.researchgate.net/profile/你的ID">
   ```

3. **研究方向**（section#about）
   - 修改中英文研究兴趣列表
   - 注意使用正确的专业术语（如"冠层间隙率建模"而非"冠层空隙概率建模"）

### 更新工作经历

在 `<section id="experience">` 中的 `<div class="timeline">` 中添加或修改：

```html
<div class="timeline-item">
    <div class="timeline-marker work"></div>
    <div class="timeline-content">
        <h3>
            <span class="lang-zh">职位名称</span>
            <span class="lang-en" style="display: none;">Position Title</span>
        </h3>
        <p class="institution-name">
            <span class="lang-zh">机构名称</span>
            <span class="lang-en" style="display: none;">Institution Name</span>
        </p>
        <p class="time-period">
            <span class="lang-zh">2025年 - 至今</span>
            <span class="lang-en" style="display: none;">2025 - Present</span>
        </p>
        <p>
            <span class="lang-zh">导师：<a href="链接" target="_blank">导师名字</a></span>
            <span class="lang-en" style="display: none;">Supervisor: <a href="链接" target="_blank">Supervisor Name</a></span>
        </p>
    </div>
</div>
```

### 更新教育背景

在 `<section id="education">` 中修改学位信息，注意区分硕士、博士和联合培养经历。

### 添加新论文

在 `<div class="publications-list">` 中添加：

```html
<div class="publication-item">
    <div class="pub-year">2026</div>
    <div class="pub-content">
        <h3>论文标题</h3>
        <p class="pub-authors"><strong>Weihua Li</strong>, 合著者</p>
        <p class="pub-venue"><em>期刊名称</em> (2026)</p>
        <div class="pub-links">
            <a href="ResearchGate链接" target="_blank" class="pub-link">
                <i class="fas fa-link"></i> 
                <span class="lang-zh">ResearchGate</span>
                <span class="lang-en" style="display: none;">ResearchGate</span>
            </a>
            <!-- 如果有Open Access的PDF，添加： -->
            <a href="PDF直链" target="_blank" class="pub-link">
                <i class="fas fa-file-pdf"></i> 
                <span class="lang-zh">PDF</span>
                <span class="lang-en" style="display: none;">PDF</span>
            </a>
            <!-- 如果有代码，添加： -->
            <a href="GitHub链接" target="_blank" class="pub-link">
                <i class="fas fa-code"></i> 
                <span class="lang-zh">代码</span>
                <span class="lang-en" style="display: none;">Code</span>
            </a>
        </div>
    </div>
</div>
```

**注意**：
- 默认链接到 ResearchGate 页面
- 只在确认有 Open Access PDF 时才添加 PDF 按钮
- 使用 `<i class="fas fa-link"></i>` 图标表示链接到期刊/ResearchGate

### 添加新代表作品

在 `<section id="research">` 的 `<div class="projects-grid">` 中复制粘贴作品卡片模板：

```html
<div class="project-card">
    <div class="project-image">
        <img src="项目图片.jpg" alt="项目名称">
    </div>
    <div class="project-content">
        <h3>
            <span class="lang-zh">作品中文名</span>
            <span class="lang-en" style="display: none;">Work English Name</span>
        </h3>
        <p class="lang-zh">中文描述</p>
        <p class="lang-en" style="display: none;">English description</p>
        <div class="project-tags">
            <span class="tag">标签1</span>
            <span class="tag">标签2</span>
        </div>
        <a href="链接" target="_blank" class="btn-link">
            <span class="lang-zh">查看详情 →</span>
            <span class="lang-en" style="display: none;">View Details →</span>
        </a>
    </div>
</div>
```

### 更新统计数据

搜索 `stats-row`（约第95行），修改数字：

```html
<div class="stat-number">16</div>  <!-- 论文数 -->
<div class="stat-number">157</div> <!-- 引用数 -->
<div class="stat-number">3,668</div> <!-- 阅读量 -->
```

---

## 🎨 自定义配色方案

打开 `style.css`，修改第 8-17 行的 CSS 变量：

```css
:root {
    --primary-color: #2563eb;      /* 主色：蓝色 */
    --secondary-color: #1e40af;    /* 次色：深蓝 */
    --text-color: #1f2937;         /* 文字颜色 */
    /* ... */
}
```

**推荐配色：**
- 学术蓝（当前）：`#2563eb` / `#1e40af`
- 科研绿：`#059669` / `#047857`
- 专业灰：`#6b7280` / `#4b5563`
- 创新紫：`#7c3aed` / `#5b21b6`

修改头部背景渐变（第91行）：

```css
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

---

## 🔧 常见问题

### Q: 语言切换按钮不工作？
**A:** 检查以下几点：
1. 确保 HTML 中有 `<script>` 部分（文件末尾）
2. 检查浏览器控制台是否有 JS 错误
3. 确认所有语言标签都正确配对：`.lang-zh` 和 `.lang-en`

### Q: 图片显示不出来？
**A:** 
- 使用图床（如 Imgur、ImgBB）的直链
- 或将图片放在仓库中，使用相对路径
- ResearchGate 头像链接可能会失效，建议下载后重新上传

### Q: 修改后 GitHub Pages 没更新？
**A:** 
1. 等待 3-10 分钟（GitHub Pages 有缓存延迟）
2. 清除浏览器缓存：`Ctrl + Shift + R`（Windows）或 `Cmd + Shift + R`（Mac）
3. 使用无痕模式查看
4. 检查 GitHub Actions 是否成功运行（仓库的 Actions 标签页）

### Q: 如何添加新页面？
**A:** 
1. 创建新 HTML 文件（如 `publications.html`）
2. 复制 `index.html` 的头部和导航栏
3. 在导航菜单中添加链接：
   ```html
   <li><a href="publications.html">Publications</a></li>
   ```

### Q: 如何绑定自定义域名？
**A:**
1. 购买域名（如 Namecheap、GoDaddy）
2. 在 DNS 设置中添加记录：
   ```
   类型: CNAME
   名称: www
   值: 你的用户名.github.io
   ```
3. 在 GitHub 仓库根目录创建 `CNAME` 文件：
   ```
   www.yourname.com
   ```
4. 在 Settings → Pages 中填入域名

---

## 📊 内容管理建议

由于你希望我来维护，建议：

1. **定期更新论文**
   - 每发表新论文，提供标题、作者、期刊、链接
   - 我会帮你添加到网站

2. **项目更新**
   - 有新项目时提供描述、技术栈、链接
   - 我会创建新的项目卡片

3. **统计数据**
   - 定期告知 ResearchGate 上的最新数据
   - 我会更新统计数字

4. **版本控制**
   - 每次更新后我会用 Git 提交
   - 保留修改历史，可随时回滚

---

## 🌟 进阶功能（可选）

### 添加 Google Analytics

在 `</head>` 前添加：

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-你的ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-你的ID');
</script>
```

### 添加访问统计

可以使用 [shields.io](https://shields.io) 添加徽章：

```html
<img src="https://img.shields.io/github/last-commit/yourusername/yourusername.github.io">
```

### 添加 PDF 简历

1. 生成 PDF 简历
2. 上传到仓库
3. 在页面添加下载链接：
   ```html
   <a href="CV-Weihua-Li.pdf" download class="btn-primary">
       <i class="fas fa-download"></i> Download CV
   </a>
   ```

---

## 📨 维护与更新

由于您希望我来维护网站，请按以下方式提供更新：

### 论文发表更新模板

```
新论文发表：
- 标题：（中英文）
- 作者：（标注您的名字位置）
- 期刊/会议：（全称和缩写）
- 年份、月份：
- PDF链接：（如有）
- 代码链接：（如有）
```

### 项目更新模板

```
新研究项目：
- 项目名称：（中英文）
- 简短描述：（中英文，50-100字）
- 使用技术：
- 项目链接：（论文、GitHub、网站等）
- 项目图片：（可选，提供图片URL）
```

### 统计数据更新

```
ResearchGate 最新数据：
- 论文数：
- 引用数：
- 阅读量：
```

---

## 🔐 安全与隐私

- ✅ 邮箱已公开（学术邮箱）
- ✅ ORCID已公开（学术标识）
- ⚠️ 如不想公开具体办公室地址，可删除该部分
- ⚠️ 个人照片使用学术照片，注意隐私

---

## 🎓 学术网站最佳实践

1. **保持更新** - 每季度更新一次论文和项目
2. **简洁明了** - 突出最重要的研究成果
3. **易于联系** - 邮箱清晰可见
4. **专业照片** - 使用正式学术照片
5. **移动友好** - 大量访问来自手机
6. **快速加载** - 优化图片大小

---

## 📖 技术文档

### HTML 结构

```
index.html
├── <head>           # 元数据、样式、字体
├── <nav>            # 导航栏 + 语言切换
├── <header.hero>    # 头部横幅
├── <section#about>  # 关于我
├── <section#education>  # 教育背景
├── <section#research>   # 研究项目
├── <section#publications> # 论文列表
├── <section#contact>    # 联系方式
├── <footer>         # 页脚
└── <script>         # 交互功能
```

### CSS 架构

```css
/* 全局变量 */
:root { --primary-color, --secondary-color, ... }

/* 组件样式 */
.navbar, .hero, .section, .timeline, .project-card, ...

/* 响应式 */
@media (max-width: 768px)  { 平板/手机样式 }
@media (max-width: 480px)  { 小屏手机样式 }
```

### JavaScript 功能

- `toggleLanguage()` - 语言切换
- 导航菜单切换（移动端）
- 平滑滚动
- 导航栏滚动效果

---

## 🚀 性能优化建议

1. **图片优化**
   - 使用 WebP 格式（更小体积）
   - 压缩到合适大小（<200KB）
   - 懒加载：`<img loading="lazy">`

2. **字体优化**
   - 只加载需要的字重
   - 使用 `font-display: swap`

3. **代码压缩**
   - HTML/CSS 压缩（可选）
   - 移除未使用的 CSS

---

## 📦 备份与版本控制

**当前文件：**
- `index.html` - 最新双语版本
- `index-old.html` - 原始单语版本备份
- `style.css` - 样式文件
- `README.md` - 说明文档

**建议备份策略：**
1. 每次修改前自动备份
2. 使用 Git 版本控制
3. 定期导出完整项目

---

## 🌍 SEO 优化

已实现：
- ✅ 语义化 HTML 标签
- ✅ Meta 描述和关键词
- ✅ Open Graph 标签（可增强）
- ✅ 响应式设计
- ✅ 快速加载速度

可增强：
- 添加 `sitemap.xml`
- 添加 `robots.txt`
- 结构化数据（Schema.org）

---

## 🔗 有用的链接

- [GitHub Pages 文档](https://docs.github.com/pages)
- [Markdown 指南](https://www.markdownguide.org/)
- [Font Awesome 图标](https://fontawesome.com/icons)
- [Google Fonts](https://fonts.google.com/)
- [Can I Use](https://caniuse.com/) - 浏览器兼容性
- [PageSpeed Insights](https://pagespeed.web.dev/) - 性能测试

---

## 📞 联系方式

**网站所有者：**
- 李伟华（Weihua Li）
- Email: weihuahk@hku.hk
- Institution: HKU Department of Geography

**网站维护：**
- 由 AI 助手协助维护
- 需要更新时请提供信息，我会及时处理

---

## 📜 更新日志

### 2026-03-12 (v3.0)
- ✅ 移除统计数据展示（16 Publications, 157 Citations, 3,668 Reads）
- ✅ 为代表作品添加代码按钮
- ✅ 地形校正模型添加 Google Earth Engine 代码链接
- ✅ 热点效应建模添加 GitHub 代码链接（PATH_LiDAR 和 PATH_RT_T）
- ✅ 分形维数 LAI 校正添加 GitHub 代码链接（PATH_LiDAR）
- ✅ 通过 ResearchGate 核实论文信息准确性
- ✅ 确认所有论文作者列表和链接的正确性
- ✅ 修正两篇DART论文期刊名称：从Remote Sensing of Environment改为Journal of Remote Sensing
- ✅ 更新Google Scholar个人主页链接
- ✅ 移除分形LAI论文的代码按钮（代码未开源）
- ✅ 为热点效应建模代码按钮添加详细说明（激光雷达波形模拟和植被BRDF模拟）
- ✅ 更新邮箱地址：weihualihk@hku.hk → weihuahk@hku.hk
- ✅ 简化"关于我"部分，聚焦智慧建模与制图，删除重复的教育经历描述
- ✅ 删除教育背景中的专业名称（博士-遥感、硕士-遥感、学士-资源与环境）
- ✅ 删除奖项荣誉section（暂时不展示）

### 2026-03-12 (v2.0)
- ✅ 添加 GitHub 链接（https://github.com/BNUL）
- ✅ 修正香港大学链接为地理系官网
- ✅ 创建独立的"工作经历"部分
- ✅ 更新博士后合作导师为宫鹏教授
- ✅ 更新博士后研究方向：多源数据融合的辐射传输智慧建模以及全球智慧制图
- ✅ 完善教育背景时间线（区分硕士2018-2020和博士2020-2025）
- ✅ 添加博士导师阎广建教授及研究方向
- ✅ 添加硕士导师穆西晗副教授及研究方向
- ✅ 添加法国联合培养导师 Jean-Philippe Gastellu-Etchegorry 教授
- ✅ 添加 CESBIO 实验室超链接
- ✅ 修正术语："冠层空隙概率建模"改为"冠层间隙率建模"
- ✅ "研究项目"更名为"代表作品"
- ✅ 论文链接改为 ResearchGate（非 Open Access 不显示 PDF）

### 2026-03-12 (v1.0)
- ✅ 创建中英双语个人主页
- ✅ 实现一键语言切换功能
- ✅ 添加李伟华完整学术信息
- ✅ 集成 ResearchGate 数据
- ✅ 添加 16 篇论文列表
- ✅ 创建 3 个研究项目展示
- ✅ 实现响应式设计
- ✅ 优化移动端显示

---

## ⭐ 特别说明

这个网站：
1. **完全免费** - 无需付费服务器
2. **易于维护** - 只需编辑 HTML
3. **国际化友好** - 中英双语无缝切换
4. **学术专业** - 专为研究人员设计
5. **长期稳定** - GitHub Pages 稳定可靠

**下一步：**
请在 GitHub 创建仓库并部署，部署成功后将链接发给我，我可以继续优化和维护。

---

**© 2026 Weihua Li. Website maintained with AI assistance.**
