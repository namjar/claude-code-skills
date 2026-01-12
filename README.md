# Claude Code Skills

Claude Code 技能集合 - 提升你的 AI 编程助手能力。

## 技能列表

| 技能 | 描述 | 用法 |
|------|------|------|
| [code-roaster](./code-roaster) | Gordon Ramsay 风格毒舌代码审查，生成搞笑且实用的代码审查报告 | `/code-roaster` |
| [invoice-scanner](./invoice-scanner) | 发票扫描识别，提取关键信息并生成分类统计报告 | `/invoice-scanner ./发票文件夹` |
| [thinking-frameworks](./thinking-frameworks) | 25种跨职业思维工具框架，帮助多角度分析问题 | `/thinking-frameworks` |

## 安装方法

### 方法一：作为本地插件安装

1. 克隆仓库到本地：
```bash
git clone https://github.com/namjar/claude-code-skills.git
```

2. 复制技能到 Claude Code 插件目录：
```bash
mkdir -p ~/.claude/plugins/local/my-skills/.claude-plugin
mkdir -p ~/.claude/plugins/local/my-skills/skills

# 复制技能文件
cp -r claude-code-skills/code-roaster ~/.claude/plugins/local/my-skills/skills/
cp -r claude-code-skills/invoice-scanner ~/.claude/plugins/local/my-skills/skills/
cp -r claude-code-skills/thinking-frameworks ~/.claude/plugins/local/my-skills/skills/
```

3. 创建插件配置文件 `~/.claude/plugins/local/my-skills/.claude-plugin/plugin.json`：
```json
{
  "name": "my-skills",
  "version": "1.0.0",
  "description": "Claude Code Skills Collection"
}
```

4. 在 `~/.claude/settings.json` 中启用插件：
```json
{
  "enabledPlugins": {
    "my-skills@my-skills-local": true
  }
}
```

5. 重启 Claude Code

### 方法二：直接使用

将 SKILL.md 文件内容复制到 Claude Code 对话中即可使用。

## 技能详情

### code-roaster

用 Gordon Ramsay 风格毒舌吐槽代码质量，生成搞笑且实用的代码审查报告。

**功能特点：**
- 多维度代码分析（代码异味、Bug、安全、性能、最佳实践）
- 三种烤制模式（温和、标准、残暴）
- 生成详细的 Markdown 报告

### invoice-scanner

扫描目录识别各类发票，提取关键信息并生成分类统计报告。

**功能特点：**
- 支持市内交通、长途交通、住宿、其他四大分类
- 自动解压 ZIP 文件
- 生成汇总统计和详细表格

### thinking-frameworks

25种跨职业思维工具框架，帮助从多角度分析复杂问题。

**功能特点：**
- 创造与设计、分析与验证、系统与工程等六大类思维工具
- 单一工具应用和多工具组合
- 视角切换清单

## License

MIT
