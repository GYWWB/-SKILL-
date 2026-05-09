# 刘伟 / liky Codex Skill（测试版）

这是一个用于 Codex / AgentSkills 的中文人格 Skill。

它基于用户提供的群聊材料和经典语录整理，用来模拟“耐三”考研群里刘伟 / liky 式的群聊二创风格：自信、嘴硬、爱讲经历、爱评价学校、喜欢用个人经历当论据，被质疑时会补定义、补细节、算账。

> 注意：本项目是群聊二创人格 Skill，不代表现实本人，也不用于冒充、骚扰或传播未经证实的现实指控。

## 适合用来做什么

- 群聊整活
- 择校短评
- 考研群式吐槽
- 数学 / 补习建议风格模拟
- 减脂、健身、饮食建议风格模拟
- “被质疑后继续嘴硬解释”的语气模拟

示例：

```text
Use $liuwei-liky 评价一下西南大学
```

```text
Use $liuwei-liky 你健身吗
```

```text
Use $liuwei-liky 为什么你退群
```

## 文件结构

这个仓库的结构如下：

```text
liuwei-liky/
├── README.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── persona.md
    ├── work.md
    ├── source.md
    └── meta.json
```

其中：

- `SKILL.md`：Skill 的主入口，Codex 会读取这里的名称、描述和使用规则。
- `agents/openai.yaml`：Codex 界面展示用的元信息。
- `references/persona.md`：刘伟 / liky 的人格、语气、表达习惯和纠偏规则。
- `references/work.md`：可处理的任务类型、回答流程和边界。
- `references/source.md`：整理后的来源材料摘要。
- `references/meta.json`：补充元数据。

## 安装方法

### 第一步：下载仓库

点击 GitHub 页面右上方绿色按钮：

```text
Code → Download ZIP
```

下载后解压。

如果解压后的文件夹叫：

```text
liuwei-liky-codex-skill
```

建议把它重命名为：

```text
liuwei-liky
```

### 第二步：放入 Codex skills 目录

把整个 `liuwei-liky` 文件夹放到你的 Codex skills 目录。

Windows 通常是：

```text
C:\Users\你的用户名\.codex\skills\liuwei-liky
```

例如你的用户名是 `Tom`，路径就是：

```text
C:\Users\Tom\.codex\skills\liuwei-liky
```

最终目录里应该能看到：

```text
C:\Users\你的用户名\.codex\skills\liuwei-liky\SKILL.md
C:\Users\你的用户名\.codex\skills\liuwei-liky\agents\openai.yaml
C:\Users\你的用户名\.codex\skills\liuwei-liky\references\persona.md
```

### 第三步：重启 Codex

放好文件夹后，重启 Codex，或者开启一个新的 Codex 会话。

这样 Codex 才能重新扫描 skills 目录。

## 使用方法

在 Codex 里直接输入：

```text
Use $liuwei-liky 评价一下西南大学
```

也可以换成其他问题：

```text
Use $liuwei-liky 你觉得考研数学怎么学
```

```text
Use $liuwei-liky 给我评价一下这个学校
```

```text
Use $liuwei-liky 你为什么退群
```

如果已经触发过这个 Skill，也可以继续追问：

```text
那你健身吗
```

```text
你去过国外吗
```

```text
退出刘伟 / liky 模式
```

## 判断是否安装成功

如果安装成功，输入：

```text
Use $liuwei-liky 评价一下西南大学
```

Codex 应该会以短句、自信、群聊式的语气回答，而不是普通助手口吻。

如果 Codex 提示找不到 `$liuwei-liky`，通常是下面几种原因：

- 文件夹没有放到 `.codex/skills` 目录下。
- 文件夹外面多套了一层目录。
- 文件夹名不是 `liuwei-liky`。
- 没有重启 Codex 或新开会话。
- `SKILL.md` 不在 skill 文件夹的第一层。

正确结构应该是：

```text
.codex/
└── skills/
    └── liuwei-liky/
        ├── SKILL.md
        ├── agents/
        └── references/
```

错误结构示例：

```text
.codex/
└── skills/
    └── liuwei-liky/
        └── liuwei-liky/
            └── SKILL.md
```

这种多套了一层，Codex 可能识别不到。

## 安全边界

这个 Skill 只用于二创、整活和风格模拟。

它不应用于：

- 冒充现实个人
- 骚扰现实个人
- 传播未经证实的现实指控
- 提供违法务工或签证规避方法
- 提供论文代写、作弊、学术不端的具体方法

涉及争议履历、兼职经历、成绩、收入等内容时，都应理解为“群聊梗”或“用户提供设定”，不是经过核验的现实事实。

## 版本说明

当前是测试版。

这个版本主要根据用户提供材料和经典语录整理，和真实人物的完整性格仍有差距。后续如果继续补充聊天记录、语录、截图 OCR 或互动样例，可以继续优化 `references/persona.md` 和 `references/source.md`。
