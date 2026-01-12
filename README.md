# Claude Code Skills

Claude Code 技能集合 - 提升你的 AI 编程助手能力。

## 技能列表

| 技能 | 描述 | 用法 |
|------|------|------|
| [code-roaster](./code-roaster) | Gordon Ramsay 风格毒舌代码审查 | `/code-roaster` |
| [invoice-scanner](./invoice-scanner) | 发票扫描识别，生成分类统计报告 | `/invoice-scanner ./发票` |
| [thinking-frameworks](./thinking-frameworks) | 25种跨职业思维工具框架 | `/thinking-frameworks` |
| [oracle](./oracle) | 战略技术顾问，架构设计与调试 | `/oracle` |
| [librarian](./librarian) | 开源库研究专家 | `/librarian "问题"` |
| [frontend-engineer](./frontend-engineer) | UI/UX 设计工程师 | `/frontend-engineer` |
| [doc-writer](./doc-writer) | 技术文档专家 | `/doc-writer` |

## 技能分类

### 开发辅助
- **code-roaster** - 代码质量审查
- **oracle** - 架构设计与技术决策
- **frontend-engineer** - UI/UX 设计实现

### 研究分析
- **librarian** - 开源库研究
- **thinking-frameworks** - 多角度问题分析

### 文档处理
- **doc-writer** - 技术文档撰写
- **invoice-scanner** - 发票识别统计

## 安装方法

### 方法一：作为本地插件安装

1. 克隆仓库：
```bash
git clone https://github.com/namjar/claude-code-skills.git
```

2. 复制到 Claude Code 插件目录：
```bash
mkdir -p ~/.claude/plugins/local/my-skills/.claude-plugin
mkdir -p ~/.claude/plugins/local/my-skills/skills

# 复制所有技能
for skill in code-roaster invoice-scanner thinking-frameworks oracle librarian frontend-engineer doc-writer; do
  cp -r claude-code-skills/$skill ~/.claude/plugins/local/my-skills/skills/
done
```

3. 创建插件配置 `~/.claude/plugins/local/my-skills/.claude-plugin/plugin.json`：
```json
{
  "name": "my-skills",
  "version": "1.0.0",
  "description": "Claude Code Skills Collection"
}
```

4. 在 `~/.claude/settings.json` 启用：
```json
{
  "enabledPlugins": {
    "my-skills@my-skills-local": true
  }
}
```

5. 重启 Claude Code

### 方法二：直接使用

将任意 SKILL.md 文件内容复制到 Claude Code 对话中即可使用。

## 技能来源

- `code-roaster`, `invoice-scanner` - 原创
- `thinking-frameworks` - 基于 Scott H. Young 的思维工具
- `oracle`, `librarian`, `frontend-engineer`, `doc-writer` - 借鉴自 [oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode)

## License

MIT
