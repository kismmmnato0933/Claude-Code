# Claude-Code

## 更经济的 Claude Code 订阅平替服务 国内可用

Claude Code 是 Anthropic 官方CLI工具，专为开发者设计的智能编程助手，让代码开发变得更高效、更智能。

直接在终端释放 Claude 的强大能力。瞬间搜索百万行代码库。将耗时数小时的工作 流程缩减为一条命令。您的工具。您的工作流程。您的代码库，以思维速度演进。


![Claude Code 订阅平替服务](/20250714210400.png)


目前Claude官网订阅价格 200美元/月，

伊莉思Code提供同等订阅服务，低至10元/天, 同等于官方 Max 200美元方案 ，支持Claude 4 Opus模型, 极致的性价比

伊莉思code官网：https://code.ylsagi.com


# Claude code 的使用技巧

## 激活思考模式

根据 Anthropic 的官方文档“Claude Code Best Practices”，要激活 Claude Code 的扩展思考模式，推荐在提示中加入特定的词语。这些词语包括：

 - “think”（思考）
 - “think hard”（深入思考）
 - “think harder”（更深入思考）
 - “ultrathink”（超深度思考）

如果你想让 Claude Code 规划解决方案，可以说：“Think about how to solve this problem before writing the code.”（先思考如何解决这个问题，然后再写代码。）

最佳实践与示例
以下是使用扩展思考模式的示例工作流：

规划阶段：在提示中加入“think”或“ultrathink”，例如：“Think about how to refactor this function to improve performance.”（思考如何重构此函数以提高性能。）

验证阶段：在实现解决方案后，可以要求 Claude 验证其合理性，例如：“Think hard to verify if this solution meets all requirements.”（深入思考验证此解决方案是否满足所有要求。）

调试阶段：对于复杂的错误，可以说：“Think harder about why this test is failing and propose multiple fixes.”（更深入思考为什么这个测试失败，并提出多种修复方案。）

⚠️注意：使用激活思考模式token消耗同时也会大幅增加


## 减少上下文Token消耗

#### 启动新聊天以处理单独任务

 - 使用 /clear 命令重置聊天历史，避免无关上下文累积。

 - 启动新聊天可减少不必要消耗。无状态对话需要每次交互包含整个历史，快速累积 token，

#### 总结长对话

 - 当接近上下文限制的 50% 时，使用 /compact 压缩历史，减少 token 使用。

 - 建议此方法可降低成本，尤其在接近上下文限制时性能下降。

#### 选择合适模型
 - 使用 /mod 切换模型，复杂任务用高级模型，简单任务用轻量模型，平衡成本和性能。

#### 创建紧凑文件

 - 保持文件精简，拆分大文件为单一目的的小文件，减少上下文需求。

#### 使用监控工具
 - 使用如 Claude-Code-Usage-Monitor 的工具实时跟踪 token 消耗，优化管理。


### 化工作流

优化工作流可以显著提升效率，以下是具体技巧：

 - 明确指令：提供具体的任务描述。例如，“为 foo.py 的登录功能编写新的测试用例” 比 “为 foo.py 添加测试” 更有效。官方文档提供示例表，强调具体性对结果的影响。

 - 使用图像：通过粘贴或提供文件路径使用图像，适用于视觉任务或调试。例如，可以拖放截图以分析 UI 问题。

 - 纠正方向：在编码前规划，使用 Esc 键中断、双击 Escape 编辑历史，或要求 Claude Code 撤销更改。这可以避免不必要的错误。

## 自定义设置

创建 CLAUDE.md 文件：在项目根目录、子目录或家目录（~/.claude/CLAUDE.md）创建 CLAUDE.md 文件，用于记录项目特定的指令、代码风格、测试说明等。

例如，可以记录常用 bash 命令、核心文件位置、代码风格指南等。这样可以帮助 Claude Code 更好地理解您的项目。

管理工具权限：使用 /permissions 命令或编辑配置文件（如 .claude/settings.json）来指定 Claude Code 可以使用的工具。可以使用 --allowedTools CLI 标志进行更细粒度的控制。


## IDE和编辑器集成

Claude Code 可以与多种 IDE 和编辑器集成，包括：

Visual Studio Code（包括流行的分支如 Cursor、Windsurf 和 VSCodium）

JetBrains IDE（包括 IntelliJ、PyCharm、Android Studio、WebStorm、PhpStorm 和 GoLand）

 - 通常在IDE的集成终端中运行 claude 命令即可自动安装Claude扩展插件。

 - 在外部终端运行claude 使用 /ide 命令也可以连接编辑器

## 定期升级

定期更新可确保您获得最新功能、性能改进和错误修复。

```
npm update -g @anthropic-ai/claude-code
```
