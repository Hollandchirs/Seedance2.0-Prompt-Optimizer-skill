# Seedance 2.0 视频提示词 Skill

[English](README.md)

适用于[即梦 Seedance 2.0](https://jimeng.jianying.com/)的 [Agent Skill](https://agentskills.io)，可生成电影级、平台合规的视频提示词。兼容 Claude Code、Cursor、Cline 等主流 AI 编程工具。

涵盖生成前信息收集、8大类型模板（动作/仙侠/广告/短剧/变身/舞蹈/生活/科幻）、SCELA公式结构化输出、版权角色安全替换，以及图片/视频/音频的 @ 引用语法。

## 功能特点

- **先问后生成** — 确认时长（5s/10s/15s）和风格后再生成，一次到位
- **8大类型模板（A–R）** — 动作战斗、仙侠奇幻、产品广告、霸总短剧、变身变装、舞蹈MV、生活治愈、科幻机甲
- **SCELA公式** — 主体 · 镜头 · 特效 · 光影 · 音效 结构化输出
- **版权安全替换** — 替换IP/明星时保留视觉相似度（颜色、服装、战斗风格）
- **纯净输出** — 不附加"禁止："说明行，不给出多余的风格建议
- **语言跟随** — 用户用什么语言提问，就用什么语言回复

## 安装

### 方式一：手动复制（推荐）

克隆或下载本仓库，将 skill 文件夹复制到 Claude skills 目录：

```bash
git clone https://github.com/Hollandchirs/seedance2.0.git
cp -r seedance2.0 ~/.claude/skills/seedance-bot
```

### 方式二：通过 skills CLI

```bash
npx skills add Hollandchirs/seedance2.0
```

然后对你的 AI 助手说：

> "帮我生成一个10秒科幻机甲战斗的视频提示词"

## Skill 文件说明

| 文件 | 说明 |
|---|---|
| [SKILL.md](SKILL.md) | 主 skill — 工作流、SCELA公式、输出规则 |
| [references/prompt-templates.md](references/prompt-templates.md) | 18个类型模板（A–R），附真实高分案例 |
| [references/compliance.md](references/compliance.md) | 版权替换规则与违禁内容处理 |
| [references/vocab.md](references/vocab.md) | 镜头语言、风格词汇、音效词汇表 |

## 工作流程

1. 用户描述视频创意
2. Skill 一次性询问时长和风格（不多轮追问）
3. 匹配最接近的类型模板
4. 用 SCELA 公式展开，填入具体特效、运镜、音效
5. 合规检查 — 将IP/品牌/真实人物内嵌替换
6. 输出干净可直接粘贴的提示词

## 参考资料

基于字节跳动官方文档：

- [Seedance 2.0 使用手册](https://bytedance.larkoffice.com/wiki/A5RHwWhoBiOnjukIIw6cu5ybnXQ) — 参数说明、交互方式、多模态能力与示例提示词
- [Seedance 2.0 真实案例](https://bytedance.larkoffice.com/wiki/LJXzwehluiFdzKkb1recZdfonZg) — 短剧制作、电商广告、舞蹈模仿、科普教育、AI MV 等

## 许可证

[MIT](LICENSE)
