# 《桑野与露娜》写作工程

这是《桑野与露娜》的 GitHub 写作仓库初始化文档包。

当前版本只包含：

- 全局提示词
- 故事圣经
- 人物档案
- 世界观档案
- 30 章总大纲
- 章节节拍表
- 风格指南
- 连续性记录
- 术语表
- 未解决伏笔表
- 修改记录
- AI 写作/修订/连续性检查提示词

当前版本**不包含小说正文**。正式正文后续放入 `chapters/` 目录，每章一个 Markdown 文件。

---

## 项目定位

《桑野与露娜》是一部长篇轻小说体量的古风科幻爱情冒险故事。

它的核心不是“复活爱人”，而是：

> 一个被爱人温柔保护过的少女，在爱人死亡后，被爱人的善意谎言推着成长；她以为自己在寻找复活他的办法，最终却学会放手，带着他的那一份继续活下去。

---

## 推荐仓库结构

```text
sangye-luna-writing-kit/
├─ README.md
├─ docs/
│  ├─ 00_GLOBAL_PROMPT.md
│  ├─ 01_STORY_BIBLE.md
│  ├─ 02_CHARACTER_BIBLE.md
│  ├─ 03_WORLD_BIBLE.md
│  ├─ 04_PLOT_OUTLINE.md
│  ├─ 05_CHAPTER_OUTLINE.md
│  ├─ 06_STYLE_GUIDE.md
│  ├─ 07_CONTINUITY_LOG.md
│  ├─ 08_TERMS_GLOSSARY.md
│  ├─ 09_UNRESOLVED_THREADS.md
│  └─ 10_REVISION_NOTES.md
├─ chapters/
│  └─ .gitkeep
├─ drafts/
│  └─ .gitkeep
├─ prompts/
│  ├─ chapter_writing_prompt.md
│  ├─ revision_prompt.md
│  └─ continuity_check_prompt.md
└─ archive/
   └─ .gitkeep
```

---

## 每写完一章后的维护流程

1. 将正文保存到 `chapters/chXX_章节名.md`。
2. 更新 `docs/07_CONTINUITY_LOG.md`，记录本章事实、伏笔、人物状态变化。
3. 若新增人物、地点、能力或术语，更新：
   - `docs/02_CHARACTER_BIBLE.md`
   - `docs/03_WORLD_BIBLE.md`
   - `docs/08_TERMS_GLOSSARY.md`
4. 若埋下或回收伏笔，更新 `docs/09_UNRESOLVED_THREADS.md`。
5. 若调整设定或大纲，更新 `docs/10_REVISION_NOTES.md`。
6. 提交 Git：

```bash
git add .
git commit -m "ch01: draft first encounter at Guixing Cliff"
```

中文提交也可以：

```bash
git commit -m "第1章：完成归星崖初遇"
```

---

## 使用 AI 写作时的建议读取顺序

每次写新章节前，建议将以下内容提供给 AI：

1. `docs/00_GLOBAL_PROMPT.md`
2. `docs/02_CHARACTER_BIBLE.md`
3. `docs/03_WORLD_BIBLE.md`
4. `docs/04_PLOT_OUTLINE.md`
5. `docs/05_CHAPTER_OUTLINE.md` 中对应章节节拍
6. `docs/07_CONTINUITY_LOG.md` 最新记录
7. 上一章正文

然后使用 `prompts/chapter_writing_prompt.md` 作为任务提示词。
