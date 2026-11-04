# jem_vault 📚

> 基于 Obsidian + Git 的共享知识笔记仓库，专注 AI 影视/短剧创作方法论、提示词工程与数字内容素材沉淀。

## 📖 项目简介

本仓库的目标是把零散的创作经验、提示词和素材沉淀为可复用、可检索、可持续积累的知识资产，防止本地笔记丢失，也欢迎更多人一起共建。内容涵盖 AI 短剧/影视创作全流程方法论（剧本、分镜、角色设定、场景设计）、提示词（Prompt）工程、游戏内容创作（CS2）及短剧项目资产。

## 📁 项目结构

```
jem_vault/
├── README.md                      # 本文件
├── AI_Drama_Skill/                # AI 短剧/影视创作技能库（19 篇方法论笔记）
│   ├── 影视编剧创作.md             #   剧本创作
│   ├── 影视剧本分析.md             #   剧本分析
│   ├── 影视剧本原创改编.md          #   剧本改编
│   ├── 剧本分镜脚本.md             #   分镜脚本
│   ├── 视觉分镜九宫格生成.md        #   分镜视觉化
│   ├── 角色设定图.md / 角色三视图.md #  角色设定（含三视图、表情、服装、道具、动作）
│   ├── 场景四视图.md / 场景俯视布局.md # 场景设计
│   ├── 视频拉片拆解.md             #   拉片分析
│   └── ...                        #   更多：故事面板、VR 场景图、90s 剧本转视频等
├── Backstepping/                  # Backstepping 视频相关笔记
├── CounterStrike_2/               # CS2 游戏内容
│   ├── csgo职业比赛中英文解说字幕.md #  职业比赛中英解说字幕
│   ├── CS2方便面文学_镜头拆解与Agnes提示词.md # 镜头拆解与提示词（中英双语）
│   ├── cs_demo.md                 #   demo 分析
│   ├── spirit/                    #   Spirit 战队选手图片素材
│   └── gameinfo.gi / pov.vpk      #   游戏配置文件
├── playlet/                       # 短剧项目资产库
│   ├── role/                      #   角色设定图（凌羽、幻音、暗星、熊出没等 13 个角色）
│   ├── scene/                     #   场景图（龙之遗迹、洪崖洞、光头强家等）
│   ├── pictures/                  #   道具设定图、收藏图标等素材
│   └── tsxt/                      #   剧本文本与表格（山城归途、重庆小剧场等）
├── runninghub_resource/           # RunningHub 平台资源记录
├── 光头强摸金发财梦_miqiang/        # 《光头强摸金发财梦》系列短剧剧本及素材
├── 宗主视频动作迁移_miqiang/        # 宗主跳舞视频动作迁移/复刻笔记
├── 打斗_test/                     # 打斗场景测试笔记（冰剑仙、法天象地等）
├── 梦的翅膀DJ摇_miqiang/           # 《AI 梦的翅膀 DJ 摇》创作笔记
├── 游戏场景图_prompt/              # 游戏场景图生成提示词（720° 全景图等）及示例图
└── .obsidian/                     # Obsidian 配置（含 obsidian-git 等插件，见下文）
```

> 📌 目录名中带 `_miqiang` 后缀的为系列短剧项目，内含剧本 Markdown 与配套图片素材（`assets/`）。

## 🚀 使用方法

### 方式一：克隆后直接查看

```bash
git clone https://github.com/Jem-Geshibao/jem_vault.git
```

所有笔记均为 Markdown 格式，可用任意文本编辑器或 Markdown 阅读器直接打开。

### 方式二：Obsidian + Git 插件自动同步（推荐）

1. 克隆仓库到本地（命令同上）。
2. 打开 Obsidian → **Open folder as vault** → 选择克隆下来的 `jem_vault` 文件夹。
3. 仓库已内置 [Obsidian Git](https://github.com/Vinzent03/obsidian-git) 插件配置，启用社区插件后即可实现笔记的定时自动 commit / pull / push——边记录边同步，长期存储不丢失。
4. 另外预装了 **Enhancing Export**（导出 PDF/Word 等格式）与 **Custom Attachment Location**（附件自动归档）插件，可按需启用。

### 方式三：手动提交贡献

```bash
# 添加或修改笔记后
git add .
git commit -m "新增/更新笔记：简要说明"
git push origin main
```

## 🤝 贡献指南

- 欢迎提交学习笔记、创作经验、提示词、素材整理等内容。
- 建议按主题放入对应目录；新主题可新建目录，命名清晰即可。
- 图片等附件建议放入同级 `assets/` 或对应子目录，保持结构整洁。
- 文件命名尽量语义化（中英文均可），方便检索。
- 遇到问题或有改进建议，欢迎在 [Issues](https://github.com/Jem-Geshibao/jem_vault/issues) 中提出。

## 📄 其他说明

- 本仓库内容仅供学习交流使用；涉及第三方 IP（如熊出没等）的素材版权归原作者所有。
- 仓库的核心理念：**让知识被记录、被保留、被共享**，让每一份笔记都能长期存储、随时检索。

---

**Last Updated**: 2026-11-04
