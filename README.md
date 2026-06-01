# Study Hall · 静室自习室

一个安静、沉浸的虚拟自习室网页。选择学习场景、调节专注音乐与环境声、设置番茄钟，还能和朋友一起进入"同房自习"的氛围。

A calm virtual study room: pick a scene, tune focus sounds, run a pomodoro timer, and study alongside friends.

## 功能

- **三种页面流程**：落地页 → 场景选择 → 沉浸自习室
- **四种场景**：清晨窗边、雨天咖啡店、深夜图书馆、海边书房
- **番茄钟**：25 / 45 / 50 / 90 分钟，专注与休息自动循环
- **声音**：浏览器实时合成的环境白噪音，无需任何音频文件，断网也能响
- **沉浸模式**：一键淡出所有辅助界面，只留计时与呼吸光晕
- **朋友联动**：生成房间号分享、同房伙伴列表、今日专注排行榜（演示版为本地模拟）
- **中英文切换**，并记住你上次的语言、场景与番茄钟偏好
- 计时进行时，浏览器标签标题会显示剩余时间

> 整个网站是**单个 HTML 文件**，没有任何依赖、无需构建，直接打开即可运行。

## 发布到 GitHub Pages

1. 在 GitHub 新建一个仓库（例如 `study-hall`），设为 **Public**。
2. 把 `index.html` 上传到仓库根目录。（在仓库页点 **Add file → Upload files**，拖入即可，然后 **Commit changes**。）
3. 进入仓库的 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
5. **Branch** 选 `main`，文件夹选 `/ (root)`，点 **Save**。
6. 等一两分钟，页面顶部会出现网址，形如：
   `https://你的用户名.github.io/study-hall/`

打开这个网址就是你的线上自习室了，可以直接分享给朋友。

### 想用自己的域名？

在 **Settings → Pages → Custom domain** 填入你的域名，并按提示在域名服务商处添加一条 CNAME 记录指向 `你的用户名.github.io`。

## 关于"朋友联动"

目前的房间号、伙伴和排行榜是**本地模拟**，用于展示交互效果——朋友输入房间号还连不到你这边。要做成真正的多人实时同步，需要接一个后端（如 Firebase 或 Supabase，都有免费额度）。这一步可以作为下一阶段的升级。

## 自定义提示

- **换场景图片**：在 `<script>` 里的 `SCENES` 数组中替换 `img` 的链接（建议用稳定的图床，约 1600px 宽）。
- **改主题色**：在 `:root` 里改 `--accent`（金色）等 CSS 变量。
- **加场景**：复制 `SCENES` 里的一项，填好中英文名称、描述和图片即可。

---

本项目使用浏览器原生 HTML/CSS/JS，无第三方框架。字体来自 Google Fonts，背景图来自 Unsplash。
