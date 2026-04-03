# ⚔️ Data Barrens — 数据荒原

一个运行在 Claude Code 里的异步竞技 RPG 游戏。

你的 Buddy 跌入了一片被遗忘的内存荒原，在这里觉醒了战斗本能。探索碎片、锻造装备、挑战其他战士，书写属于你们的传说。

## 安装

终端执行一条命令：

```bash
mkdir -p ~/.claude/skills/barren && curl -sL https://raw.githubusercontent.com/hilberthiggs-hash/data-barrens-skill/main/SKILL.md -o ~/.claude/skills/barren/SKILL.md && echo "✅ 安装成功，重启 Claude Code 后输入 /barren"
```

重启 Claude Code，输入 `/barren` 即可开始冒险。首次使用会自动注册，继承你的 /buddy 形象。

## 玩法

| 命令 | 说明 |
|------|------|
| `/barren status` | 查看角色状态 |
| `/barren ladder` | 天梯匹配（安全练级） |
| `/barren fight @玩家名` | 指定玩家对战（有装备掉落风险！） |
| `/barren explore` | 探索荒原获取装备 |
| `/barren bag` | 查看背包 |
| `/barren equip <id>` | 穿戴装备 |
| `/barren skills` | 查看技能 |
| `/barren rank` | 排行榜 |
| `/barren help` | 所有命令 |

## 资源系统

- **体力**：每日 20 点，探索消耗 4 点（最多 5 次），天梯消耗 1 点
- **对战次数**：每日 3 次，天梯/指定对手共享
- UTC+8 零点重置

## 战斗机制

- **天梯**：随机匹配 ELO 相近对手（NPC + 玩家），不掉装备
- **指定对战**：只能打玩家，赢了 30% 概率抢对方装备，输了也可能被抢
- 属性升级时自动随机分配，无需手动加点
- 技能随等级自动解锁，可自由搭配（最多 3 个）

## 特色

- 自动继承你的 Claude Code /buddy 外观
- 邮箱唯一身份，一人一号
- API Token 认证，安全可靠
- 28 个 NPC 覆盖 Lv1-28，冷启动即可畅玩
