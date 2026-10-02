# PDF 逐页转图片

把 PDF 每一页转成图片，逐页预览、逐页下载。**全程在浏览器里完成 —— 文件不会上传到任何服务器。**

## 🌐 在线使用

https://yalways17.github.io/pdf2image/

## ✨ 功能

* 📄 选一个 PDF，自动逐页渲染
* 🖼️ 每页一张预览卡 + 「点击下载」，存成 `page-1.jpg`、`page-2.jpg`…
* 📱 **移动端优先** —— 手机上长按图片即可存入相册
* 🔍 固定 2× 渲染（约 144 DPI），Retina 屏上清晰
* 🗜️ 输出 JPEG（质量 0.9）—— 手机上比 PNG 省内存得多
* ⏳ 转换过程有逐页进度提示（正在转换第 N / M 页）

## 🔒 隐私

pdf.js 在你自己的浏览器里渲染，**没有上传步骤，也没有后端** —— PDF 内容不会离开你的设备。

首次打开需要联网从 CDN 取一次 pdf.js；之后断网也能用。

## ⚠️ 目前不可调的部分

* 页码范围、DPI、输出格式**固定**（全部页 / 2× / JPEG）
* 没有打包下载，只能逐页点
* 页数很多的 PDF 会把所有页同时留在页面上，手机上可能吃内存

> 这些不是 bug，是这一版刻意做简的结果。`_alt-full-version.html` 里有一份功能更全的备用实现（页码范围、36–600 DPI、JPEG/PNG、打包 zip、可取消），需要时可以换上去。

## 🛠️ 技术

单文件 HTML + [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174（来自 cdnjs）

## 📦 部署

```powershell
.\_pub.ps1
```

需要 GitHub PAT 放在 `C:\Users\26290\.dsh\gh_token.txt`，权限：**Contents: Read and write**（想自动开 Pages 还需 Pages 权限）。

---

**PDF 逐页转图片 · v.1.0.0**
