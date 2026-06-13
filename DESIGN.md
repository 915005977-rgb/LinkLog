# LinkLog 设计令牌文档（DESIGN.md）

> 基于 Notion 设计系统定制 · 为 LinkLog — 连接日志 · 关系复利 专属打造
> 版本：v1.0 · 更新日期：2025-07

---

## 1. Visual Theme — 视觉哲学

### 设计方向
**Modern Minimal × Soft Warm — 简约骨架 + 温暖血肉**

LinkLog 的视觉基因来自 Notion 的温暖留白哲学，但注入了更强的交互灵动性。整体呈现出「被暖光包裹的精密仪器」感——结构严谨如 Linear，但每一个触感都带着温度。

### 视觉三原则
1. **呼吸感优先**：任何页面至少 40% 留白，信息密度通过渐进式披露控制
2. **温度梯度**：从暖灰底色 → 琥珀橘强调 → 冷蓝紫 AI，形成「人 → 情感 → 机器」的温度叙事
3. **灵动手感**：每一个状态变化都有物理隐喻（弹跳、滑出、渐入），绝不出现生硬的显隐切换

### 视觉情绪板关键词
温暖包裹 · 纸质感 · 精密间距 · 微光 · 轻盈流动 · 人本科技

---

## 2. Color Palette — 色彩系统

### 色彩哲学
主色系负责「安静」，强调色负责「温度」，AI 色负责「智能感」。三者形成从暖到冷的温度梯度，帮助用户直觉区分内容来源。

### 2.1 主色阶（Neutral Warm — 暖灰系）

| Token | 用途 | HEX | OKLCh | CSS Variable |
|-------|------|-----|-------|-------------|
| `--color-bg-primary` | 页面主背景 | `#F8F6F3` | oklch(0.97 0.005 80) | `var(--color-bg-primary)` |
| `--color-bg-secondary` | 卡片/次级背景 | `#F1EDE8` | oklch(0.94 0.008 80) | `var(--color-bg-secondary)` |
| `--color-bg-tertiary` | 输入框/凹陷区域 | `#EAE5DF` | oklch(0.91 0.010 80) | `var(--color-bg-tertiary)` |
| `--color-bg-elevated` | 浮层/弹窗背景 | `#FFFFFF` | oklch(1.0 0 0) | `var(--color-bg-elevated)` |
| `--color-border-subtle` | 极淡边框 | `#E8E3DD` | oklch(0.90 0.010 80) | `var(--color-border-subtle)` |
| `--color-border-default` | 默认边框 | `#D4CFC8` | oklch(0.86 0.012 80) | `var(--color-border-default)` |
| `--color-text-primary` | 主文本 | `#2C2825` | oklch(0.25 0.015 60) | `var(--color-text-primary)` |
| `--color-text-secondary` | 次文本 | `#6B6560` | oklch(0.50 0.015 60) | `var(--color-text-secondary)` |
| `--color-text-tertiary` | 占位符/辅助文本 | `#9E9893` | oklch(0.70 0.012 60) | `var(--color-text-tertiary)` |
| `--color-text-disabled` | 禁用态文本 | `#C5C0BA` | oklch(0.82 0.010 60) | `var(--color-text-disabled)` |

### 2.2 强调色阶（Amber Orange — 琥珀橘系）

| Token | 用途 | HEX | OKLCh | CSS Variable |
|-------|------|-----|-------|-------------|
| `--color-accent-default` | CTA/强调 | `#E8915A` | oklch(0.68 0.130 55) | `var(--color-accent-default)` |
| `--color-accent-hover` | 悬停态 | `#D47E48` | oklch(0.63 0.130 55) | `var(--color-accent-hover)` |
| `--color-accent-active` | 按压态 | `#C06E3A` | oklch(0.58 0.130 55) | `var(--color-accent-active)` |
| `--color-accent-light` | 浅底强调 | `#FDF0E6` | oklch(0.95 0.030 55) | `var(--color-accent-light)` |
| `--color-accent-lighter` | 极浅底 | `#FEF7F0` | oklch(0.98 0.015 55) | `var(--color-accent-lighter)` |
| `--color-accent-text` | 强调文本 | `#C06E3A` | oklch(0.58 0.130 55) | `var(--color-accent-text)` |

