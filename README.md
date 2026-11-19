# GiftCraft Studio · 礼创工坊

Bilingual Codex plugin for branded gifts, packaging and supplier preparation.
中英文品牌纪念品设计插件 · v1.1.0 · Vincent Chen

## 安装 / Install

1. 下载并解压下方完整插件ZIP，保留隐藏文件夹。
   Download and extract the ZIP below, preserving hidden folders.
2. 在装有Codex CLI的终端运行，将路径替换为实际解压位置：
   Register the extracted local marketplace, then install:

```sh
codex plugin marketplace add /absolute/path/to/GiftCraft_Studio_Plugin_1.1.0
codex plugin add giftcraft-studio@giftcraft-local
```

重启或刷新 Codex，打开新对话并输入 `$giftcraft-studio`。
Restart or refresh Codex, open a new chat and invoke `$giftcraft-studio`.

已有同名独立Skill时可能显示重复入口；确认插件可用后再自行停用旧入口。
If a standalone skill with the same name is installed, duplicate selectors may appear.

## 功能 / Features

- 创意设计 / Gift concepts: default three distinct directions, or a requested count.
- 方案比较 / Concept comparison: brand, perceived value, emotion, quality and feasibility.
- 产品效果图 / Product visualization: uses available host image tools.
- 包装设计 / Packaging: box, insert, finishes, copy and opening views.
- 精准修改 / Scoped revisions: change specified elements while preserving the rest.
- 生产准备 / Production preparation: specifications, itemized costs, RFQs and QC checklists.

简短开场后一次收集六项资料：品牌名称、行业、赠送对象、纪念场景、采购数量、单件预算。每轮提供五款不同礼品、按场景评分并推荐一款；不满意则根据反馈继续提出新的五款，直到满意。用户满意并确认出图、官方素材齐备后，五款各生成一张礼品本体效果图。
Brief opening and six-field intake → five concepts with scenario-adjusted scores and one recommendation → feedback rounds until satisfied → explicit image authorization and official assets → five separate product-only images.

预算或数量未知时按场景提供选项；不报数字成本估价、不承诺预算内，报价和交期由用户与制造商确认。默认排除食品酒类保健品、电池电子类和易碎笨重不便携带品；只预留个性化区域，不处理名单。精准改图出现额外变化时展示偏差，交用户决定是否修正。
Scenario-specific planning bands, no numerical cost estimates or budget/lead-time promises. No personalization lists. Unintended image changes are shown for user decision.

## 生图备用流程 / Image fallback

多次生图失败后直接提供完整提示词，可用于新的支持生图对话或其他AI生图工具；Logo和参考图需重新上传。插件不提供独立图片服务，不保证修复网络错误。API备用方式仅在用户明确选择后使用。
Repeated failures produce a complete prompt for another image-capable chat or tool. Re-upload assets there. No independent image service or recovery guarantee is included.

## 下载 / Download

[完整插件ZIP / Complete plugin ZIP](GiftCraft_Studio_Plugin_1.1.0.zip)

## 验证 / Validate

Python 3.9+，仅使用标准库 / standard library only:

```sh
python3 scripts/validate_plugin.py
```

实际测试：Codex CLI识别、安装、启用通过；完整文件、相对路径和损坏输入检测通过。用户已反馈v1.1.0本机使用正常；自动检查覆盖安装和文件完整性，不代表图片服务可靠性已全面验证。
Verified: CLI discovery, installation, enablement, resource integrity and invalid-package checks. The user reports successful local usage of v1.1.0. Automated checks verify package integrity and installation; comprehensive live image reliability is not established.

完整源码及下列目录均包含在ZIP中 / Complete source and the following directories are bundled inside the ZIP.

## 结构 / Structure

- `.agents/plugins/marketplace.json`: marketplace catalog.
- `plugins/giftcraft-studio/`: portable and Codex-compatible plugin manifests, icons and complete skill.
- `plugins/giftcraft-studio/skills/giftcraft-studio/templates/`: 10 bilingual templates.
- `plugins/giftcraft-studio/skills/giftcraft-studio/references/`: scoped edits, 6 industry examples and acceptance scenarios.

GitHub distribution only; not published in OpenAI's official public plugin directory.
此仓库为GitHub分发版本，并非OpenAI官方公共插件目录上架。

[测试报告 / Test report](TEST_REPORT.md)

## v1.1.0 更新 / Changes

五款反馈循环、六项开场资料、五张独立产品图、动态评分、品牌背景与素材分检、单款失败提示词交付及用户决定精准修改偏差。
Five-concept satisfaction loop, six-field intake, five separate visuals, dynamic scoring, separate brand/asset checks and partial-failure handoffs.
