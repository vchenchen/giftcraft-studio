# GiftCraft Studio · 礼创工坊

Bilingual Codex plugin for branded gifts, packaging and supplier preparation.
中英文品牌纪念品设计插件 · v1.0.5 · Vincent Chen

## 安装 / Install

1. 下载并解压下方完整插件ZIP，保留隐藏文件夹。
   Download and extract the ZIP below, preserving hidden folders.
2. 在装有Codex CLI的终端运行，将路径替换为实际解压位置：
   Register the extracted local marketplace, then install:

```sh
codex plugin marketplace add /absolute/path/to/GiftCraft_Studio_Plugin_1.0.5
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

先介绍功能，再收集行业、赠送对象、纪念场景、采购数量和单件预算；提醒上传官方Logo与参考图。收到简报后自动提出三方向并推荐一款，无需用户输入执行指令。
Starts with capabilities and a five-field brief, then automatically proposes three directions and recommends one.

## 生图备用流程 / Image fallback

多次生图失败后直接提供完整提示词，可用于新的支持生图对话或其他AI生图工具；Logo和参考图需重新上传。插件不提供独立图片服务，不保证修复网络错误。API备用方式仅在用户明确选择后使用。
Repeated failures produce a complete prompt for another image-capable chat or tool. Re-upload assets there. No independent image service or recovery guarantee is included.

## 下载 / Download

[完整插件ZIP / Complete plugin ZIP](GiftCraft_Studio_Plugin_1.0.5.zip)

## 验证 / Validate

Python 3.9+，仅使用标准库 / standard library only:

```sh
python3 scripts/validate_plugin.py
```

实际测试：Codex CLI识别、安装、启用通过；完整文件、相对路径和损坏输入检测通过。未验证新模型对话行为和实时生图恢复。
Verified: CLI discovery, installation, enablement, resource integrity and invalid-package checks. Fresh model conversation behavior and live image-service recovery remain unverified.

完整源码及下列目录均包含在ZIP中 / Complete source and the following directories are bundled inside the ZIP.

## 结构 / Structure

- `.agents/plugins/marketplace.json`: marketplace catalog.
- `plugins/giftcraft-studio/`: portable and Codex-compatible plugin manifests, icons and complete skill.
- `plugins/giftcraft-studio/skills/giftcraft-studio/templates/`: 9 bilingual templates.
- `plugins/giftcraft-studio/skills/giftcraft-studio/references/`: scoped edits, 6 industry examples and acceptance scenarios.

GitHub distribution only; not published in OpenAI's official public plugin directory.
此仓库为GitHub分发版本，并非OpenAI官方公共插件目录上架。

[测试报告 / Test report](TEST_REPORT.md)
