# Contributing

## Documentation sync rule · 文档同步规则

**English version below · 中文见下方**

Every change to the skill must update the documentation in **both languages, in the same commit**:

| If you change... | Then update... |
|---|---|
| `SKILL.md` (workflow, levers, ladder discipline) | The "Ladder discipline" + showcase-case behavior in both READMEs |
| `references/prompts.md` or `references/scenarios.md` | Links and any showcased examples in both READMEs |
| Trigger behavior / frontmatter description | The Usage / trigger sections in both READMEs |

**Pre-commit checklist:**

- [ ] `git diff README.md README.zh-CN.md` — both files reflect the change
- [ ] Showcase cases still match current `SKILL.md` behavior (recommended rung, effort, verification, teach-back)
- [ ] Both languages are structurally parallel: same sections, same tables, same examples

---

**中文版**

任何对 skill 的优化，都必须在**同一个提交内**更新**中英文双份**文档：

| 如果你改了… | 必须同步更新… |
|---|---|
| `SKILL.md`（工作流、杠杆、阶梯纪律） | 两份 README 中的"阶梯纪律"和展示案例的行为描述 |
| `references/prompts.md` 或 `references/scenarios.md` | 两份 README 中的链接和展示的示例 |
| 触发行为 / frontmatter 描述 | 两份 README 的"触发方式"章节 |

**提交前检查清单：**

- [ ] `git diff README.md README.zh-CN.md` —— 两个文件都体现了这次变更
- [ ] 展示案例仍与当前 `SKILL.md` 行为一致（推荐档位、成本、验证方式、teach-back）
- [ ] 中英结构对齐：章节相同、表格相同、案例相同
