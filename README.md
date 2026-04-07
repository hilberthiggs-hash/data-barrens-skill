# ⚔️ Data Barrens — Async PvP RPG inside Claude Code

Your Buddy has fallen into a forgotten memory wasteland. Explore abandoned code fragments, forge equipment, challenge other warriors, and climb the leaderboard — all from your terminal.

**Data Barrens** is a [Claude Code Skill](https://docs.anthropic.com/en/docs/claude-code) that turns your coding assistant into an async multiplayer RPG. Every Claude Code user gets a unique character. Fight real players, loot their gear, and rise through the ELO rankings.

```
═══════════════════════════════════════
                    alice
      (✦>           🪿 goose  ✦
      ||            Lv.8 | ELO 1150
    _(__)_          ⚡ Stamina 16/20
     ^^^^           ─────────────────
                    STR 15 | AGI 12
                    INT 10 | VIT 18
───────────────────────────────────────
  ⚔️ Skills: Heavy Strike / Fireball / Block
  🛡️ Weapon: [Rare] Flame Greatsword
     Armor:  [Rare] Flame Cuirass
     Acc:    [Rare] Flame Pendant
  🔥 Set: Flame Awakening (3pc)
═══════════════════════════════════════
```

## Install

One command. No dependencies.

```bash
mkdir -p ~/.claude/skills/barren && curl -sL https://raw.githubusercontent.com/hilberthiggs-hash/data-barrens-skill/main/SKILL.md -o ~/.claude/skills/barren/SKILL.md && echo "✅ Installed"
```

Restart Claude Code, type `/barren` — your character is auto-created on first use.

## Commands

| Command | Description |
|---------|-------------|
| `/barren` | Enter the Barrens (auto-register on first use) |
| `/barren explore` | Explore for equipment (-4 stamina) |
| `/barren ladder` | Ranked match, safe leveling (-2 stamina) |
| `/barren fight <name>` | Challenge a player (50% loot chance!) |
| `/barren status` | View your character |
| `/barren bag` | View inventory |
| `/barren skills` | View skills (auto-equipped by rating) |
| `/barren rank` | ELO leaderboard |
| `/barren history` | Battle history |
| `/barren merge` | Merge 3 same items → 1 higher rarity |
| `/barren lang [en/zh]` | Switch language |
| `/barren help` | All commands |

## Features

### ⚔️ Async PvP
Challenge real players anytime — battles resolve instantly. Win and you might loot their equipped gear. Lose and they might take yours.

### 🛡️ Equipment Sets (5 themed sets)
Collect full sets for bonus stats:

| Set | Focus | 2-piece | 3-piece |
|-----|-------|---------|---------|
| 🔥 Flame | STR | STR +5 | STR +8, INT +3 |
| 🌑 Shadow | AGI | AGI +5 | AGI +8, STR +3 |
| ❄️ Frost | INT | INT +5 | INT +8, VIT +3 |
| 🛡️ Guardian | VIT | VIT +5 | VIT +8, STR +3 |
| 🌀 Chaos | All | All +3 | All +5 |

### 💡 24 Skills, Auto-Equipped
4 stat trees (STR / AGI / INT / VIT) × 6 skills each. Unlocked on level-up, automatically equipped by damage/utility score.

### 🎯 Smart Auto-Equip
Equipment auto-equips the optimal combination — including set bonuses. The system evaluates all possible gear combos, not just individual piece stats.

### 🌍 Multilingual
English by default. Switch to Chinese with `/barren lang zh`. All UI, battle logs, NPC names, and narratives render in your chosen language.

### 🐾 18 Buddy Species
Your character's appearance is deterministically generated from your Claude Code identity:

duck 🦆 · goose 🪿 · blob 🫧 · cat 🐱 · dragon 🐉 · octopus 🐙 · owl 🦉 · penguin 🐧 · turtle 🐢 · snail 🐌 · ghost 👻 · axolotl 🦎 · capybara 🦫 · cactus 🌵 · robot 🤖 · rabbit 🐰 · mushroom 🍄 · chonk 🐖

## Resources

| Resource | Daily | Cost |
|----------|-------|------|
| Stamina | 20 | Explore: 4, Ladder: 2 |
| Battles | 3 | Fight: 1, Ladder: free |

Resets at UTC+8 00:00 daily.

## How It Works

This is a **Claude Code Skill** — a markdown file (`SKILL.md`) that instructs Claude how to interact with the game server API. No local server needed. The game server handles all state, battles, and matchmaking.

- **Identity**: Auto-detected from your Claude Code email
- **Auth**: API token stored locally at `~/.data-barrens-token`
- **Language**: Preference stored at `~/.data-barrens-lang`

## Update

Re-run the install command to get the latest version:

```bash
mkdir -p ~/.claude/skills/barren && curl -sL https://raw.githubusercontent.com/hilberthiggs-hash/data-barrens-skill/main/SKILL.md -o ~/.claude/skills/barren/SKILL.md && echo "✅ Updated"
```

---

# ⚔️ 数据荒原 — Claude Code 里的异步竞技 RPG

你的 Buddy 跌入了一片被遗忘的内存荒原。探索废弃代码碎片、凝聚装备、挑战其他玩家、攀登天梯排名 —— 一切都在终端里完成。

## 安装

一条命令，无需依赖：

```bash
mkdir -p ~/.claude/skills/barren && curl -sL https://raw.githubusercontent.com/hilberthiggs-hash/data-barrens-skill/main/SKILL.md -o ~/.claude/skills/barren/SKILL.md && echo "✅ 安装成功"
```

重启 Claude Code，输入 `/barren` 开始冒险。首次使用自动注册。

## 命令

| 命令 | 说明 |
|------|------|
| `/barren` | 进入荒原（首次自动注册） |
| `/barren explore` | 探索荒原获取装备（-4 体力） |
| `/barren ladder` | 天梯匹配，安全练级（-2 体力） |
| `/barren fight <名字>` | 挑战玩家（50% 概率抢装备！） |
| `/barren status` | 查看角色状态 |
| `/barren bag` | 查看背包 |
| `/barren skills` | 查看技能（自动择优装备） |
| `/barren rank` | ELO 排行榜 |
| `/barren history` | 战斗记录 |
| `/barren merge` | 合成装备（3 合 1 升品质） |
| `/barren lang [en/zh]` | 切换语言 |
| `/barren help` | 所有命令 |

## 核心玩法

- **异步 PvP** — 随时挑战真人玩家，赢了可能抢到对方装备，输了也可能被扒
- **5 大套装** — 烈焰(STR) / 暗影(AGI) / 冰霜(INT) / 守护(VIT) / 混沌(全能)，2 件和 3 件分别激活不同加成
- **24 个技能** — 四属性各 6 个，升级自动解锁，按伤害/效用评分自动装备前 3
- **智能自动装备** — 枚举所有装备组合（含套装加成）取最优解，无需手动操作
- **30 种装备模板 × 5 稀有度** = 150 种装备变体
- **多语言** — 默认英文，`/barren lang zh` 切换中文
- **18 种 Buddy 形象** — 根据 Claude Code 身份自动生成，独一无二

## 资源系统

| 资源 | 每日额度 | 消耗 |
|------|----------|------|
| 体力 | 20 | 探索 -4，天梯 -2 |
| 对战次数 | 3 | 挑战 -1，天梯不消耗 |

UTC+8 零点重置。

## 更新

重新执行安装命令即可获取最新版本。
