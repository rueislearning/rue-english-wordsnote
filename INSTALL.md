# 安装 Rue English Wordsnote

供收到用户安装请求的 Agent 使用。先判断当前环境能否加载 Skill、访问 GitHub，以及读写用户指定的 Obsidian 目录。遇到缺失能力时，说明具体受阻步骤，并提供 README 中的手动安装方式。

## 获取与安装

从 https://github.com/rueislearning/rue-english-wordsnote 获取默认分支的同一个提交版本，先在临时目录读取 SKILL.md 和本说明。

Codex 优先使用当前环境提供的 Skill 安装工具。默认目录为 $CODEX_HOME/skills/rue-english-wordsnote，CODEX_HOME 未设置时使用 ~/.codex/skills/rue-english-wordsnote。其他 Agent 使用其官方支持的技能目录，并核实加载方式。

安装完整的可复用内容，包括 SKILL.md、agents/、references/、assets/、config.example.json、README.md、INSTALL.md、LICENSE 和 examples/。可使用宿主安装工具安装整个公开仓库。检查安装结果中这些文件是否齐全、内部链接是否指向已安装文件。

如果已有同名安装，先读取已有版本及本地修改。备份需要替换的文件后更新，保留 config.local.json 和用户定制内容。出现无法自动合并的本地修改时，说明冲突位置，请用户选择后继续。

## 配置 Obsidian

优先沿用用户明确指定的位置或已安装版本的有效 config.local.json。需要新配置时，询问 Obsidian 笔记库位置，并确认其中的单词本专用目录。配置中的 notebook_path 使用当前执行环境能访问的绝对路径。写入 JSON 时正确转义路径字符。

按 references/connection.md 的要求，在单词本目录创建一份明确标为连接测试的 Markdown 笔记。使用独立文件名避免覆盖已有内容。写入测试标识，再实际读回核对。连接测试独立于查词记录。

用户通过安装口令已要求进行这次配置和连接测试。宿主需要文件授权时，按其机制处理。文件不可访问时，报告安装完成到哪一步、哪个路径或权限仍需处理。

## 交付启动指令

分别报告 Skill 文件安装、单词本配置、连接测试读回的实际结果。提供 README 中“安装后，复制这段开始使用”的完整启动指令。按宿主要求提示在下一轮或新聊天中加载 Skill，并说明手机需要连接保存词库的电脑。

启动时的配置检查读取 config.local.json 并核对目录可访问性即可。连接测试由用户明确请求时执行。日常查词遵循 SKILL.md 的即时解释与手动同步规则。
