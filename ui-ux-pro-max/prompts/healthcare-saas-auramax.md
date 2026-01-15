# AuraMax 医疗SaaS平台 - UI/UX设计指南

## 项目背景

**产品名称**: AuraMax B2B精准医疗平台
**行业**: Healthcare / Medical SaaS
**技术栈**: React 19 + Next.js 16 + Refine.dev + shadcn/ui
**设计原则**: HIPAA合规 + 医疗级可访问性 + 数据可视化

---

## 核心设计要求

### 1. 医疗行业合规性
- **HIPAA隐私保护**: 敏感数据脱敏显示，访问权限清晰标识
- **可访问性标准**: WCAG 2.1 AA级别，最低4.5:1文字对比度
- **专业可信度**: 使用医疗级配色和排版，避免过于花哨的设计

### 2. 用户角色
- **医生/临床医师**: 需要快速浏览患者数据，关注诊断辅助工具
- **医院管理员**: 关注报表、统计数据、权限管理
- **数据分析师**: 需要复杂的数据可视化和筛选功能
- **患者**: 查看自己的医疗报告（B2C端，未来扩展）

---

## UI/UX Pro Max Skill 搜索策略

### 阶段1: 产品类型与风格定位

```bash
# 1. 搜索医疗SaaS产品推荐
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare medical SaaS dashboard analytics" --domain product -n 5

# 2. 搜索专业/可信赖的UI风格
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "professional trustworthy medical clinical" --domain style -n 5

# 3. 搜索最小化/清晰风格（医疗行业适用）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "minimalism clean data-dense" --domain style -n 3
```

**预期结果**:
- 推荐风格：Minimalism（简约）、Professional（专业）、Data-dense（数据密集）
- 避免：过于花哨的Glassmorphism、Claymorphism

---

### 阶段2: 颜色系统设计

```bash
# 1. 搜索医疗行业配色方案
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare medical clinical" --domain color -n 5

# 2. 搜索信任感蓝色系（医疗行业主色调）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "blue trust professional" --domain color -n 3

# 3. 搜索数据可视化配色（用于图表）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "data visualization analytics accessible" --domain color -n 3
```