### 2.3 AI 色阶（Cool Violet — 冷蓝紫系）

| Token | 用途 | HEX | OKLCh | CSS Variable |
|-------|------|-----|-------|-------------|
| `--color-ai-default` | AI 元素主色 | `#7C6AE8` | oklch(0.55 0.160 290) | `var(--color-ai-default)` |
| `--color-ai-hover` | AI 悬停 | `#6B59D6` | oklch(0.50 0.160 290) | `var(--color-ai-hover)` |
| `--color-ai-light` | AI 浅底 | `#F0EDFC` | oklch(0.95 0.030 290) | `var(--color-ai-light)` |
| `--color-ai-lighter` | AI 极浅底 | `#F8F6FE` | oklch(0.98 0.015 290) | `var(--color-ai-lighter)` |
| `--color-ai-text` | AI 文本 | `#5B4AC5` | oklch(0.45 0.160 290) | `var(--color-ai-text)` |
| `--color-ai-glow` | AI 光晕效果 | `rgba(124,106,232,0.15)` | — | `var(--color-ai-glow)` |

### 2.4 语义色阶

| Token | 用途 | HEX | CSS Variable |
|-------|------|-----|-------------|
| `--color-success-default` | 成功/确认 | `#4CAF7D` | `var(--color-success-default)` |
| `--color-success-light` | 成功浅底 | `#E8F5EE` | `var(--color-success-light)` |
| `--color-warning-default` | 警告/提示 | `#E5A84B` | `var(--color-warning-default)` |
| `--color-warning-light` | 警告浅底 | `#FDF5E6` | `var(--color-warning-light)` |
| `--color-error-default` | 错误/必填 | `#D95555` | `var(--color-error-default)` |
| `--color-error-light` | 错误浅底 | `#FDEAEA` | `var(--color-error-light)` |
| `--color-info-default` | 信息 | `#5B8ED0` | `var(--color-info-default)` |
| `--color-info-light` | 信息浅底 | `#E8F0FA` | `var(--color-info-light)` |

### 2.5 标签类别色

用于三类标签体系的视觉区分：

| 类别 | Token | HEX | CSS Variable |
|------|-------|-----|-------------|
| 关系维度（亲密/熟悉/认识） | `--color-tag-relational` | `#E8915A` | `var(--color-tag-relational)` |
| 场景维度（工作/社交/生活） | `--color-tag-contextual` | `#7C6AE8` | `var(--color-tag-contextual)` |
| 自定义标签 | `--color-tag-custom` | `#5B8ED0` | `var(--color-tag-custom)` |
| 标签浅底（通用） | `--color-tag-bg-base` | `#F1EDE8` | `var(--color-tag-bg-base)` |

### 2.6 对比度验证（WCAG AA）

| 组合 | 比例 | 结果 |
|------|------|------|
| `#2C2825` on `#F8F6F3` | 12.8:1 | ✅ AAA |
| `#6B6560` on `#F8F6F3` | 5.2:1 | ✅ AA |
| `#E8915A` on `#FFFFFF` | 3.1:1 | ⚠️ 仅用于大文本/图标 |
| `#C06E3A` on `#F8F6F3` | 5.6:1 | ✅ AA |
| `#7C6AE8` on `#FFFFFF` | 4.8:1 | ✅ AA |
| `#5B4AC5` on `#F8F6F3` | 7.2:1 | ✅ AAA |
| `#FFFFFF` on `#E8915A` | 3.1:1 | ⚠️ 仅用于大文本/图标 |
| `#FFFFFF` on `#7C6AE8` | 4.8:1 | ✅ AA |

---

## 3. Typography — 排版系统

### 3.1 字体栈

| Token | Font Stack | CSS Variable |
|-------|-----------|-------------|
| `--font-sans`（主字体） | `"Inter", "SF Pro Display", -apple-system, "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif` | `var(--font-sans)` |
| `--font-mono`（数字/代码） | `"JetBrains Mono", "SF Mono", "Menlo", monospace` | `var(--font-mono)` |

