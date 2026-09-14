# 实验史记·春秋笔

据 音克思《实验史记》改编的第二款游戏（第一款是「实验史记·马刀风云」，回合制对战）。
本作是完全不同的类型：**校园探索 + 社交养成 + 撰史经营**——玩家扮演史官音克思，
在校园里行走、结识书中人物、亲历名场面收集史料、把十五卷史记写出来。

## 运行 / 交付

- 双击 `实验史记·春秋笔.html` 即玩（单文件、无依赖、无网络）。
- 交付目录：`C:\Users\LENOVO\Desktop\实验史记·春秋笔\`（html + 玩法说明.txt）。

## 开发

```
python build.py      # 把 index.html + css + js 打包成单文件 html
node smoke.mjs       # playwright 冒烟测试 + 截图到 testshots/（需在 D:\code 下运行，依赖其 node_modules）
```

- 源码结构：`js/data/`（people/items/scenes/events/volumes 数据）+ `engine/world/dialog/writing/minigames/ui/main`。
- 台词与史料引文基本照抄《实验史记》原文（桌面 `实验史记  音克思著.docx`）。
- UI 遵循 apple-design skill（玻璃材质、弹簧动画、按时段切换晨昏主题）。
- 改数据不用改逻辑：加人物 → `people.js`；加名场面 → `events.js`；加卷 → `volumes.js`。
