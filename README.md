# 纽斯珊瑚灯可视化编辑器（GitHub Pages 自动构建版）

这是一个适合部署到 **GitHub Pages** 的版本。  
它不是直接引用 CDN，而是通过 **GitHub Actions 在云端自动安装 npm 依赖并构建**。

## 这版解决了什么
- 不需要你本地装 Python
- 不依赖 CDN 的 `qrcode.js` / `jsQR` 外链
- 二维码生成使用 `qrcode` npm 包
- 二维码识别使用 `jsqr` npm 包
- 依赖由 GitHub Actions 自动安装和打包

## 使用步骤
1. 新建 GitHub 仓库
2. 把这个文件夹里的全部文件上传到仓库根目录
3. 打开仓库的 **Settings → Pages**
4. 在 **Build and deployment** 中选择 **GitHub Actions**
5. 确保默认分支是 `main`
6. 推送后等待 Actions 跑完
7. 部署完成后会得到 Pages 地址

## 目录结构
- `index.html`
- `src/main.js`
- `src/styles.css`
- `package.json`
- `vite.config.js`
- `.github/workflows/deploy.yml`

## 本地开发（可选）
如果你自己也想本地运行：
```bash
npm install
npm run dev
```

## 说明
- 这版适合你“多设备直接访问”的需求
- GitHub 会在云端完成依赖安装和构建
- 你平时只需要更新源码然后 push
- 原始串格式为：`手动模式六通道亮度 HEX（12 位）#24 组 16 位时序数据`
- 例如 `323232323232` 表示手动模式下 6 个光通道各自的亮度头部值，不是单纯的固定前缀
