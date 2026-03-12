# 🚀 快速部署指南

## 3步部署到 GitHub Pages

### 第1步：创建 GitHub 仓库（2分钟）

1. 访问 https://github.com
2. 点击右上角 **"+"** → **"New repository"**
3. **仓库名必须是：`你的用户名.github.io`**
   - 例如：`weihualihk.github.io`
   - ⚠️ 注意：用户名要和你的 GitHub 用户名完全一致
4. 选择 **Public**（公开）
5. 不要勾选 "Add a README file"
6. 点击 **"Create repository"**

### 第2步：上传文件（3分钟）

**方法A：网页上传（推荐，最简单）**

1. 在新建的仓库页面，点击 **"uploading an existing file"**
2. 拖拽以下文件到页面：
   - ✅ `index.html`
   - ✅ `style.css`
3. 页面底部：
   - Commit message 填写：`Initial commit - My academic homepage`
   - 点击 **"Commit changes"**

**方法B：Git 命令行**

```bash
cd d:/PhD/CV
git init
git add index.html style.css
git commit -m "Initial commit"
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
git branch -M main
git push -u origin main
```

### 第3步：启用 GitHub Pages（1分钟）

1. 在仓库页面，点击 **Settings**（设置）
2. 左侧菜单找到 **Pages**
3. 在 "Build and deployment" 部分：
   - **Source**: 选择 **Deploy from a branch**
   - **Branch**: 选择 **main** → **/ (root)** → **Save**
4. 等待 1-3 分钟
5. 刷新页面，顶部会显示：
   ```
   ✅ Your site is live at https://你的用户名.github.io
   ```

### 🎉 完成！

访问：`https://你的用户名.github.io`

---

## ⚡ 快速测试

部署后测试以下功能：

- [ ] 页面能正常打开
- [ ] 点击右上角 🌐 按钮，中英文切换正常
- [ ] 导航菜单能跳转到各部分
- [ ] 社交链接能正常打开
- [ ] 手机访问显示正常

---

## 🔄 以后如何更新？

### 方法1：网页编辑（推荐）

1. 在 GitHub 仓库中点击 `index.html`
2. 点击铅笔图标 ✏️ **Edit**
3. 修改内容
4. 底部填写 Commit message
5. 点击 **Commit changes**
6. 等待 1-2 分钟，网站自动更新

### 方法2：本地修改后推送

```bash
cd d:/PhD/CV
# 修改文件...
git add .
git commit -m "Update publications"
git push
```

---

## ❓ 常见问题

### Q1: 网站显示 404 错误？
**原因**：
- 仓库名错误（必须是 `用户名.github.io`）
- Pages 没有启用
- 文件名不是 `index.html`

**解决**：
1. 检查仓库名是否正确
2. 确认 Settings → Pages 已启用
3. 确认文件名是 `index.html`（全小写）

### Q2: 样式显示不正常？
**原因**：CSS 文件没有上传或路径错误

**解决**：
1. 确认 `style.css` 已上传
2. 确认两个文件在同一目录
3. 清除浏览器缓存（Ctrl + Shift + R）

### Q3: 语言切换不工作？
**原因**：JavaScript 被浏览器拦截

**解决**：
1. 确认 HTML 末尾有 `<script>` 部分
2. 按 F12 打开开发者工具，查看 Console 是否有错误
3. 尝试其他浏览器

### Q4: 修改后没生效？
**原因**：GitHub Pages 缓存或浏览器缓存

**解决**：
1. 等待 3-5 分钟
2. 清除浏览器缓存：`Ctrl + Shift + R`
3. 使用无痕模式查看
4. 检查 GitHub Actions 是否成功（Actions 标签页）

### Q5: 图片不显示？
**原因**：
- 图片链接失效
- 网络问题

**解决**：
1. ResearchGate 头像可能会失效，建议：
   - 下载图片到本地
   - 上传到仓库
   - 修改 HTML：`<img src="photo.jpg">`
2. 或使用图床：Imgur、ImgBB

---

## 📱 移动端测试

在手机上访问网站，测试：

1. **汉堡菜单**：点击右上角三条杠
2. **语言切换**：点击 🌐 按钮
3. **平滑滚动**：点击菜单项
4. **社交链接**：点击邮箱、RG图标
5. **响应式**：旋转手机，横竖屏都正常

---

## 🎯 部署检查清单

- [ ] GitHub 仓库已创建
- [ ] 仓库名正确：`用户名.github.io`
- [ ] index.html 已上传
- [ ] style.css 已上传
- [ ] GitHub Pages 已启用
- [ ] 网站可以访问
- [ ] 语言切换正常
- [ ] 导航功能正常
- [ ] 移动端显示正常
- [ ] 社交链接正确

---

## 📞 需要帮助？

如果遇到问题：

1. **查看 GitHub Pages 文档**：https://docs.github.com/pages
2. **检查 GitHub Status**：https://www.githubstatus.com/
3. **告诉我具体错误信息**，我会帮你解决

---

## 🎓 部署后建议

1. **分享链接**
   - 添加到简历
   - 添加到 ResearchGate 个人资料
   - 添加到邮件签名

2. **提交到搜索引擎**
   - [Google Search Console](https://search.google.com/search-console)
   - [Bing Webmaster Tools](https://www.bing.com/webmasters)

3. **定期更新**
   - 每发表新论文及时添加
   - 每季度更新统计数据
   - 保持内容新鲜

---

**祝你部署成功！🚀**
