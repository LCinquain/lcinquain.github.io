# 个人主页：部署与待办

## 文件结构

```
index.html            主页（单文件，CSS 和 JS 都已内联）
images/profile.jpg    头像占位图 → 换成你的照片，建议正方形，约 400×400
images/sketch.png     SKETCH 配图（已取自论文 Table 1 第一个定性对比图，可自行替换）
images/policy-memory.png  TMLR 论文配图占位 → 同上
images/logo-*.png     CUHK-Shenzhen、华为、中远海运的标（取自 Wikimedia）
```

替换图片时直接用**同名文件覆盖**即可，不需要改 HTML。图片尽量压缩到 200 KB 以内。

## 上线前必须改的地方（在 index.html 里搜 `TODO`）

- [x] GitHub 链接（已填好）
- [x] SKETCH 的 PMLR、arXiv、Code 链接（已填好）
- [ ] 头像和 TMLR 论文配图换成真实图片（SKETCH 配图已放好）
- [x] SKETCH 的 BibTeX 已按 PMLR 官方条目填写（作者名已更正为 Li, Xingjian，见下）

## PMLR 上你的名字顺序是反的

PMLR 页面和官方 BibTeX 里把你写成了 `Li Xingjian`（BibTeX 为 `Xingjian, Li`，即姓被当成了 Xingjian）。别人直接复制官方 BibTeX 引用时，会引成 "L. Xingjian"，也可能影响 Google Scholar 的归档。页面右上角有个 [edit] 链接，指向 PMLR 的 GitHub 仓库（mlresearch/v306），可以提一个 pull request 改掉；也可以联系 ICML 的 proceedings chair。

## 建议确认的内容

- **Ongoing research**：两个 CDLM 项目都只写了研究问题，没有写任何实验发现。第一个项目由学长主导，上线前可以跟胡老师或学长说一声。
- **Huawei capstone**：只写了方法思路，没有放数字。如果项目有保密要求，需要再确认一下。
- 侧栏的 CV 链接目前指向主页本身（占位）。CV 暂不公开：完整版含手机号、组内未发表的阶段性发现和华为项目数字。以后做好公开版（去掉手机号、EDCLM 只写问题、华为去掉数字）后，把 PDF 命名为 cv.pdf 放进根目录，再把 index.html 里 CV 链接的 href="./" 改成 href="cv.pdf"。
- 所有日期和论文状态都已与 CV 对齐；TMLR 那篇在主页上写作 arXiv preprint（避免公开关联正在双盲评审的投稿），接收后改为 Transactions on Machine Learning Research (TMLR), 2026，并换成官方 BibTeX。

## 部署到 GitHub Pages（约 10 分钟）

1. 登录 GitHub，新建一个仓库，名字必须是 `你的用户名.github.io`，设为 Public。
2. 把这个文件夹里的所有文件上传到仓库根目录（网页上点 "Add file → Upload files" 拖进去即可）。
3. 进入仓库的 Settings → Pages，Source 选 "Deploy from a branch"，Branch 选 `main`、目录选 `/ (root)`，保存。
4. 等一两分钟，访问 `https://你的用户名.github.io` 即可。

本地预览：直接双击 `index.html` 用浏览器打开。

## 上线后

- 在手机上打开检查一遍，确认所有链接都能点开。
- 把主页链接加到：CV 抬头、邮件签名、Google Scholar 个人资料的 "Homepage" 字段、GitHub 个人资料。
- 页面会自动适配浅色和深色模式。
- 侧栏图标来自 Font Awesome Free 6.5.2（CC BY 4.0），已内联在 HTML 里，不依赖外部加载；署名注释保留在源码中，不要删。
- 字体用的是系统字体，没有引用 Google Fonts，这样在大陆访问也不会卡顿。