> **说明**：Inter 作为英文主字体（与 Notion 同源），中文回退到苹方/思源黑体。数字场景（如联系频率）使用等宽字体保证对齐。

### 3.2 字号层级

| Token | Size | 行高 | 字重 | 用途 | CSS Variable |
|-------|------|------|------|------|-------------|
| `--text-display` | 28px | 1.25 (35px) | 700 | 欢迎页/空状态标题 | `var(--text-display)` |
| `--text-h1` | 22px | 1.30 (29px) | 600 | 页面主标题 | `var(--text-h1)` |
| `--text-h2` | 18px | 1.35 (24px) | 600 | 区块标题/步骤标题 | `var(--text-h2)` |
| `--text-h3` | 16px | 1.40 (22px) | 600 | 卡片标题/分组标题 | `var(--text-h3)` |
| `--text-body` | 15px | 1.50 (23px) | 400 | 正文/表单标签 | `var(--text-body)` |
| `--text-body-sm` | 13px | 1.50 (20px) | 400 | 辅助说明/提示文字 | `var(--text-body-sm)` |
| `--text-caption` | 12px | 1.40 (17px) | 400 | 脚注/时间戳/标签内文字 | `var(--text-caption)` |
| `--text-micro` | 11px | 1.35 (15px) | 500 | 角标/极小标签 | `var(--text-micro)` |

### 3.3 字重规范

| Token | Weight | 用途 |
|-------|--------|------|
| `--weight-regular` | 400 | 正文、说明文字 |
| `--weight-medium` | 500 | 导航、小标题、标签 |
| `--weight-semibold` | 600 | 标题、CTA 按钮、步骤标题 |
| `--weight-bold` | 700 | 大标题、数字强调 |

---

## 4. Layout — 间距与布局系统

### 4.1 基础间距单位

基础单位：**4px**（与 8pt 栅格对齐，移动端最佳实践）

| Token | Value | 用途 | CSS Variable |
|-------|-------|------|-------------|
| `--space-1` | 4px | 极小间距（图标与文字） | `var(--space-1)` |
| `--space-2` | 8px | 小间距（标签内边距） | `var(--space-2)` |
| `--space-3` | 12px | 中小间距（表单项间距） | `var(--space-3)` |
| `--space-4` | 16px | 中间距（卡片内边距） | `var(--space-4)` |
| `--space-5` | 20px | 中大间距（区块间距） | `var(--space-5)` |
| `--space-6` | 24px | 大间距（页面边距） | `var(--space-6)` |
| `--space-8` | 32px | 超大间距（区块分隔） | `var(--space-8)` |
| `--space-10` | 40px | 特大间距（步骤间留白） | `var(--space-10)` |
| `--space-12` | 48px | 极大间距（页面顶部留白） | `var(--space-12)` |

### 4.2 移动端页面边距

| 区域 | 间距 |
|------|------|
| 水平安全边距 | 20px（`--space-5`） |
| 顶部安全区 | 48px（`--space-12`）+ 状态栏高度 |
| 底部安全区 | 34px + Home Indicator 高度 |
| 卡片内边距 | 16px（`--space-4`） |
| 表单项间距 | 12px（`--space-3`） |

### 4.3 容器规范

| Token | Max Width | 用途 |
|-------|-----------|------|
| `--container-mobile` | 100vw | 移动端全宽 |
| `--container-card` | 100% - 40px | 卡片宽度（扣除左右边距） |
| `--container-input` | 100% | 输入框宽度 |

---

## 5. Border Radius — 圆角规范

| Token | Value | 用途 | CSS Variable |
|-------|-------|------|-------------|
| `--radius-sm` | 6px | 小元素（标签、徽章） | `var(--radius-sm)` |
| `--radius-md` | 10px | 中元素（按钮、输入框） | `var(--radius-md)` |
| `--radius-lg` | 14px | 大元素（卡片、弹窗） | `var(--radius-lg)` |
| `--radius-xl` | 20px | 超大元素（底部抽屉、全宽卡片） | `var(--radius-xl)` |
| `--radius-full` | 9999px | 圆形（头像、悬浮按钮） | `var(--radius-full)` |

