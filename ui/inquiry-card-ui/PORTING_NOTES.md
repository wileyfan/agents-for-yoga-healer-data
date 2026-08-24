# PORTING NOTES — inquiry-card-ui

## 来源

| 项 | 值 |
|---|---|
| 源仓库 | `wileyfan/betwell-docs` |
| 源路径 | `foundations/specs/` |
| 源 commit | `68ee286` |
| 同步日期 | 2026-06-12 |
| 同步方式 | 纯文件复制（无 git history） |
| 同步人 | wileyfan |

## 复制清单

| 源路径 | 目标路径 | 改动 |
|---|---|---|
| `foundations/specs/assets/betwell_tg_ai_consultation_ui.svg` | `assets/betwell_tg_ai_consultation_ui.svg` | 无 |
| `foundations/specs/betwell-telegram-ai-consultation-ui-v0.1.md` | `betwell-telegram-ai-consultation-ui-v0.1.md` | 无 |
| `foundations/specs/intake-card-typed-schema.json` | `intake-card-typed-schema.json` | 无 |
| — | `README.md` | 新建：三屏三纪律提炼 + 与本仓其它模块的关系 |

## 为什么搬到 agents-for-healer

- 抽卡问诊是疗愈瑜伽 L2a 度假村场景的核心交互模式
- 与本仓 `disciplines/therapeutic-yoga/agents/assessment/` 直接耦合
- typed schema 需要与 `platform/schemas/profile_schema.json` 字段对齐
- 原 betwell-docs 仓库是"foundations 决策档案"性质，不适合频繁迭代实现细节

## 与原仓的关系

- **本副本为后续唯一权威源**（实现层面）
- betwell-docs 原文件**保留**，作为决策时点的快照
- 若有 v0.2 / v0.3 迭代，**直接在本仓修改**，重大版本可回写 betwell-docs

## 未完成 / 待办

- [ ] 6 张固定卡组的 Telegram InlineKeyboard 渲染实现（对接 `betwell-cards` skill）
- [ ] 与 `assessment/` 智能体的 method 接口契约
- [ ] 与 ACSM 规则库的禁忌联动（屏 1 完成后触发 A 阶段评估）
- [ ] HIPAA / PDPA 合规审计清单
- [ ] L3 师傅手法 + 医师签字的链上锚定（P2 · Cloudflare）
