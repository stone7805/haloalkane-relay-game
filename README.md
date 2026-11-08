# 卤代烃命名接接乐 V1.1 · 全氢蛛网式

单文件、离线可玩的课堂网页游戏，延续接接乐的单人/双人、左右独立十轮、四选一落下名称、道具提示、错误暂停重试、逐侧计分、声音与本地记录。

## 学习内容

两档分别为“结构辨名”和“定位命名”；前 3 轮练简单一卤代烷，共得 60 分，后 7 轮练卤素位置、双卤取代及甲基支链。题卡采用全氢蛛网式：每个碳、每个氢、每个卤素以及相连的化学键均单独画出，甲基支链的三个氢也不省略。位标辅助观察，命名时仍须按较小定位号选编号方向。本版只覆盖简单饱和开链卤代烷，不含复杂母体或立体异构。

## GitHub Pages 发布

1. 在 GitHub 新建仓库，例如 `haloalkane-relay-game`。
2. 将发布包内 `index.html` 上传到仓库根目录；`README.md` 可一同上传。请勿把整个 ZIP 当成网页入口直接上传。
3. 打开仓库 **Settings → Pages → Build and deployment**，选 **Deploy from a branch**，设置 **main / (root)** 并保存。
4. 等 Pages 显示已发布网址再打开；未发布前不能把示例地址当成现成链接。

`index.html` 也可本地直接打开。成绩只存在当前浏览器，清理站点数据可能丢失，不能作为正式考试凭证。

## 题库维护

`skill/build-learning-relay-game/` 保留已复刻的接接乐技能和校验/生成脚本；`卤代烃题库素材.json`、`生成题库.py`、`question-bank.json` 是本游戏题库与可复现源。修改题意或结构后先核查化学正确性，再运行：

```text
python 生成题库.py
python skill/build-learning-relay-game/scripts/validate_relay_bank.py question-bank.json
python skill/build-learning-relay-game/scripts/build_relay_game.py question-bank.json index.html
```

修改规则或学科内容时，请同步提升版本号、浏览器存储键并重新验收；最后一条只覆盖本项目目录里的 `index.html`，不会碰你最初上传的根目录文件。
