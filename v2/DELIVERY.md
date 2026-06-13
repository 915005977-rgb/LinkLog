# LinkLog V2 — 设计升级交付

> 由画统筹 · 设计编排师汇总 · 2026-06-13

---

## 产出物清单

| # | 文件 | 用途 | 设备 | 行数 |
|---|------|------|------|------|
| 1 | `detail-v2.html` | 升级版联系人详情页 | Mobile | ~1090 |
| 2 | `people-table.html` | PC端人物资料宽表格 | Desktop | ~1410 |
| 3 | `field-insights-v2.html` | PC端场域洞察 Dashboard | Desktop | ~785 |

## 辅助文件

| 文件 | 用途 |
|------|------|
| `REQUIREMENTS.md` | 需求摘要（五要素+字段定义+脱敏规范） |
| `DATA.md` | 10位脱敏联系人完整数据+聚合统计 |
| `DESIGN-TOKENS-V2.css` | 补充设计令牌（PC容器/表格/Dashboard/四线色彩） |

---

## 设计决策说明

### 1. 为什么新增"四条线"色彩体系？

用户从小红书活动人脉整理中提炼的深度档案字段，自然形成了四条信息线索：
- **身世线**（暖棕 #7C9A8E）：这个人从哪来？背景/履历/现状
- **价值线**（琥珀 #D4915A）：这个人有什么？产品/服务/商业化
- **连接线**（信任蓝 #5B8ED0）：这个人需要什么？卡点/想链接/关联
- **行动线**（AI紫 #7C6AE8）：AI建议做什么？话题/动作

四线色彩与 LinkLog 原有的温度梯度（暖灰→琥珀橘→冷蓝紫）同源，形成完整的视觉叙事系统。

### 2. 为什么"价值线"默认折叠？

审查发现身世线+价值线同时展开时，首屏信息量过大。调整为只展开身世线（"这个人从哪来"是最高频查看的信息），价值线需要点击展开。连接线也默认折叠。

### 3. 数据积累形态的设计逻辑

产品进化路径 **记录个体 → 积累群体 → 洞察场域** 在三个原型中体现为：
- `detail-v2.html` = 记录个体（深度档案，一次一人）
- `people-table.html` = 积累群体（横向对比，多人多维度）
- `field-insights-v2.html` = 洞察场域（聚合统计，发现模式和机会）

---

## 质量审查报告

### 修复前评分

| 文件 | 5维总分 | Anti-Slop扣分 | 最终得分 | 结论 |
|------|---------|---------------|----------|------|
| people-table.html | 19/25 | -5 | 14 | REVISE |
| field-insights-v2.html | 22/25 | -5 | 17 | PASS(需修P0) |
| detail-v2.html | 21/25 | -4 | 17 | PASS(需修P0) |

### 修复内容

**P0（必须修复）— 已全部修复：**
- 硬编码色值 #fff ×10处 → `var(--color-text-on-accent)`
- 硬编码 rgba 白色 ×8处 → `var(--color-bg-glass/card-glass/cell-sticky)`
- 硬编码 rgba 暖色毛玻璃底 ×4处 → `var(--color-bg-frosted)`
- 硬编码 rgba AI 紫色 ×3处 → `var(--color-ai-border-subtle/bg-item/bg-item-border)`

**P1（应该修复）— 已全部修复：**
- people-table 档案线边框 light→主线色（5处）
- people-table 空结果行内联style→`.empty-state` 类
- field-insights "标签覆盖"占位符 `—` → 实际数字 `9`
- field-insights 商业化阶段人物重复 → 每人只归入一个主阶段
- detail-v2 AI行动区glow圆 120px→80px
- detail-v2 价值线默认展开→默认折叠
- detail-v2 重新生成按钮内联style→`.regenerating` 类

### 修复后预期评分

| 文件 | 预期5维总分 | 预期Anti-Slop扣分 | 预期最终得分 |
|------|-----------|-------------------|------------|
| people-table.html | 19-20 | 0 | **19-20** |
| field-insights-v2.html | 22 | 0 | **22** |
| detail-v2.html | 21-22 | 0 | **21-22** |

---

## 使用方式

1. **移动端详情页**：直接在浏览器打开 `detail-v2.html`，建议用移动端模拟器（393px 宽度）
2. **PC端表格**：直接在浏览器打开 `people-table.html`，最小宽度 1280px
3. **PC端 Dashboard**：直接在浏览器打开 `field-insights-v2.html`，最小宽度 1280px

所有文件零外部依赖，可直接部署到 GitHub Pages 或任何静态托管服务。