**配色要求**:
- **主色调**: 信任蓝 (Primary: #0066CC, #1E88E5)
- **辅助色**: 医疗绿 (Success: #10B981), 警告橙 (Warning: #F59E0B), 危险红 (Danger: #EF4444)
- **背景色**: 纯白 (#FFFFFF) 或浅灰 (#F9FAFB)
- **文字色**: 深灰 (#111827) 确保4.5:1对比度

---

### 阶段3: 排版系统

```bash
# 1. 搜索专业医疗排版
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "professional medical clinical readable" --domain typography -n 5

# 2. 搜索数据密集型排版（适合表格/报表）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "data-dense tabular legible" --domain typography -n 3
```

**字体要求**:
- **标题**: Inter / Roboto / SF Pro Display (清晰、专业)
- **正文**: Inter / Open Sans (16px+, 行高1.5-1.75)
- **数据表格**: JetBrains Mono / Roboto Mono (等宽字体，用于数值对齐)
- **可访问性**: 最小字体16px (移动端), 行长65-75字符

---

### 阶段4: Dashboard 图表设计

```bash
# 1. 搜索医疗仪表板图表类型
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare dashboard patient analytics" --domain chart -n 5

# 2. 搜索趋势/时间序列图表（患者生命体征）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "trend timeline timeseries vital signs" --domain chart -n 3

# 3. 搜索对比/分组图表（临床试验对比）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "comparison grouping clinical trial" --domain chart -n 3

# 4. 搜索分布/散点图（基因数据、药物响应）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "distribution scatter genomic drug response" --domain chart -n 3
```

**图表推荐**:
- **患者生命体征**: Line Chart (折线图)
- **临床试验对比**: Bar Chart (柱状图) / Grouped Bar Chart
- **基因数据分布**: Heatmap (热力图) / Scatter Plot (散点图)
- **药物疗效**: Sankey Diagram (桑基图) / Funnel Chart (漏斗图)

---

### 阶段5: UX 最佳实践

```bash
# 1. 搜索可访问性规范（WCAG 2.1 AA）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "accessibility wcag contrast aria" --domain ux -n 5

# 2. 搜索表单设计最佳实践（患者信息录入）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form validation error handling label" --domain ux -n 5

# 3. 搜索数据表格设计（大数据量患者列表）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "table data-table pagination sorting" --domain ux -n 5

# 4. 搜索加载状态设计（异步医疗报告）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "loading skeleton async state" --domain ux -n 3
```

**UX 关键规则**:
- ✅ `color-contrast`: 最低4.5:1文字对比度（医疗合规）
- ✅ `focus-states`: 键盘导航焦点环（可访问性）
- ✅ `form-labels`: 表单字段必须有`<label>`标签
- ✅ `aria-labels`: 图标按钮必须有`aria-label`
- ✅ `error-feedback`: 表单错误提示靠近问题字段
- ✅ `loading-states`: 异步操作显示加载状态（Skeleton Screen）

---

### 阶段6: React + Next.js + shadcn/ui 技术栈

```bash
# 1. 搜索 shadcn/ui 组件库指南
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form table card dialog" --stack shadcn -n 5

# 2. 搜索 Next.js SSR 性能优化
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "ssr image optimization routing" --stack nextjs -n 5

# 3. 搜索 React 状态管理（患者数据缓存）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "state cache tanstack-query swr" --stack react -n 5
```

**技术要点**:
- **shadcn/ui组件**: 优先使用`<Form>`, `<Table>`, `<Dialog>`, `<Card>`
- **Next.js优化**: 使用`<Image>`组件，启用`loading="lazy"`
- **数据缓存**: TanStack Query (React Query) 缓存患者数据
- **表单验证**: Zod + React Hook Form

---

## 完整设计工作流示例

### 场景: 设计"患者详情页"

```bash
# Step 1: 搜索医疗SaaS产品推荐
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare patient profile detail" --domain product -n 3

# Step 2: 搜索专业风格
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "minimalism professional medical" --domain style -n 3

# Step 3: 搜索医疗配色
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare trust blue" --domain color -n 3

# Step 4: 搜索排版（患者姓名/病历号清晰可读）
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "professional readable data-dense" --domain typography -n 3

# Step 5: 搜索生命体征图表
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "trend timeline vital signs" --domain chart -n 3

# Step 6: 搜索可访问性规范
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "accessibility contrast aria keyboard" --domain ux -n 5

# Step 7: 搜索 shadcn/ui 组件
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "card table tabs" --stack shadcn -n 5
```

**输出**: 基于搜索结果，生成患者详情页设计方案：
- **布局**: 左侧患者基本信息卡片 + 右侧Tabs切换（生命体征/用药记录/检查报告）
- **配色**: 主色#1E88E5（信任蓝）+ 成功色#10B981 + 背景#F9FAFB
- **字体**: Inter 16px正文，JetBrains Mono用于病历号/数值
- **图表**: 生命体征折线图（shadcn/ui + Recharts）
- **可访问性**: 所有文字4.5:1对比度，Tabs可键盘导航

---

## Pre-Delivery Checklist（交付前检查）

基于UI/UX Pro Max skill的检查清单：

### 视觉质量
- [ ] 无emoji图标（使用shadcn/ui内置图标或Lucide Icons）
- [ ] 所有图标来自统一图标集（Lucide Icons）
- [ ] 悬停状态不导致布局偏移（使用`transition-colors`而非`scale`）
- [ ] 直接使用主题颜色（`bg-primary`而非`var(--primary)`）

### 交互
- [ ] 所有可点击元素有`cursor-pointer`
- [ ] 悬停状态提供清晰视觉反馈（颜色/阴影/边框变化）
- [ ] 过渡动画流畅（150-300ms）
- [ ] 焦点状态可见（键盘导航支持）

### 亮色/暗色模式
- [ ] 亮色模式文字对比度≥4.5:1（医疗合规）
- [ ] 玻璃/透明元素在亮色模式可见（使用`bg-white/80`而非`bg-white/10`）
- [ ] 边框在两种模式下可见（亮色`border-gray-200`，暗色`border-gray-800`）
- [ ] 测试两种模式再交付

### 布局
- [ ] 浮动元素有适当间距（`top-4 left-4`而非`top-0 left-0`）
- [ ] 内容不被固定导航栏遮挡（预留`pt-16`等padding）
- [ ] 响应式设计：320px, 768px, 1024px, 1440px测试
- [ ] 移动端无横向滚动

### 可访问性（医疗合规关键）
- [ ] 所有图片有`alt`属性
- [ ] 表单输入有`<label>`标签
- [ ] 颜色不是唯一信息传达方式（例如错误提示有图标+文字）
- [ ] 支持`prefers-reduced-motion`（减少动画）

### HIPAA 合规
- [ ] 敏感数据脱敏显示（病历号部分隐藏：`****1234`）
- [ ] 权限标识清晰（仅医生可见的数据有锁图标）
- [ ] 操作日志记录（所有数据访问可追溯）
- [ ] 会话超时机制（15分钟无操作自动登出）

---

## 常见设计场景的快速搜索

### 场景1: 患者列表页（Table）
```bash
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "table pagination sorting filtering" --domain ux -n 5
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "data-table" --stack shadcn -n 3
```

### 场景2: 医疗报告详情（PDF预览）
```bash
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "document preview pdf viewer" --domain ux -n 3
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "dialog modal" --stack shadcn -n 3
```

### 场景3: 临床数据录入表单
```bash
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form validation error-feedback" --domain ux -n 5
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form input select" --stack shadcn -n 5
```

### 场景4: 数据可视化仪表板
```bash
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "dashboard analytics card" --domain product -n 3
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "trend comparison distribution" --domain chart -n 5
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "card" --stack shadcn -n 3
```

---

## 设计资源推荐

### 医疗行业参考
- **Epic MyChart**: 患者门户设计参考（简洁、信任感）
- **Cerner PowerChart**: 临床医师工作站（数据密集型）
- **Meditech Expanse**: 现代医疗系统UI（蓝色主调）

### shadcn/ui 组件优先级
1. **高优先级**: `<Form>`, `<Table>`, `<Card>`, `<Dialog>`, `<Tabs>`
2. **中优先级**: `<Select>`, `<Input>`, `<Button>`, `<Badge>`, `<Alert>`
3. **低优先级**: `<Accordion>`, `<Carousel>`, `<Combobox>`

### 图表库选择
- **Recharts**: React原生，shadcn/ui推荐，适合常规图表
- **Apache ECharts**: 复杂医疗数据可视化（基因热力图、3D散点图）
- **D3.js**: 完全自定义，适合特殊医疗图表

---

## 示例: 完整的患者详情页Prompt

当你需要设计患者详情页时，可以使用以下完整prompt：

```
请设计AuraMax B2B医疗平台的"患者详情页"，使用UI/UX Pro Max skill：

1. 产品类型：医疗SaaS仪表板
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare patient profile" --domain product -n 3

2. UI风格：专业、简约、数据密集
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "minimalism professional medical" --domain style -n 3

3. 配色方案：信任蓝为主，医疗级配色
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare blue trust" --domain color -n 3

4. 排版系统：Inter字体，16px最小字体，数据表格等宽
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "professional data-dense readable" --domain typography -n 3

5. 图表需求：生命体征折线图、用药时间轴
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "trend timeline vital signs" --domain chart -n 3

6. 可访问性：WCAG 2.1 AA，4.5:1对比度，键盘导航
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "accessibility wcag contrast keyboard" --domain ux -n 5

7. 技术栈：React + Next.js + shadcn/ui
   搜索：python3 .claude/skills/ui-ux-pro-max/scripts/search.py "card tabs table" --stack shadcn -n 5

要求：
- 符合HIPAA合规（敏感数据脱敏）
- 支持移动端响应式设计
- 使用shadcn/ui组件库
- 所有文字颜色对比度≥4.5:1
```

---

## 快速启动命令

复制粘贴以下命令快速开始AuraMax设计：

```bash
# 一键搜索医疗SaaS完整设计方案
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare medical SaaS" --domain product -n 5 && \
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "minimalism professional" --domain style -n 3 && \
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "healthcare blue" --domain color -n 3 && \
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "professional readable" --domain typography -n 3 && \
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "accessibility wcag" --domain ux -n 5 && \
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form table card" --stack shadcn -n 5
```

---

## 联系与反馈

**项目**: AuraMax B2B精准医疗平台
**技术栈**: React 19 + Next.js 16 + Refine.dev + shadcn/ui
**设计目标**: HIPAA合规 + 医疗级可访问性 + 专业信任感

如有设计问题，请参考：
1. UI/UX Pro Max skill文档：`~/.claude/skills/ui-ux-pro-max/SKILL.md`
2. AuraMax项目上下文：`~/.claude/CLAUDE.md`
3. shadcn/ui官方文档：https://ui.shadcn.com/
