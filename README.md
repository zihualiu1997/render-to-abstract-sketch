# 效果图转抽象手绘 · render-to-abstract-sketch

把建筑、室内或景观效果图提炼成连笔、写意的黑白空间意向草图，用少量线条表达围合、悬挑、层叠与穿插。

**当前版本：v0.1.1 · 2026-10-20 · [MIT](LICENSE)**

## 下载与安装

[下载完整安装包](downloads/render-to-abstract-sketch-v0.1.1.zip)

解压后，把整个 `render-to-abstract-sketch` 文件夹放到项目的 `.agents/skills/` 下：

```text
你的项目/
└── .agents/
    └── skills/
        └── render-to-abstract-sketch/
            ├── SKILL.md
            ├── LICENSE
            ├── agents/openai.yaml
            └── references/
                ├── prompt-framework.zh-CN.md
                ├── style-gesture.jpg
                └── style-architectural.jpg
```

也可以复制本仓库的 `SKILL.md`、`LICENSE`、`agents/` 和 `references/` 到同名 Skill 文件夹。运行环境需要能读取图片并调用参考图生图／图像编辑工具；Skill 不包含模型服务或 API Key，也不绑定具体模型版本。

## 使用

上传一张效果图，然后发送：

```text
使用 $render-to-abstract-sketch，
将这张效果图转成连笔、写意的黑白空间意向手绘。
人物与配景只用一两笔带过。
```

## 工作方式

1. 从输入图提炼约 2—4 组空间关系，例如围合与空洞、悬挑与支撑、层叠与汇聚。
2. 将相邻关系合并为少量连续笔势，允许压缩透视、合并层次、留下开放轮廓。
3. 用笔触的提按、回带和粗细变化表达深度，以白纸表达空气、光和未画出的表面。
4. 将人物和配景简化为极少量墨迹，生成独立黑白草图并核对。

内容图决定空间与结构；随附参考图只决定笔势和抽象尺度，不将参考图中的建筑搬进结果。

## 输出与适用范围

默认输出一张独立黑白意向草图，不附原图或标题。适合探索空间意向与建筑表达；会主动省略构件、材质和精确层数，不作为工程图纸。

首批整理了椭圆围合、悬挑切口、错层路径三组案例，随后完成滨水双翼、错叠盒体两组新输入测试。滨水案例曾针对人物尺度符号进行一次局部修订。测试只说明这些输入的观察，不代表所有建筑类型或模型均有相同表现。测试照片和帖子内部资料不包含在安装包中。

## 文件

- [SKILL.md](SKILL.md)：运行规则与检查标准。
- [提示词框架](references/prompt-framework.zh-CN.md)：空间关系到生图提示词的组织方法。
- [连笔参考](references/style-gesture.jpg)：主要笔势参考。
- [建筑参考](references/style-architectural.jpg)：少量线条表达空间的辅助参考。
- [更新记录](CHANGELOG.md)。

## 许可

本仓库的原创 Skill 指令、提示词、文档，以及作者确认原创的两张随附参考图，统一采用 [MIT License](LICENSE)。允许商业使用、修改、出售与再分发；分发副本或实质性部分时，须保留版权声明和许可文本，无需公开修改后的源码。

本版本仅更新许可及分发说明，Skill 的生成逻辑和参考资源保持不变。历史版本曾以 Unlicense 发布；既有授权不因本次变更撤回。旧安装包可从 Git 历史追溯，当前下载入口仅提供 MIT 版本。

本许可针对仓库内容，不代替所使用图像模型服务的条款，也不替使用者取得其自行上传素材的权利。
