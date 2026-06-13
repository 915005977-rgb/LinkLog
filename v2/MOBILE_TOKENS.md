# LinkLog 移动端设计令牌

> 由彩格调（design-system-expert）产出 · 2026-06-13
> 基于 LinkLog V2 PC 端设计令牌，适配移动端 App（375px 优化，微信浏览器兼容）

---

## 完整 CSS :root 变量块

```css
:root {
  /* ============================================
     1. 色彩系统 — 温度梯度：暖灰 → 琥珀橘 → 冷蓝紫
     与 PC 端完全一致，不做裁剪
     ============================================ */

  /* --- 1.1 背景色 --- */
  --color-bg-primary: #F8F6F3;       /* 页面底色 · 暖灰 */
  --color-bg-secondary: #F1EDE8;     /* 区块底色 · 次暖灰 */
  --color-bg-tertiary: #EAE5DF;      /* 深层底色 · 三级暖灰 */
  --color-bg-elevated: #FFFFFF;      /* 卡片/弹层底色 · 白 */

  /* --- 1.2 边框色 --- */
  --color-border-subtle: #E8E3DD;    /* 微弱分割 */
  --color-border-default: #D4CFC8;   /* 默认分割 */

  /* --- 1.3 文字色 --- */
  --color-text-primary: #2C2825;     /* 主文字 */
  --color-text-secondary: #6B6560;   /* 辅助文字 */
  --color-text-tertiary: #9E9893;    /* 占位/提示 */
  --color-text-disabled: #C5C0BA;    /* 禁用态 */
  --color-text-on-accent: #FFFFFF;   /* 强调色上的文字 */

  /* --- 1.4 琥珀橘系（主强调） --- */
  --color-accent-default: #E8915A;   /* 主按钮/关键操作 */
  --color-accent-hover: #D47E48;     /* 按下态 */
  --color-accent-active: #C06E3A;    /* 激活态 */
  --color-accent-light: #FDF0E6;     /* 浅底标签 */
  --color-accent-lighter: #FEF7F0;   /* 极浅底 */
  --color-accent-text: #C06E3A;       /* 强调文字 */

  /* --- 1.5 冷蓝紫系（AI 智能） --- */
  --color-ai-default: #7C6AE8;       /* AI 标识/按钮 */
  --color-ai-hover: #6B59D6;         /* AI 按下态 */
  --color-ai-light: #F0EDFC;         /* AI 浅底 */
  --color-ai-lighter: #F8F6FE;       /* AI 极浅底 */
  --color-ai-text: #5B4AC5;          /* AI 文字 */
  --color-ai-glow: rgba(124,106,232,0.15); /* AI 光晕 */

  /* --- 1.6 语义色 --- */
  --color-success-default: #4CAF7D;
  --color-success-light: #E8F5EE;
  --color-warning-default: #E5A84B;
  --color-warning-light: #FDF5E6;
  --color-error-default: #D95555;
  --color-error-light: #FDEAEA;
  --color-info-default: #5B8ED0;
  --color-info-light: #E8F0FA;

  /* --- 1.7 标签色 --- */
  --color-tag-relational: #E8915A;   /* 关系标签 */
  --color-tag-contextual: #7C6AE8;   /* 语境标签 */
  --color-tag-custom: #5B8ED0;       /* 自定义标签 */
  --color-tag-bg-base: #F1EDE8;      /* 标签底色 */

  /* --- 1.8 四线档案色（移动端调整：提高饱和度以适应小尺寸） --- */
  --color-line-origin: #B8834A;          /* 身世线 · 暖棕 */
  --color-line-origin-light: #F5EDE3;
  --color-line-origin-subtle: rgba(184,131,74,0.12);
  --color-line-value: #C47A2E;           /* 价值线 · 琥珀金 */
  --color-line-value-light: #FBF0E2;
  --color-line-value-subtle: rgba(196,122,46,0.12);
  --color-line-connection: #4A9B7F;       /* 连接线 · 翠绿 */
  --color-line-connection-light: #E8F5EF;
  --color-line-connection-subtle: rgba(74,155,127,0.12);
  --color-line-action: #C45B5B;           /* 行动线 · 深红 */
  --color-line-action-light: #FBEBEB;
  --color-line-action-subtle: rgba(196,91,91,0.12);

  /* --- 1.9 透明度/毛玻璃色（移动端高频使用） --- */
  --color-bg-frosted: rgba(248,246,243,0.92);     /* 导航栏/底栏毛玻璃底 */
  --color-bg-glass: rgba(255,255,255,0.6);         /* 卡片毛玻璃 */
  --color-bg-card-glass: rgba(255,255,255,0.7);    /* 浮层毛玻璃 */
  --color-bg-cell-sticky: rgba(255,255,255,0.95);  /* Sticky 单元格底 */
  --color-bg-overlay: rgba(44,40,37,0.4);           /* ★ 遮罩层 · 移动端专属：底部Sheet/模态的背景遮罩 */
  --color-bg-overlay-heavy: rgba(44,40,37,0.6);     /* ★ 重遮罩层 · 移动端专属：全屏模态/确认弹窗的背景遮罩 */

  /* --- 1.10 AI 紫透明度变体 --- */
  --color-ai-border-subtle: rgba(124,106,232,0.2);
  --color-ai-bg-item: rgba(255,255,255,0.8);
  --color-ai-bg-item-border: rgba(124,106,232,0.15);
  --color-ai-bg-subtle: rgba(124,106,232,0.10);
  --color-ai-bg-faint: rgba(124,106,232,0.08);

  /* --- 1.11 图表色（复用 PC 端色板） --- */
  --color-chart-cat-1: #E8915A;
  --color-chart-cat-2: #7C6AE8;
  --color-chart-cat-3: #4A9B7F;
  --color-chart-cat-4: #C45B5B;
  --color-chart-cat-5: #B8834A;
  --color-chart-cat-6: #6B8FBF;
  --color-chart-cat-7: #D4A0C0;
  --color-chart-cat-8: #8B9E6B;


  /* ============================================
     2. 字体系统
     ============================================ */

  --font-sans: "Inter", "SF Pro Display", -apple-system, "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif;
  --font-mono: "JetBrains Mono", "SF Mono", "Menlo", monospace;

  /* --- 2.1 字号（移动端在 PC 基础上微调） --- */
  --text-display: 28px;     /* 大标题 · 仅首页问候语 */
  --text-h1: 22px;           /* 页面标题 */
  --text-h2: 18px;           /* 区块标题 */
  --text-h3: 16px;           /* 卡片标题 */
  --text-body: 15px;         /* 正文 */
  --text-body-sm: 13px;      /* 辅助正文 */
  --text-caption: 12px;      /* 标注/标签 */
  --text-micro: 11px;        /* 极小标注 */
  --text-overline: 10px;     /* ★ 移动端专属：极小大写标注，用于四线区块标题上方 */

  /* --- 2.2 字重 --- */
  --weight-regular: 400;
  --weight-medium: 500;
  --weight-semibold: 600;
  --weight-bold: 700;

  /* --- 2.3 行高 --- */
  --leading-tight: 1.25;    /* ★ 移动端专属：标题行高，避免多行标题行距过大 */
  --leading-normal: 1.5;    /* 正文行高 */
  --leading-relaxed: 1.65;  /* 长文行高 */


  /* ============================================
     3. 间距系统
     ============================================ */

  /* --- 3.1 基础间距（与 PC 端一致） --- */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;

  /* --- 3.2 ★ 移动端专属间距 --- */
  --space-screen-x: 20px;          /* ★ 屏幕左右安全内边距 · 375px 下保证舒适阅读宽度 335px */
  --space-screen-x-compact: 16px;  /* ★ 紧凑模式内边距 · 标签栏/搜索栏等需要更多内容宽度的场景 */
  --space-section-y: 32px;         /* ★ 区块间垂直间距 · 保证信息分组的呼吸感 */
  --space-card-stack: 12px;        /* ★ 卡片堆叠间距 · 同一区块内卡片之间的间距 */
  --space-list-item: 0px;          /* ★ 列表项间距 · 靠分隔线而非间距来区分，紧凑列表用 */
  --space-inline-chip: 6px;        /* ★ 标签气泡间距 · 同行标签之间的水平间距 */
  --space-inline-chip-row: 8px;    /* ★ 标签行间距 · 多行标签之间的垂直间距 */


  /* ============================================
     4. 圆角系统
     ============================================ */

  --radius-sm: 6px;        /* 小元素 · 标签/小按钮 */
  --radius-md: 10px;       /* 中元素 · 输入框/小卡片 */
  --radius-lg: 14px;       /* 大元素 · 卡片/区块 */
  --radius-xl: 20px;       /* 超大元素 · 底部Sheet/模态 */
  --radius-full: 9999px;   /* 圆形/胶囊 */
  --radius-sheet: 20px;    /* ★ 移动端专属：底部 Sheet 顶部圆角 */
  --radius-toast: 12px;    /* ★ 移动端专属：Toast 提示圆角 */


  /* ============================================
     5. 阴影系统
     ============================================ */

  --shadow-xs: 0 1px 2px rgba(44,40,37,0.04);
  --shadow-sm: 0 2px 8px rgba(44,40,37,0.06);
  --shadow-md: 0 4px 16px rgba(44,40,37,0.08);
  --shadow-lg: 0 8px 32px rgba(44,40,37,0.10);
  --shadow-focus: 0 0 0 3px rgba(232,145,90,0.3);
  --shadow-focus-ai: 0 0 0 3px rgba(124,106,232,0.3);
  --shadow-sheet: 0 -4px 24px rgba(44,40,37,0.10);  /* ★ 移动端专属：底部 Sheet 向上投影 */
  --shadow-nav: 0 1px 12px rgba(44,40,37,0.06);     /* ★ 移动端专属：导航栏投影，比 shadow-sm 更横向扩散 */
  --shadow-tab-bar: 0 -1px 8px rgba(44,40,37,0.05);  /* ★ 移动端专属：底栏投影，向上扩散 */


  /* ============================================
     6. 触摸目标 — ★ 移动端专属
     Apple HIG 要求 44px，Material 要求 48px
     LinkLog 取 44px 最小值，关键操作用 48px
     ============================================ */

  --touch-min: 44px;           /* 最小触摸目标 · 列表项/标签 */
  --touch-comfort: 48px;       /* 舒适触摸目标 · 主操作按钮/底部导航 */
  --touch-cta: 52px;           /* CTA 触摸目标 · 主要行动按钮高度 */
  --touch-icon: 40px;          /* 图标触摸目标 · 小图标按钮的点击区域 */
  --touch-gap: 8px;            /* 触摸目标间距 · 相邻可点击元素最小间距，避免误触 */
  --hit-slop: 4px;             /* 扩展点击区域 · 视觉小于 44px 的元素通过 padding 扩展至最小触摸目标 */


  /* ============================================
     7. 安全区域 — ★ 移动端专属
     适配 iPhone X+ 灵动岛 / 刘海屏
     及 Android 手势导航栏
     ============================================ */

  --safe-top: env(safe-area-inset-top, 0px);           /* 顶部安全区 · 状态栏高度 */
  --safe-bottom: env(safe-area-inset-bottom, 0px);      /* 底部安全区 · Home Indicator 高度 */
  --safe-left: env(safe-area-inset-left, 0px);          /* 左侧安全区 · 横屏时使用 */
  --safe-right: env(safe-area-inset-right, 0px);        /* 右侧安全区 · 横屏时使用 */
  --status-bar-height: 44px;                              /* 状态栏预估高度（不含灵动岛） */
  --home-indicator-height: 34px;                          /* Home Indicator 预估高度 */


  /* ============================================
     8. 导航栏 — ★ 移动端专属
     ============================================ */

  --nav-height: 44px;                /* 导航栏内容高度 */
  --nav-height-total: calc(var(--nav-height) + var(--safe-top));  /* 含安全区的总高度 */
  --nav-title-font-size: 17px;       /* 导航栏标题字号 */
  --nav-title-font-weight: 600;      /* 导航栏标题字重 */
  --nav-icon-size: 24px;             /* 导航栏图标尺寸 */
  --nav-bg: var(--color-bg-frosted); /* 导航栏背景 · 毛玻璃 */
  --nav-border: 0.5px solid var(--color-border-subtle);  /* 导航栏底部分割线 */

  /* --- 底部标签栏 --- */
  --tab-bar-height: 49px;            /* 底栏内容高度 · Apple HIG 标准 */
  --tab-bar-height-total: calc(var(--tab-bar-height) + var(--safe-bottom));  /* 含安全区总高度 */
  --tab-bar-bg: var(--color-bg-frosted);  /* 底栏背景 · 毛玻璃 */
  --tab-bar-border: 0.5px solid var(--color-border-subtle);  /* 底栏顶部分割线 */
  --tab-bar-icon-size: 24px;         /* 底栏图标尺寸 */
  --tab-bar-label-font-size: 10px;   /* 底栏标签字号 */
  --tab-bar-item-min-width: 64px;    /* 底栏单项最小宽度 */


  /* ============================================
     9. 底部 Sheet — ★ 移动端专属
     ============================================ */

  --sheet-bg: var(--color-bg-elevated);              /* Sheet 背景 */
  --sheet-radius: var(--radius-sheet);               /* Sheet 顶部圆角 */
  --sheet-handle-width: 36px;                         /* 拖拽指示条宽度 */
  --sheet-handle-height: 5px;                         /* 拖拽指示条高度 */
  --sheet-handle-radius: 2.5px;                       /* 拖拽指示条圆角 */
  --sheet-handle-color: rgba(44,40,37,0.15);          /* 拖拽指示条颜色 */
  --sheet-handle-margin-top: 8px;                     /* 拖拽指示条距顶部距离 */
  --sheet-padding-x: var(--space-screen-x);           /* Sheet 水平内边距 */
  --sheet-padding-bottom: calc(var(--space-6) + var(--safe-bottom));  /* 含安全区的底部内边距 */
  --sheet-min-height: 30vh;                           /* Sheet 最小高度 · 半屏 */
  --sheet-max-height: 90vh;                           /* Sheet 最大高度 · 几乎全屏 */
  --sheet-shadow: var(--shadow-sheet);                /* Sheet 阴影 */


  /* ============================================
     10. 卡片系统 — 移动端适配
     ============================================ */

  --card-bg: var(--color-bg-elevated);   /* 卡片背景 */
  --card-radius: var(--radius-lg);        /* 卡片圆角 14px */
  --card-border: 1px solid var(--color-border-subtle);  /* 卡片边框 */
  --card-shadow: var(--shadow-xs);        /* 卡片阴影 */
  --card-padding: var(--space-4);          /* 卡片内边距 16px */
  --card-padding-lg: var(--space-5);       /* 大卡片内边距 20px */
  --card-gap: var(--space-card-stack);     /* 卡片间距 12px */

  /* --- 人物卡片（首页联系人列表） --- */
  --person-card-height: 72px;              /* 卡片高度 · 包含头像+两行文字 */
  --person-card-padding: var(--space-3);   /* 卡片内边距 12px */
  --person-card-gap: var(--space-3);       /* 头像与文字间距 12px */
  --person-avatar-size: 48px;             /* 头像尺寸 · 列表视图 */
  --person-avatar-size-lg: 72px;          /* 大头像 · 详情页 */
  --person-avatar-radius: var(--radius-full); /* 头像圆角 · 圆形 */
  --person-avatar-placeholder-bg: var(--color-bg-secondary);  /* 头像占位底色 */


  /* ============================================
     11. 标签/气泡系统 — 移动端适配
     ============================================ */

  /* --- 标签气泡 --- */
  --chip-height: 28px;                  /* 标签高度 · 移动端比 PC 端稍大以保证可触摸 */
  --chip-height-compact: 24px;         /* 紧凑标签 · 空间有限时 */
  --chip-padding-x: 10px;              /* 标签水平内边距 */
  --chip-padding-x-compact: 8px;      /* 紧凑标签水平内边距 */
  --chip-font-size: var(--text-caption);  /* 标签字号 12px */
  --chip-font-size-compact: var(--text-micro);  /* 紧凑标签字号 11px */
  --chip-radius: var(--radius-full);   /* 胶囊圆角 */
  --chip-gap: var(--space-inline-chip);  /* 标签间距 6px */

  /* --- 标签颜色映射 --- */
  --chip-bg-relational: var(--color-accent-light);     /* 关系标签底色 */
  --chip-text-relational: var(--color-accent-text);     /* 关系标签文字 */
  --chip-bg-contextual: var(--color-ai-light);          /* 语境标签底色 */
  --chip-text-contextual: var(--color-ai-text);          /* 语境标签文字 */
  --chip-bg-custom: var(--color-info-light);             /* 自定义标签底色 */
  --chip-text-custom: var(--color-info-default);         /* 自定义标签文字 */
  --chip-bg-neutral: var(--color-tag-bg-base);           /* 中性标签底色 */
  --chip-text-neutral: var(--color-text-secondary);      /* 中性标签文字 */

  /* --- 可交互标签（筛选标签） --- */
  --chip-interactive-bg: var(--color-bg-secondary);
  --chip-interactive-bg-active: var(--color-accent-light);
  --chip-interactive-text: var(--color-text-secondary);
  --chip-interactive-text-active: var(--color-accent-text);
  --chip-interactive-border: 1px solid transparent;
  --chip-interactive-border-active: 1px solid var(--color-accent-default);
  --chip-interactive-min-width: var(--touch-min);  /* 保证最小触摸目标 */


  /* ============================================
     12. 输入框 — 移动端适配
     ============================================ */

  --input-height: var(--touch-comfort);        /* 输入框高度 48px · 舒适触摸目标 */
  --input-height-multiline: 100px;             /* 多行文本输入框高度 */
  --input-padding-x: var(--space-4);           /* 水平内边距 16px */
  --input-font-size: var(--text-body);          /* 字号 15px · 小于 16px 在 iOS 上会触发缩放，但 LinkLog 已设置 user-scalable=no */
  --input-bg: var(--color-bg-elevated);        /* 输入框背景 */
  --input-border: 1px solid var(--color-border-default);  /* 边框 */
  --input-border-focus: 1px solid var(--color-accent-default);  /* 聚焦边框 */
  --input-radius: var(--radius-md);            /* 圆角 10px */
  --input-placeholder-color: var(--color-text-disabled);   /* 占位文字色 */

  /* --- 搜索框 --- */
  --search-height: 40px;                       /* 搜索框高度 · 比标准输入框略小 */
  --search-radius: var(--radius-full);          /* 搜索框圆角 · 胶囊形 */
  --search-bg: var(--color-bg-secondary);       /* 搜索框背景 */
  --search-icon-color: var(--color-text-tertiary);  /* 搜索图标色 */
  --search-padding-x: var(--space-4);          /* 搜索框水平内边距 */
  --search-font-size: var(--text-body-sm);      /* 搜索框字号 13px */


  /* ============================================
     13. 按钮系统 — 移动端适配
     ============================================ */

  --btn-height-sm: 36px;              /* 小按钮高度 */
  --btn-height-md: var(--touch-comfort);  /* 中按钮高度 48px */
  --btn-height-lg: var(--touch-cta);     /* 大按钮高度 52px · CTA */
  --btn-padding-x-sm: 12px;
  --btn-padding-x-md: 20px;
  --btn-padding-x-lg: 24px;
  --btn-font-size-sm: var(--text-caption);   /* 12px */
  --btn-font-size-md: var(--text-body-sm);   /* 13px */
  --btn-font-size-lg: var(--text-body);       /* 15px */
  --btn-radius: var(--radius-md);             /* 10px */
  --btn-radius-full: var(--radius-full);      /* 胶囊按钮 */

  /* --- 主按钮（琥珀橘） --- */
  --btn-primary-bg: var(--color-accent-default);
  --btn-primary-bg-hover: var(--color-accent-hover);
  --btn-primary-bg-active: var(--color-accent-active);
  --btn-primary-text: var(--color-text-on-accent);
  --btn-primary-shadow: 0 2px 8px rgba(232,145,90,0.25);  /* 主按钮投影 */

  /* --- AI 按钮（冷蓝紫） --- */
  --btn-ai-bg: var(--color-ai-default);
  --btn-ai-bg-hover: var(--color-ai-hover);
  --btn-ai-text: var(--color-text-on-accent);
  --btn-ai-shadow: 0 2px 8px rgba(124,106,232,0.25);  /* AI 按钮投影 */

  /* --- 幽灵按钮 --- */
  --btn-ghost-bg: transparent;
  --btn-ghost-bg-hover: rgba(0,0,0,0.04);
  --btn-ghost-text: var(--color-text-secondary);
  --btn-ghost-border: 1px solid var(--color-border-default);

  /* --- 浮动操作按钮 FAB --- */
  --fab-size: 56px;                   /* FAB 尺寸 */
  --fab-radius: var(--radius-full);   /* 圆形 */
  --fab-bg: var(--color-accent-default);
  --fab-icon-size: 24px;
  --fab-shadow: 0 4px 16px rgba(232,145,90,0.3);
  --fab-bottom: calc(var(--tab-bar-height-total) + var(--space-4));  /* FAB 距底栏上方 16px */
  --fab-right: var(--space-screen-x);  /* FAB 距右边缘 20px */


  /* ============================================
     14. 分隔线
     ============================================ */

  --divider-color: var(--color-border-subtle);   /* 分隔线颜色 */
  --divider-thickness: 0.5px;                     /* 分隔线粗细 · 移动端用更细的线 */
  --divider-inset: var(--space-screen-x);         /* 分隔线左边距 · 与屏幕内边距对齐 */
  --divider-inset-with-avatar: calc(var(--person-avatar-size) + var(--person-card-gap) + var(--person-card-padding));  /* 带头像列表的分隔线左边距 */


  /* ============================================
     15. 四线档案系统 — 移动端适配
     ============================================ */

  /* --- 左侧指示条 --- */
  --line-indicator-width: 3px;          /* 默认指示条宽度 */
  --line-indicator-width-active: 4px;    /* 激活态指示条宽度 */
  --line-indicator-radius: 2px;          /* 指示条圆角 */

  /* --- 区块折叠/展开 --- */
  --line-section-padding: var(--space-4);           /* 四线区块内边距 16px */
  --line-section-header-height: var(--touch-min);   /* 区块头部高度 44px · 保证触摸目标 */
  --line-section-gap: var(--space-2);                /* 区块内字段间距 8px */
  --line-section-label-font-size: var(--text-micro); /* 区块标签字号 11px */
  --line-section-label-letter-spacing: 0.04em;      /* 区块标签字间距 */
  --line-section-value-font-size: var(--text-body-sm);  /* 区块内容字号 13px */
  --line-section-value-line-height: var(--leading-relaxed);  /* 区块内容行高 */

  /* --- 四线颜色变量映射（方便 JS 切换主题） --- */
  --line-origin-color: var(--color-line-origin);
  --line-origin-light: var(--color-line-origin-light);
  --line-value-color: var(--color-line-value);
  --line-value-light: var(--color-line-value-light);
  --line-connection-color: var(--color-line-connection);
  --line-connection-light: var(--color-line-connection-light);
  --line-action-color: var(--color-line-action);
  --line-action-light: var(--color-line-action-light);


  /* ============================================
     16. AI 破冰卡片 — 移动端适配
     ============================================ */

  --ai-card-bg: var(--color-ai-lighter);            /* AI 卡片底色 */
  --ai-card-border: 1px solid var(--color-ai-border-subtle);  /* AI 卡片边框 */
  --ai-card-radius: var(--radius-lg);               /* AI 卡片圆角 */
  --ai-card-padding: var(--space-4);                  /* AI 卡片内边距 */
  --ai-badge-size: 20px;                              /* AI 标记图标尺寸 · 移动端稍大 */
  --ai-badge-radius: var(--radius-sm);                /* AI 标记圆角 */
  --ai-glow-size: 80px;                               /* AI 光晕尺寸 */
  --ai-glow-color: var(--color-ai-glow);              /* AI 光晕颜色 */
  --ai-icebreak-font-size: var(--text-body);          /* 破冰话术字号 15px */
  --ai-icebreak-line-height: var(--leading-relaxed);  /* 破冰话术行高 */
  --ai-icebreak-text-color: var(--color-text-primary);  /* 破冰话术文字色 */


  /* ============================================
     17. 动效系统 — 移动端适配
     ============================================ */

  /* --- 时长 --- */
  --duration-instant: 100ms;   /* 即时反馈 · 按下态/切换 */
  --duration-fast: 200ms;     /* 快速过渡 · 标签切换 */
  --duration-normal: 300ms;   /* 标准过渡 · 页面切换 */
  --duration-slow: 400ms;    /* 慢速过渡 · 底部Sheet */
  --duration-spring: 500ms;  /* 弹性动画 · 气泡弹入 */

  /* --- 缓动 --- */
  --ease-out: cubic-bezier(0.25, 0.1, 0.25, 1);
  --ease-in-out: cubic-bezier(0.42, 0, 0.58, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);    /* 弹性缓动 · 气泡/卡片入场 */
  --ease-decelerate: cubic-bezier(0, 0, 0.2, 1);       /* 减速缓动 · 页面滑入 */
  --ease-accelerate: cubic-bezier(0.4, 0, 1, 1);       /* ★ 移动端专属：加速缓动 · 页面滑出 */

  /* --- ★ 移动端专属动画 --- */
  --motion-page-enter: var(--duration-normal) var(--ease-decelerate);      /* 页面进入 */
  --motion-page-exit: var(--duration-fast) var(--ease-accelerate);         /* 页面退出 */
  --motion-sheet-enter: var(--duration-slow) var(--ease-decelerate);       /* Sheet 展开 */
  --motion-sheet-exit: var(--duration-normal) var(--ease-accelerate);      /* Sheet 收起 */
  --motion-chip-pop: var(--duration-spring) var(--ease-spring);            /* 标签弹入 */
  --motion-card-swipe-threshold: 0.3;   /* ★ 卡片滑动触发阈值 · 滑动距离占卡片宽度的比例 */
  --motion-card-swipe-velocity: 0.5;    /* ★ 卡片滑动速度阈值 · px/ms，超过此速度直接触发 */
  --motion-haptic: light;                /* ★ 触觉反馈等级 · light/medium/heavy，用于 JS 调用 HapticFeedback */


  /* ============================================
     18. 页面布局 — ★ 移动端专属
     ============================================ */

  --page-max-width: 375px;              /* 设计基准宽度 */
  --page-min-width: 320px;              /* 最小支持宽度 · iPhone SE 1st gen */
  --page-max-width-tablet: 428px;       /* ★ 平板最大宽度 · iPhone 14 Pro Max / iPad mini */
  --page-bg: var(--color-bg-primary);   /* 页面底色 */
  --page-content-width: calc(100% - var(--space-screen-x) * 2);  /* 内容区实际宽度 335px @375 */

  /* --- 页面切换容器 --- */
  --page-stack-shadow: -2px 0 8px rgba(44,40,37,0.08);  /* 堆叠页面投影 · 详情页覆盖在列表上时 */

  /* --- 首页（Dashboard）布局 --- */
  --dashboard-greeting-margin-top: var(--space-6);      /* 问候语距顶部 24px */
  --dashboard-search-margin-top: var(--space-3);         /* 搜索框距问候语 12px */
  --dashboard-filter-margin-top: var(--space-3);         /* 筛选标签距搜索框 12px */
  --dashboard-list-margin-top: var(--space-4);           /* 列表距筛选标签 16px */
  --dashboard-filter-chip-wrap: wrap;                     /* 筛选标签换行 */


  /* ============================================
     19. 步骤流程 — ★ 移动端专属
     添加联系人 Step 1-3
     ============================================ */

  --step-indicator-height: 4px;          /* 步骤指示条高度 */
  --step-indicator-bg: var(--color-bg-tertiary);       /* 未完成步骤底色 */
  --step-indicator-active-bg: var(--color-accent-default);  /* 当前步骤色 */
  --step-indicator-done-bg: var(--color-success-default);   /* 已完成步骤色 */
  --step-indicator-radius: 2px;          /* 步骤指示条圆角 */
  --step-indicator-gap: var(--space-1);  /* 步骤指示条间距 4px */
  --step-header-height: 56px;            /* 步骤页头部高度 · 含返回+标题+跳过 */
  --step-content-padding: var(--space-screen-x);   /* 步骤页内容区水平内边距 */
  --step-field-gap: var(--space-5);      /* 步骤页字段间距 20px */
  --step-field-label-gap: var(--space-1); /* 字段标签与输入框间距 4px */
  --step-field-label-font-size: var(--text-caption);  /* 字段标签字号 */
  --step-field-label-color: var(--color-text-secondary);  /* 字段标签颜色 */
  --step-cta-bottom: calc(var(--safe-bottom) + var(--space-4));  /* CTA 按钮距底部距离 */
  --step-cta-width: calc(100% - var(--space-screen-x) * 2);     /* CTA 按钮宽度 · 全宽减去屏幕内边距 */


  /* ============================================
     20. Toast / 提示 — ★ 移动端专属
     ============================================ */

  --toast-bg: var(--color-text-primary);    /* Toast 背景 · 深色 */
  --toast-text: var(--color-text-on-accent); /* Toast 文字 · 白色 */
  --toast-radius: var(--radius-toast);        /* Toast 圆角 */
  --toast-padding: 12px 20px;                 /* Toast 内边距 */
  --toast-font-size: var(--text-body-sm);     /* Toast 字号 */
  --toast-min-width: 120px;                   /* Toast 最小宽度 */
  --toast-max-width: calc(100vw - var(--space-screen-x) * 2);  /* Toast 最大宽度 */
  --toast-bottom: calc(var(--tab-bar-height-total) + var(--space-4));  /* Toast 距底栏上方 */
  --toast-duration: 2500ms;                   /* Toast 显示时长 */


  /* ============================================
     21. 空状态 — ★ 移动端专属
     ============================================ */

  --empty-icon-size: 64px;                       /* 空状态图标尺寸 */
  --empty-icon-color: var(--color-text-disabled);  /* 空状态图标颜色 */
  --empty-title-font-size: var(--text-h3);        /* 空状态标题字号 */
  --empty-title-color: var(--color-text-secondary);  /* 空状态标题颜色 */
  --empty-desc-font-size: var(--text-body-sm);     /* 空状态描述字号 */
  --empty-desc-color: var(--color-text-tertiary);   /* 空状态描述颜色 */
  --empty-gap: var(--space-3);                      /* 空状态元素间距 */


  /* ============================================
     22. 时间感知问候 — ★ 移动端专属
     首页顶部的动态问候语
     ============================================ */

  --greeting-font-size: var(--text-display);   /* 问候语字号 28px */
  --greeting-line-height: var(--leading-tight); /* 问候语行高 */
  --greeting-font-weight: var(--weight-bold);   /* 问候语字重 */
  --greeting-color: var(--color-text-primary);  /* 问候语文字色 */
  --greeting-sub-font-size: var(--text-body-sm); /* 副问候语字号 */
  --greeting-sub-color: var(--color-text-secondary);  /* 副问候语颜色 */
  --greeting-sub-margin-top: var(--space-1);     /* 副问候语间距 */


  /* ============================================
     23. 微交互细节 — ★ 移动端专属
     ============================================ */

  --pull-to-refresh-threshold: 60px;        /* 下拉刷新触发距离 */
  --pull-to-refresh-indicator-size: 24px;  /* 下拉刷新指示器尺寸 */
  --overscroll-behavior: contain;           /* 阻止滚动穿透 */
  --scrollbar-display: none;                /* 移动端隐藏滚动条 · 由系统级滚动反馈替代 */
  --ios-rubber-band: auto;                  /* iOS 橡皮筋效果 · 在列表容器内设为 none 防止穿透 */
  --momentum-scroll: -webkit-overflow-scrolling: touch;  /* iOS 惯性滚动 */
}
```

