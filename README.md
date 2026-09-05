# anime-lineart-director

动漫手绘线稿导演：把一句自然语言人物需求组织成可执行的日系动漫手写乱线速写提示词，并在环境支持图像生成时直接完成出图。

[查看作品画廊源码](https://github.com/Spark-chenlin/anime-lineart-director-gallery)

## 它解决什么问题

普通的“动漫线稿”提示往往只描述外观，容易出现人物身份不稳定、动作链断裂、双人关系混乱、全画面平均铺线或背景变成泛黄纸张等问题。

这个 Skill 会先锁定人物、事件和构图，再组织结构轮廓、方向性排线、局部高密区、受保护的脸和手，以及大面积呼吸留白。最终结果保持在一套明确的视觉范围内：清晰动漫母稿、手写乱线、角色主色墨线和克制的海报设计。

风格依据已整理在[视觉语法](references/visual-grammar.md)中，包含线层、密度、构图与配色规则；安装完整仓库即可使用，无需另行获取原始参考图片。可在[作品画廊](https://spark-chenlin.github.io/anime-lineart-director-gallery/)查看生成效果示例。

## 可以处理

- 单人头像、半身像、全身动作和角色海报；
- 情侣、搭档和多人关系构图；
- 角色主色转译为线稿颜色；
- 黑底反相、选择性平涂、双联画等受控机制；
- 同母稿配色变体和具有统一视觉 DNA 的系列组图；
- 已生成图片的偏差诊断与单变量修正；
- 用户明确要求的英文角色字标和 `ChenLin` 署名。

## 安装

把仓库克隆到当前工具使用的 Skills 目录中，确保 `SKILL.md` 位于 `anime-lineart-director` 文件夹根部。

```bash
git clone https://github.com/Spark-chenlin/anime-lineart-director.git
```

不同客户端的 Skills 目录可能不同，请以客户端的本地 Skill 配置为准。

## 使用示例

```text
用 anime-lineart-director 画五条悟抬手扶住眼罩，使用深靛蓝乱线，加入英文角色名和 ChenLin 署名。
```

```text
画一对恋人隔着窄白缝伸手相对，两个人使用各自的角色主色，不要让手指真正接触。
```

```text
给我三张同系列原创角色海报。统一笔触和白色画布，但每张使用不同动作、视线和构图。
```

需要提示词时直接说“给我提示词”；需要出图时明确说“直接出图”。图像生成依赖当前运行环境提供的生成能力。

## 仓库结构

```text
.
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ director-workflow.md
   ├─ modes-and-examples.md
   ├─ visual-grammar.md
   └─ eval-cases.md
```

`SKILL.md` 定义交互、任务路由和不可破坏的画面规则。`references/` 保存详细视觉语法、导演流程、模式示例和回归测试。

## 当前版本

`v1.0.0` · 首个对外正式版本 · 作者：尘林 Spark

此前的版本编号用于开发迭代，历史标签保留供追溯。

## License

[MIT](LICENSE)

