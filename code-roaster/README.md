# Code Roaster

用 Gordon Ramsay 风格毒舌吐槽代码质量，生成搞笑且实用的代码审查报告。

## 用法

```bash
/code-roaster                    # 烤当前目录的所有代码
/code-roaster ./src             # 烤指定目录
/code-roaster app.py            # 烤单个文件
/code-roaster --mild            # 温和模式（少点毒舌）
/code-roaster --brutal          # 残暴模式（火力全开）
```

## 功能特点

- 多维度代码分析：代码异味、潜在 Bug、安全隐患、性能问题、最佳实践违规
- 三种烤制模式：温和、标准、残暴
- 支持多种语言：JavaScript/TypeScript、Python、Java、Go、Rust、C/C++、Ruby、PHP、Swift、C#
- 生成详细的 Markdown 报告，包含评分和改进建议

## 输出示例

```
🔥 代码烤肉机启动！

📂 正在扫描目录: ./src
🔍 找到 42 个代码文件

📊 快速总结:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
总评分: 💩💩💩☆☆ (3/10)

问题总数: 156 个
  🚨 严重: 8 个（安全/Bug）
  ⚠️  中等: 45 个（性能/异味）
  ℹ️  轻微: 103 个（格式/注释）
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

💬 Gordon 说: "这代码就像三天没洗的平底锅，
   虽然能用，但你真的想用吗？"

📄 详细报告已生成: ./CODE_ROAST_REPORT.md
```
