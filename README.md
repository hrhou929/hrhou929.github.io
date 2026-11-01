# Haoran Hou — Personal Website

为 `https://hrhou929.github.io/` 准备的个人学术主页。纯 HTML/CSS/JavaScript，无需安装依赖或运行构建。

## 先预览

解压后双击 `index.html`。点击 Home、Experience、Beyond 切换内容，点击 CV 查看可打印简历。CV 页面点击 Print / Save PDF，再在浏览器打印窗口选择保存为 PDF。

## 发布到 GitHub Pages

1. 登录 `hrhou929`，打开 https://github.com/new 。
2. Repository name 输入 **hrhou929.github.io**，选择 **Public**，勾选 Add a README file，然后创建仓库。
3. 在仓库点击 **Add file → Upload files**。上传本文件夹里面的 `index.html`、`cv.html`、`assets` 文件夹。不要把整个 `personal-homepage` 外层文件夹上传进去；`index.html` 必须在仓库根目录。
4. 提交文件后打开 **Settings → Pages**。
5. Source 选 **Deploy from a branch**，Branch 选 **main**，Folder 选 **/ (root)**，保存。
6. 等待部署完成，访问 **https://hrhou929.github.io/**。部署结果可在仓库 Actions 或 Settings → Pages 查看。

`.nojekyll` 可以一并上传，用于声明不使用 Jekyll；本网站不依赖该文件才能工作。README 不需要作为网页内容上传。

## 内容和编辑

- `index.html`：主页文案、样式、分区切换逻辑。
- `cv.html`：为网站整理的公开简历页面，基于最新 CV，不是原文件的逐字复制；保留邮箱，未展示电话与 GPA。
- `assets/favicon.svg`：浏览器标签页图标。
- 第一版采用姓名首字母作为头像，未使用他人的照片或生活照片。
- 首页文案基于 `HOU_Haoran_CV_tpg(1).docx` 和 `HOU Haoran_General Personal Statement.pdf`。
- 论文作者和标题已对照 arXiv 核实。ICSE 2027 状态按 CV 标注为 **major revision**，尚未标注为 accepted。
- 参考 Jinghan Yang 主页的信息组织方式，重新编写页面，没有复制其自我介绍、图片或源代码。
- 本版本未加入未经 CV / PS 确认的其他经历；可以后续补充交换经历、项目链接、Google Scholar 等。

### 更换头像

把自己的头像放到 `assets/portrait.jpg`，将 `index.html` 中的：

```html
<div class="portrait" aria-label="Haoran Hou initials"><span>HH</span></div>
```

替换为：

```html
<img class="portrait" src="assets/portrait.jpg" alt="Haoran Hou" style="object-fit:cover">
```

### 换成 PDF 简历下载

将确认过的 PDF 放到 `assets/Haoran_Hou_CV.pdf`，把 `index.html` 中两处 `href="cv.html"` 都改为 `href="assets/Haoran_Hou_CV.pdf"`。

## 文件检查与已知限制

已检查 HTML 结构中的标题、导航、ID、内部链接及本地资源路径；页面使用响应式布局、键盘焦点和系统字体。未进行真实浏览器的桌面 / 手机渲染检查。当前文件仅完成本地制作，尚未发布到 GitHub Pages。

发布指南：https://docs.github.com/en/pages/quickstart
