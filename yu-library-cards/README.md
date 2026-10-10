# Yu · Library Cards (v0.1)

一个可持续生长的个人卡片盒。当前只有一张卡片：GPT + Terminal 修改网站。

## 本地预览

双击 `index.html` 即可在浏览器打开（与 `cards.js` 保持在同一文件夹）。

## 修改卡片

**方式 A：网页上编辑**

点击卡片右上角「编辑」，修改内容，点击「保存并下载 cards.js」。将下载的 `cards.js` 替换网站文件夹里的旧版本。注意：浏览器无法直接把修改写入 GitHub，刷新前务必下载并替换文件。

**方式 B：Terminal 编辑**

直接编辑 `cards.js` 中的卡片对象。以后也可以让 GPT 生成一段 Terminal 可粘贴执行的修改命令。

每张卡包含 `id`、`drawer`、`title`、`trigger`、`action`、`tags`、`links`。`links` 填其他卡片 ID，例如 `['002']`，对应卡片存在后就会显示链接。

## 发布到已有 GitHub Pages

建议把整个 `yu-library-cards` 文件夹复制到现有网站仓库根目录，保留里面的 `index.html` 和 `cards.js`。例如：

```bash
cd /path/to/your/github-pages-repo
git add yu-library-cards/
git commit -m "Add library cards"
git push origin main
```

如果仓库 Pages 从 main 根目录发布，访问路径一般是：
`https://yu-tao-5.github.io/yutao.github.io/yu-library-cards/`

如果 Pages 使用其他分支或目录，请按实际配置调整。

## 下一步（以后再做）

更多卡片、双向关联、图谱、分类、快捷编辑，都可以在现有数据结构上逐步增加。当前不需要数据库或构建工具。