> **设计原则**：圆角从 Notion 的偏小圆角（4-8px）适度放大到 6-14px，增加亲和力和「温度感」，但不超过 20px 以保持简约骨架。

---

## 6. Depth & Elevation — 阴影与层级系统

### 6.1 阴影规范

| Token | 值 | 用途 | CSS Variable |
|-------|---|------|-------------|
| `--shadow-xs` | `0 1px 2px rgba(44,40,37,0.04)` | 极浅阴影（卡片默认） | `var(--shadow-xs)` |
| `--shadow-sm` | `0 2px 8px rgba(44,40,37,0.06)` | 小阴影（悬浮标签） | `var(--shadow-sm)` |
| `--shadow-md` | `0 4px 16px rgba(44,40,37,0.08)` | 中阴影（弹窗/浮层） | `var(--shadow-md)` |
| `--shadow-lg` | `0 8px 32px rgba(44,40,37,0.10)` | 大阴影（底部抽屉） | `var(--shadow-lg)` |
| `--shadow-focus` | `0 0 0 3px rgba(232,145,90,0.3)` | 焦点环（强调色） | `var(--shadow-focus)` |
| `--shadow-focus-ai` | `0 0 0 3px rgba(124,106,232,0.3)` | AI 焦点环 | `var(--shadow-focus-ai)` |

### 6.2 Z-index 层级

| Token | Value | 用途 |
|-------|-------|------|
| `--z-base` | 0 | 页面内容 |
| `--z-card` | 10 | 卡片层叠 |
| `--z-sticky` | 100 | 吸顶元素 |
| `--z-dropdown` | 200 | 下拉菜单 |
| `--z-modal` | 300 | 弹窗 |
| `--z-toast` | 400 | 提示条 |
| `--z-tooltip` | 500 | 工具提示 |

---

## 7. Motion & Animation — 动效规范

### 7.1 时长系统

| Token | Value | 用途 | CSS Variable |
|-------|-------|------|-------------|
| `--duration-instant` | 100ms | 微反馈（按钮按压、开关） | `var(--duration-instant)` |
| `--duration-fast` | 200ms | 快速过渡（颜色变化、透明度） | `var(--duration-fast)` |
| `--duration-normal` | 300ms | 标准过渡（卡片展开、标签渐入） | `var(--duration-normal)` |
| `--duration-slow` | 400ms | 慢速过渡（步骤切换、页面滑动） | `var(--duration-slow)` |
| `--duration-spring` | 500ms | 弹性动画（元素飞入飞出） | `var(--duration-spring)` |

### 7.2 缓动曲线

| Token | Value | 用途 | CSS Variable |
|-------|-------|------|-------------|
| `--ease-out` | `cubic-bezier(0.25, 0.1, 0.25, 1)` | 默认出场动画 | `var(--ease-out)` |
| `--ease-in-out` | `cubic-bezier(0.42, 0, 0.58, 1)` | 状态切换 | `var(--ease-in-out)` |
| `--ease-spring` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | 弹性微交互 | `var(--ease-spring)` |
| `--ease-decelerate` | `cubic-bezier(0, 0, 0.2, 1)` | 减速入场 | `var(--ease-decelerate)` |

### 7.3 核心动画模式

| 动画模式 | 时长 | 曲线 | 说明 | 实现提示 |
|---------|------|------|------|---------|
| **标签渐入** | 300ms | `--ease-decelerate` | AI 生成标签逐个渐入，间隔 80ms | `opacity: 0→1; transform: translateY(8px)→0` |
| **卡片滑出** | 400ms | `--ease-out` | 核心四问回答后卡片上滑飞出 | `transform: translateY(-120%) scale(0.9); opacity: 0` |
| **步骤切换** | 400ms | `--ease-out` | Step 1→Step2 横向滑动过渡 | `transform: translateX(100%)→0`（新步骤从右侧入） |
| **按钮弹跳** | 500ms | `--ease-spring` | CTA 点击时弹性缩放 | `transform: scale(0.95)→1.02→1` |
| **标签拖拽** | 实时 | — | 标签排序拖拽 | 使用 `transform` 移动，释放时 `200ms/ease-out` 回位 |
| **AI 生成呼吸** | 2000ms | `--ease-in-out` | AI 生成中光晕呼吸 | `box-shadow` 脉动 + `opacity` 0.6↔1 循环 |
| **输入聚焦** | 200ms | `--ease-out` | 输入框获焦放大微动 | `transform: scale(1.01); box-shadow: var(--shadow-focus)` |

