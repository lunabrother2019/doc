# Generative Agents 研究文档库

围绕 **Stanford Smallville**（Park et al. 2023, arXiv:2304.03442）展开的研究笔记与延伸阅读库。不含可执行代码，只有文档、概念图和论文深度解读。

## 入口

所有内容都可以从 [`html/index1.html`](html/index1.html) 导航进入。推荐阅读顺序：

1. **锚点**：`html/deep-dive/19-generative-agents.html` — 原论文深度解读
2. **全景**：`html/concepts-map.html` — 五支柱 × Top 15 概念 × 全演化图（3 Tab 可切换）
3. **论文索引**：`html/papers-reference.html` — 95 篇论文 3 视图（分类手册 / 卡片浏览 / 表格）
4. **深度解读**：`html/deep-dive/01-24` — 24 篇按主题分组的详读笔记
5. **挑战笔记**：`html/challenge/` — 自产思考（工程 gap / 验证鸿沟 / 开放问题）

## 目录结构

```
.
├── html/
│   ├── index1.html              # 导航中心
│   ├── concepts-map.html        # 概念图 3 Tab
│   ├── papers-reference.html    # 95 篇论文索引
│   ├── cot-reflexion-map.html   # CoT × Reflexion 专题关系图
│   ├── architecture-study.html  # Agent 架构学习（Claude Code 源码分析）
│   ├── study-guide.html         # 学习中心（3 Track）
│   ├── evolution-chains.html    # 演化链路专题
│   ├── deep-dive/               # 24 篇论文深度解读
│   │   ├── 01-06*.html          # 原始研究（01-03 初始，04-06 补充）
│   │   ├── 07-17*.html          # CoT 推理链系列（11 篇）
│   │   ├── 18-21*.html          # 记忆系列（HiAgent / Generative Agents 原论文 / A-MEM / MemoryOS）
│   │   └── 22-24*.html          # 多 Agent 协作 + 记忆综述（MetaGPT / ChatDev / Memory Survey）
│   └── challenge/               # 自产分析笔记
│       ├── open-problems.html
│       ├── validation-gap.html
│       ├── verification-testbeds.html
│       ├── user-simulation-challenges.html
│       ├── free-code-vs-reflexion.html
│       └── reflexion-architecture-comparison.html
├── logs/                        # 会话日志与阶段总结
│   ├── conversation-*.txt
│   └── session-summary-*.md
├── generative-agents-study-guide.md
├── session-summary-2026-04-05-06.md
├── CLAUDE.md                    # Claude Code 工作规范
└── README.md
```

## 标记约定

- **粉色虚线 "后加" 徽章**：所有用户补充的论文（区别于初始 01-03 的核心研究）
- **核心 5 支柱**：Memory Stream / Reflection / Planning / Action / Multi-Agent

## 复习路径

拓扑复习（4 阶段，总计 ~10 小时）：

| 阶段 | 时长 | 内容 |
|---|---|---|
| 0 锚点 | 1h | deep-dive 19（原论文） |
| 1 五支柱 | 3h | 每支柱主读 + 对照 |
| 2 两条演化链 | 4h | CoT 链（07→14）+ 记忆链（19→18→21→20→24） |
| 3 跨界启发 | 2h | 04/05 + 16/17 + 22/23 对照阅读 |

详见对话记录或在 `cot-reflexion-map.html` 查看三层阅读法。

## 论文追加工作流

用户提到新论文时触发的标准 3 步（详见 `CLAUDE.md`）：

1. **Deep Dive**：`html/deep-dive/NN-name.html` 新建页面，带"后加"徽章 + GitHub 链接
2. **Papers Reference**：在分类手册 / 卡片浏览 / 表格视图 3 处加条目
3. **Concept Map**：在"外围方法论启发"子图加粉色 ★后加 节点 + 论文卡片
