# Design AI Skills

团队共用的设计 AI skills 仓库。

## 包含

- `skills/lark-user-feedback`：从飞书反馈群提炼用户反馈、主题聚类、优先级和设计机会点，生成带原文跳转和可视化分析的用研报告。

## 安装到 Codex 和 Claude Code

一键安装：

```bash
curl -fsSL https://raw.githubusercontent.com/easondoittt/design-ai-skills/main/install-lark-user-feedback.sh | bash
```

也可以手动安装：

```bash
git clone https://github.com/easondoittt/design-ai-skills.git ~/design-ai-skills
cd ~/design-ai-skills
./install-lark-user-feedback.sh
```

## 验证

```bash
grep '^version:' ~/.codex/skills/lark-user-feedback/SKILL.md
grep '^version:' ~/.claude/skills/lark-user-feedback/SKILL.md
readlink ~/.claude/skills/lark-user-feedback
```

两边都指向 `~/design-ai-skills/skills/lark-user-feedback`，且版本一致，就说明 Codex 和 Claude Code 使用同一份 skill。

## 更新

```bash
cd ~/design-ai-skills
git pull
```

如果本地用软链接安装，`git pull` 后 Codex 和 Claude Code 会自动读到新版。