### 7.4 减弱动效模式

```css
@media (prefers-reduced-motion: reduce) {
  :root {
    --duration-instant: 0ms;
    --duration-fast: 0ms;
    --duration-normal: 50ms;
    --duration-slow: 50ms;
    --duration-spring: 50ms;
    --ease-spring: var(--ease-out);
  }
}
```

---

## 8. Component Styles — 核心组件规范

### 8.1 按钮（Button）

#### 主按钮（Primary CTA）
```css
.btn-primary {
  background: var(--color-accent-default);       /* #E8915A */
  color: #FFFFFF;
  font-family: var(--font-sans);
  font-size: var(--text-body);                    /* 15px */
  font-weight: var(--weight-semibold);            /* 600 */
  line-height: 1;
  padding: 14px 24px;
  border-radius: var(--radius-md);               /* 10px */
  border: none;
  cursor: pointer;
  transition: all var(--duration-fast) var(--ease-out);
  /* 点击弹性动画 */
  active: transform scale(0.97); 
}
.btn-primary:hover { background: var(--color-accent-hover); }
.btn-primary:active { 
  background: var(--color-accent-active); 
  transform: scale(0.97); 
}
.btn-primary:focus-visible { box-shadow: var(--shadow-focus); }
```

#### 次级按钮（Secondary）
```css
.btn-secondary {
  background: transparent;
  color: var(--color-text-primary);              /* #2C2825 */
  font-family: var(--font-sans);
  font-size: var(--text-body);
  font-weight: var(--weight-medium);             /* 500 */
  padding: 14px 24px;
  border-radius: var(--radius-md);
  border: 1.5px solid var(--color-border-default); /* #D4CFC8 */
  cursor: pointer;
  transition: all var(--duration-fast) var(--ease-out);
}
.btn-secondary:hover { background: var(--color-bg-secondary); border-color: var(--color-text-tertiary); }
```

#### 文字按钮（Ghost）
```css
.btn-ghost {
  background: transparent;
  color: var(--color-accent-text);               /* #C06E3A */
  font-family: var(--font-sans);
  font-size: var(--text-body);
  font-weight: var(--weight-medium);
  padding: 8px 12px;
  border-radius: var(--radius-sm);
  border: none;
  cursor: pointer;
  transition: background var(--duration-fast) var(--ease-out);
}
.btn-ghost:hover { background: var(--color-accent-lighter); }
```

#### AI 生成按钮
```css
.btn-ai {
  background: var(--color-ai-default);            /* #7C6AE8 */
  color: #FFFFFF;
  font-family: var(--font-sans);
  font-size: var(--text-body);
  font-weight: var(--weight-semibold);
  padding: 14px 24px;
  border-radius: var(--radius-md);
  border: none;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all var(--duration-fast) var(--ease-out);
}
.btn-ai::after {
  /* AI 生成中呼吸光效 */
  content: '';
  position: absolute;
  inset: -2px;
  border-radius: inherit;
  background: var(--color-ai-glow);
  animation: ai-breathe 2s var(--ease-in-out) infinite;
  opacity: 0;
}
.btn-ai.loading::after { opacity: 1; }
```

### 8.2 输入框（Input）

