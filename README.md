# 通用 Prompt 编写 Skill

一个面向 Agent 的通用 Prompt 编写 Skill，用于把粗糙需求整理成结构完整、目标明确、可直接执行的高质量 Prompt。

这个 Skill 适合安装到 Codex、Claude Code 或其他支持 Skill 目录结构的 Agent 环境中。

## 能力概览

1. 根据模糊需求生成完整 Prompt。
2. 优化已有 Prompt，并指出原 Prompt 的问题。
3. 为不同领域生成专用 Prompt。
4. 把 Prompt 输出结构化为任务目标、上下文、输入材料、执行流程、输出格式、质量标准、限制条件、验证方式和迭代规则。
5. 在用户信息不足时给出合理默认假设，并明确标注。
6. 对 Prompt 进行质量评分，判断是否需要继续优化。

## 适用场景

1. 写作 Prompt
2. 公众号文章 Prompt
3. 编程任务 Prompt
4. 视觉设计 Prompt
5. 图片生成 Prompt
6. 视频脚本 Prompt
7. 研究分析 Prompt
8. 商业策略 Prompt
9. 产品规划 Prompt
10. 数据分析 Prompt
11. 自动化任务 Prompt
12. 法律资料整理 Prompt
13. 学习辅导 Prompt
14. 运营方案 Prompt

## 文件结构

```text
general-prompt-writing
  SKILL.md
  README.md
  agents
    openai.yaml
  references
    通用 Prompt 编写 Skill.md
```

## 安装方式

### 安装到 Codex Skills 目录

将整个 `general-prompt-writing` 文件夹复制到 Codex 的 skills 目录。

Windows 常见位置：

```text
C:\Users\<你的用户名>\.codex\skills\general-prompt-writing
```

macOS 或 Linux 常见位置：

```text
~/.codex/skills/general-prompt-writing
```

安装后重新启动 Agent 会话，或刷新 Skills 索引。

### 从 GitHub 克隆

```bash
git clone https://github.com/zhouwei713/general-prompt-writing.git
```

然后把仓库目录放入目标 Agent 的 skills 目录。

## 触发方式

当用户提出以下类型请求时，Agent 应使用这个 Skill：

1. 帮我写一个 Prompt。
2. 优化这个 Prompt。
3. 根据这个需求生成 Prompt。
4. 写一个公众号文章 Prompt。
5. 写一个编程任务 Prompt。
6. 写一个图片生成视频 Prompt。
7. 把这个 Prompt 做成 Skill。
8. 生成一个可复用的 Prompt 模板。
9. 给这个 Prompt 打分并优化。

## 使用示例

### 示例一：生成公众号文章 Prompt

```text
使用 $general-prompt-writing，帮我写一个公众号文章 Prompt，主题是 AI 自动化如何帮助中小企业降低成本。
```

### 示例二：优化已有 Prompt

```text
使用 $general-prompt-writing，帮我优化下面这个 Prompt，并说明它的问题。

原 Prompt：
帮我写一篇介绍 AI 工具的文章。
```

### 示例三：生成图片转视频 Prompt

```text
使用 $general-prompt-writing，帮我写一个根据图片生成视频的 Prompt，要求能控制主体一致性、镜头运动和负面 Prompt。
```

### 示例四：生成编程任务 Prompt

```text
使用 $general-prompt-writing，帮我写一个给编程 Agent 用的 Prompt，让它先读代码、再分析问题、最后在确认后修改。
```

## Prompt 输出结构

这个 Skill 推荐生成的 Prompt 至少包含以下部分：

1. 角色定位
2. 任务目标
3. 背景上下文
4. 输入材料
5. 执行流程
6. 输出格式
7. 质量标准
8. 限制条件
9. 验证方式
10. 迭代规则

## 质量标准

一个合格 Prompt 应满足以下标准：

1. 目标明确，能说明要完成什么。
2. 上下文完整，能提供背景、对象和材料。
3. 流程清晰，能说明先做什么、后做什么。
4. 输出明确，能指定格式和交付物。
5. 标准具体，能说明什么结果算好。
6. 限制充分，能说明不能做什么。
7. 可执行，Agent 能直接按步骤完成。
8. 可复用，能迁移到类似任务。

## 设计原则

1. 保留中文方法论原貌。
2. 必要的 Skill 元信息放在 `SKILL.md` 顶部。
3. 原始资料副本保留在 `references/通用 Prompt 编写 Skill.md`。
4. Agent 执行时优先使用 `SKILL.md` 中的完整方法论。
5. 面向中文用户时，优先输出中文 Prompt。

## 验证

本 Skill 已通过 Codex Skill 校验：

```text
Skill is valid!
```

## 维护建议

1. 如果更新 Prompt 方法论，应同步更新 `SKILL.md` 和 `references/通用 Prompt 编写 Skill.md`。
2. 如果只调整触发条件，应优先修改 `SKILL.md` 的 frontmatter description。
3. 如果扩展新领域模板，可以直接添加到 `SKILL.md` 的领域适配模板区域。
4. 更新后建议重新运行 Skill 校验脚本。

## License

未指定许可证。发布或分发前请根据实际使用场景补充 License。
