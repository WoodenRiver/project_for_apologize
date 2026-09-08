# project_apologize

一个部署在 GitHub Pages 上的道歉小网站：点一下按钮，小人就会深深鞠躬道歉，附带随机俏皮文案和语音朗读；语音播完，小人站回原位。主题：宝宝，对不起忘记了你的生日。

## 本地预览

直接双击打开 `index.html` 即可，或起一个本地服务：

```bash
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 部署到 GitHub Pages

1. 推送本仓库到 GitHub
2. 仓库 Settings → Pages → Source 选择 `main` 分支 `/ (root)`
3. 约 1 分钟后访问 `https://WoodenRiver.github.io/project_apologize/`

## 部署前必做

- 把 `index.html` 标题里的 `{宝宝名字}` 替换成真实昵称

## 自定义

- **文案**：编辑 `main.js` 顶部的 `LINES` 数组
- **小人图片**：替换 `Cartoon/apologize1.png`（站姿）与 `Cartoon/apologize2.png`（鞠躬）即可
- **语音替换为录音**：改写 `main.js` 中的 `speakApology()` 函数，改为播放音频文件（`onEnd` 改挂 `audio.onended`），其余逻辑无需改动

详细设计见 `设计文档.md`。