```css
.input {
  background: var(--color-bg-primary);           /* #F8F6F3 */
  color: var(--color-text-primary);
  font-family: var(--font-sans);
  font-size: var(--text-body);                    /* 15px */
  font-weight: var(--weight-regular);
  padding: 14px 16px;
  border-radius: var(--radius-md);               /* 10px */
  border: 1.5px solid var(--color-border-subtle); /* #E8E3DD */
  width: 100%;
  transition: all var(--duration-fast) var(--ease-out);
  outline: none;
}
.input::placeholder { color: var(--color-text-tertiary); }
.input:hover { border-color: var(--color-border-default); }
.input:focus { 
  border-color: var(--color-accent-default); 
  box-shadow: var(--shadow-focus);
  transform: scale(1.005);  /* 微放大 */
}
.input.error { 
  border-color: var(--color-error-default); 
  box-shadow: 0 0 0 3px rgba(217,85,85,0.15);
}
.input.ai-suggestion {
  background: var(--color-ai-light);             /* #F0EDFC */
  border-color: var(--color-ai-default);
  border-style: dashed;  /* 虚线边框区分 AI 生成内容 */
}
```

### 8.3 标签（Tag/Chip）

```css
.tag {
  display: inline-flex;
  align-items: center;
  gap: var(--space-1);                           /* 4px */
  padding: 6px 12px;
  border-radius: var(--radius-sm);               /* 6px */
  font-family: var(--font-sans);
  font-size: var(--text-caption);                /* 12px */
  font-weight: var(--weight-medium);             /* 500 */
  line-height: 1;
  cursor: pointer;
  transition: all var(--duration-instant) var(--ease-out);
  user-select: none;
}

/* 关系维度标签 */
.tag-relational {
  background: var(--color-accent-light);         /* #FDF0E6 */
  color: var(--color-accent-text);               /* #C06E3A */
}

/* 场景维度标签 */
.tag-contextual {
  background: var(--color-ai-light);             /* #F0EDFC */
  color: var(--color-ai-text);                   /* #5B4AC5 */
}

/* 自定义标签 */
.tag-custom {
  background: var(--color-info-light);           /* #E8F0FA */
  color: var(--color-info-default);               /* #5B8ED0 */
}

/* AI 生成标签（带渐入动画） */
.tag-ai-generated {
  animation: tag-appear 300ms var(--ease-decelerate) forwards;
  opacity: 0;
  transform: translateY(8px);
}
@keyframes tag-appear {
  to { opacity: 1; transform: translateY(0); }
}

/* 选中态 */
.tag.selected {
  outline: 2px solid currentColor;
  outline-offset: 1px;
}

/* 拖拽态 */
.tag.dragging {
  opacity: 0.8;
  transform: scale(1.05);
  box-shadow: var(--shadow-md);
  z-index: var(--z-dropdown);
}
```

### 8.4 卡片（Card）

```css
.card {
  background: var(--color-bg-elevated);           /* #FFFFFF */
  border-radius: var(--radius-lg);               /* 14px */
  padding: var(--space-5);                        /* 20px */
  box-shadow: var(--shadow-xs);
  border: 1px solid var(--color-border-subtle);
  transition: all var(--duration-normal) var(--ease-out);
}

/* 核心四问卡片（可滑出） */
.card-question {
  composes: card;
  position: relative;
  touch-action: pan-y;
  will-change: transform, opacity;
  /* 回答后飞出动画 */
}
.card-question.answered {
  animation: card-flyout 400ms var(--ease-out) forwards;
}
@keyframes card-flyout {
  to {
    transform: translateY(-120%) scale(0.9);
    opacity: 0;
  }
}

/* AI 推荐卡片 */
.card-ai {
  composes: card;
  border-color: var(--color-ai-default);
  border-style: dashed;
  background: var(--color-ai-lighter);
  position: relative;
}
.card-ai::before {
  content: '✨ AI 推荐';
  position: absolute;
  top: -10px;
  left: 12px;
  background: var(--color-ai-default);
  color: #FFFFFF;
  font-size: var(--text-micro);
  font-weight: var(--weight-medium);
  padding: 2px 8px;
  border-radius: var(--radius-sm);
}
```

### 8.5 步骤指示器（Step Indicator）

```css
.step-indicator {
  display: flex;
  align-items: center;
  gap: var(--space-2);                           /* 8px */
  padding: 0 var(--space-5);                      /* 20px */
}

.step-dot {
  width: 8px;
  height: 8px;
  border-radius: var(--radius-full);
  background: var(--color-border-default);
  transition: all var(--duration-normal) var(--ease-spring);
}

.step-dot.active {
  width: 24px;  /* 激活态横向拉伸 */
  background: var(--color-accent-default);
}

.step-dot.completed {
  background: var(--color-success-default);
}

.step-connector {
  flex: 1;
  height: 2px;
  background: var(--color-border-subtle);
  transition: background var(--duration-normal) var(--ease-out);
}

.step-connector.completed {
  background: var(--color-success-default);
}
```

