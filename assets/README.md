# 版画插画接入

`illustration-catalog.json` 包含 80 个剧情事件及 6 个天选事件的路径和 Prompt 备忘。当前未批量生成图片，缺图时使用内置 CSS 徽章，游戏可完整离线游玩。

- 事件图片放在 `assets/events/<事件 id>.webp`，例如 `tang_1.webp`、`MEDIEVAL_1.webp`。
- 每年的图片放在 `assets/years/<epochId>_<regionId>_<year>.webp`，例如 `MEDIEVAL_East_Asia_750.webp`。公元前年份保留负号，例如 `PRIMITIVE_Nordic_-5000.webp`。
- 推荐 1280×720、16:9、无文字、单色交叉排线版画。图片展示时自动施加统一的棕褐色滤镜。
- 自定义事件可填写 `year`、`image`、`imagePrompt`、`artType`。`artType` 支持 `book`、`scales`、`swords`、`coins`、`medicine`、`hourglass`。
- 事件历史保存实际发生年份、图片路径与 Prompt；旧存档没有这些字段时，会按事件标题补齐展示。
- 插画按需加载，8 秒超时或加载失败时自动隐藏图片并展示徽章。替换图片后刷新页面或重新读取存档即可重试。

游戏逻辑仍在根目录 `index.html` 中；附加插画后，分享或部署时请同时携带 `assets` 目录。
