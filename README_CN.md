# wplace-bot

[wplace.live](https://wplace.live) 自动填涂脚本。Tampermonkey 用户脚本，fork 自 [Readixyee/wplace-bot](https://github.com/Readixyee/wplace-bot)。

[English](README.md)

## 新增功能

- **自动填涂循环** — 勾选 Auto draw 后每轮画完自动倒计时下一轮
- **智能定时器** — 根据颜料上限动态计算间隔（charges × 30s + 15s），等级越高等待越久
- **一键确认** — 所有像素预览完毕后自动点击 Paint 按钮确认

## 快速安装

1. 装 [Tampermonkey](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
2. 打开 [dist.user.js](https://github.com/rD227/wplace-bot/raw/master/dist.user.js)，点 Install
3. `chrome://extensions` → Tampermonkey → 详情 → 允许用户脚本
4. 打开 wplace.live，bot 面板自动出现

## 使用

1. 拖入图片或 `.wbot` 导出文件
2. 拖拽图片边缘调整位置
3. 可选：调整颜色顺序、策略等
4. 勾选 **Auto draw** 开启自动循环
5. 点 **Draw** 开始

## 构建

需要 [Bun](https://bun.sh)：

```bash
bun install
bun start     # 生成 dist.user.js
```

修改源文件后重建：

```bash
bun start && cp dist.user.js ~/Downloads/
```

## 更新脚本

构建后在 Tampermonkey Dashboard 中编辑脚本，粘贴 `dist.user.js` 保存。

或者等 Tampermonkey 自动检测 `@updateURL` 提示更新。

## License

MPL-2.0 — 继承自 [SoundOfTheSky/wplace-bot](https://github.com/SoundOfTheSky/wplace-bot)