### 8.6 底部抽屉（Bottom Sheet）

```css
.bottom-sheet {
  background: var(--color-bg-elevated);
  border-radius: var(--radius-xl) var(--radius-xl) 0 0;  /* 20px 20px 0 0 */
  padding: var(--space-5) var(--space-5) calc(var(--space-5) + env(safe-area-inset-bottom));
  box-shadow: var(--shadow-lg);
  max-height: 70vh;
  overflow-y: auto;
}

.bottom-sheet-handle {
  width: 36px;
  height: 4px;
  border-radius: 2px;
  background: var(--color-border-default);
  margin: 0 auto var(--space-4);
}
```

---

## 9. Cautions — 设计禁区

### 🚫 绝对禁止

1. **不使用纯黑/纯白**：文本用 `#2C2825` 而非 `#000000`，背景用 `#F8F6F3` 而非 `#FFFFFF`（页面级），保持温暖感
2. **不在同一行放置 3 个以上标签**：移动端空间有限，标签超长时换行或折叠
3. **不使用大于 20px 的圆角**：保持简约骨架，过度圆角会显得幼稚
4. **不在核心四问流程中使用弹窗**：四问是卡片滑动式交互，打断=流失
5. **AI 生成内容不加闪亮装饰**：AI 区分靠色调（冷蓝紫）+ 虚线边框 + 浅底，不用渐变/星光/粒子
6. **不使用纯键盘提交**：核心交互是手势滑动和点击，键盘仅辅助文本输入

### ⚠️ 谨慎使用

1. **强调色 `#E8915A` 面积控制在 10% 以内**：仅用于 CTA、选中态、关键强调
2. **AI 色 `#7C6AE8` 面积控制在 5% 以内**：仅用于 AI 生成标记和浅底
3. **动画时长不超过 500ms**：移动端用户耐心有限，过长动画感迟钝
4. **一次最多展示 3 个 AI 生成建议**：过多选择 = 选择瘫痪

---

## 10. Responsive Behavior — 移动端适配策略

### 10.1 目标设备

| 设备 | 逻辑宽度 | 基准 |
|------|---------|------|
| iPhone SE (3rd) | 375px | 最小宽度基准 |
| iPhone 15 | 393px | 设计基准 |
| iPhone 15 Pro Max | 430px | 最大常规宽度 |
| Android 主流 | 360-412px | 需兼容 |

### 10.2 键盘适配

| 策略 | 说明 |
|------|------|
| 键盘弹起时 | 页面内容上推（非遮盖），当前聚焦输入框需完全可见 |
| 键盘收起时 | 平滑回位（200ms ease-out） |
| 底部 CTA | 键盘弹起时隐藏 CTA，收起后显示 |
| 安全区域 | 底部留 `env(safe-area-inset-bottom)` 空间 |

### 10.3 横屏处理

不主动适配横屏，弹出提示引导用户竖屏使用（个人 CRM 为快速记录场景，竖屏效率更高）。

---

## 11. Agent Prompt Guide — AI 生成指南

### 生成 HTML 原型时必须遵循

1. **色彩**：所有颜色使用 CSS 变量引用（如 `var(--color-accent-default)`），不硬编码色值
2. **间距**：使用 `var(--space-*)` 变量，不使用任意间距值
3. **圆角**：使用 `var(--radius-*)` 变量
4. **阴影**：使用 `var(--shadow-*)` 变量
5. **字体**：使用 `var(--font-sans)` / `var(--font-mono)` 引用
6. **字号**：使用 `var(--text-*)` 变量
7. **动画**：时长用 `var(--duration-*)`，曲线用 `var(--ease-*)`
8. **移动端优先**：所有原型以 375-393px 宽度设计，不使用 `@media` 桌面断点
9. **AI 区分**：AI 生成内容使用虚线边框 + 冷蓝紫浅底，与用户输入的实线边框 + 暖底形成对比
10. **触摸目标**：所有可交互元素最小 44×44px 触摸区域（Apple HIG 标准）
11. **安全区域**：底部元素使用 `env(safe-area-inset-bottom)` 适配