---

## 令牌设计原则

### 色彩策略

移动端与 PC 端色彩系统**完全一致**，温度梯度叙事保持不变：暖灰 → 琥珀橘 → 冷蓝紫。移动端新增的 `--color-bg-overlay` 系列为底部 Sheet 和模态弹窗提供遮罩层，这是移动端高频出现的交互模式。

### 触摸优先

所有可交互元素必须满足 44px 最小触摸目标（`--touch-min`），CTA 按钮使用 52px（`--touch-cta`）。视觉尺寸小于 44px 的图标按钮通过 `--hit-slop` 扩展点击区域。相邻可点击元素间距至少 8px（`--touch-gap`）。

### 安全区域

使用 `env(safe-area-inset-*)` 适配灵动岛和手势导航栏，所有底部固定元素（底栏、CTA、Sheet）都预留了安全区域高度。

### 移动端间距

375px 宽度下屏幕内边距为 20px（`--space-screen-x`），保证内容区实际宽度 335px。这个值在紧凑模式下降至 16px，为标签筛选等需要更多水平空间的场景服务。

### 四线档案色

移动端沿用了 PC 端 V2 版本的四线色彩（暖棕/琥珀金/翠绿/深红），这套色彩比 V1 版本饱和度更高，在小尺寸指示条上更易辨识。

### 动效策略

移动端新增了 `--ease-accelerate` 和对应的页面/Sheet 退出动画，遵循 iOS Human Interface Guidelines 的进入减速、退出加速的动效模式。`--motion-card-swipe-threshold` 和 `--motion-card-swipe-velocity` 为卡片滑动手势提供判断依据。