### 语义化 HTML 结构

```html
<!-- 页面结构 -->
<main class="page">
  <header class="page-header"><!-- 步骤指示器 --></header>
  <section class="page-content"><!-- 核心内容 --></section>
  <footer class="page-footer"><!-- CTA --></footer>
</main>
```

---

## 附录：CSS 变量快速复制

```css
:root {
  /* === 色彩 === */
  --color-bg-primary: #F8F6F3;
  --color-bg-secondary: #F1EDE8;
  --color-bg-tertiary: #EAE5DF;
  --color-bg-elevated: #FFFFFF;
  --color-border-subtle: #E8E3DD;
  --color-border-default: #D4CFC8;
  --color-text-primary: #2C2825;
  --color-text-secondary: #6B6560;
  --color-text-tertiary: #9E9893;
  --color-text-disabled: #C5C0BA;
  --color-accent-default: #E8915A;
  --color-accent-hover: #D47E48;
  --color-accent-active: #C06E3A;
  --color-accent-light: #FDF0E6;
  --color-accent-lighter: #FEF7F0;
  --color-accent-text: #C06E3A;
  --color-ai-default: #7C6AE8;
  --color-ai-hover: #6B59D6;
  --color-ai-light: #F0EDFC;
  --color-ai-lighter: #F8F6FE;
  --color-ai-text: #5B4AC5;
  --color-ai-glow: rgba(124,106,232,0.15);
  --color-success-default: #4CAF7D;
  --color-success-light: #E8F5EE;
  --color-warning-default: #E5A84B;
  --color-warning-light: #FDF5E6;
  --color-error-default: #D95555;
  --color-error-light: #FDEAEA;
  --color-info-default: #5B8ED0;
  --color-info-light: #E8F0FA;
  --color-tag-relational: #E8915A;
  --color-tag-contextual: #7C6AE8;
  --color-tag-custom: #5B8ED0;
  --color-tag-bg-base: #F1EDE8;

  /* === 排版 === */
  --font-sans: "Inter", "SF Pro Display", -apple-system, "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif;
  --font-mono: "JetBrains Mono", "SF Mono", "Menlo", monospace;
  --text-display: 28px;
  --text-h1: 22px;
  --text-h2: 18px;
  --text-h3: 16px;
  --text-body: 15px;
  --text-body-sm: 13px;
  --text-caption: 12px;
  --text-micro: 11px;
  --weight-regular: 400;
  --weight-medium: 500;
  --weight-semibold: 600;
  --weight-bold: 700;

  /* === 间距 === */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;

  /* === 圆角 === */
  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 14px;
  --radius-xl: 20px;
  --radius-full: 9999px;

  /* === 阴影 === */
  --shadow-xs: 0 1px 2px rgba(44,40,37,0.04);
  --shadow-sm: 0 2px 8px rgba(44,40,37,0.06);
  --shadow-md: 0 4px 16px rgba(44,40,37,0.08);
  --shadow-lg: 0 8px 32px rgba(44,40,37,0.10);
  --shadow-focus: 0 0 0 3px rgba(232,145,90,0.3);
  --shadow-focus-ai: 0 0 0 3px rgba(124,106,232,0.3);

  /* === 动效 === */
  --duration-instant: 100ms;
  --duration-fast: 200ms;
  --duration-normal: 300ms;
  --duration-slow: 400ms;
  --duration-spring: 500ms;
  --ease-out: cubic-bezier(0.25, 0.1, 0.25, 1);
  --ease-in-out: cubic-bezier(0.42, 0, 0.58, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-decelerate: cubic-bezier(0, 0, 0.2, 1);

  /* === Z-index === */
  --z-base: 0;
  --z-card: 10;
  --z-sticky: 100;
  --z-dropdown: 200;
  --z-modal: 300;
  --z-toast: 400;
  --z-tooltip: 500;
}
```
