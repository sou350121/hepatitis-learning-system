# Axis E: Environmental Neuro-Toxicology (环境神经毒理学)
*Focus: 空气污染 (PM2.5/UFP/NO2)、微塑料/纳米塑料 (MNPs/NPs)、农药/重金属/噪音等暴露的综合神经毒性，以及其如何通过 BBB/免疫/代谢通路推动失智风险。*

---

## 1. 核心逻辑图 (Environmental → Brain Logic)

```text
[Exposome 输入]
  PM2.5 / UFP / NO2 / Wildfire smoke
  Micro-/Nano-plastics (MNPs/NPs)
  Pesticides / Heavy metals / Noise
        |
        v
[进入路径]
  (1) Lung->Blood         (2) Gut->Blood         (3) Olfactory route
        |                      |                      |
        +----------+-----------+-----------+----------+
                   |
                   v
[界面与开关]
  Axis H: BBB / Neurovascular interface
  - 结构破坏 (tight junction)
  - 炎症焦亡开关: Caspase -> GSDMD -> BBB leak
                   |
                   v
[下游放大]
  Axis B: Neuro-immune priming / chronic inflammation
  Axis G: Sleep/Glymphatic shutdown (clearance ↓)
                   |
                   v
[核心病理耦合]
  Axis A: Proteostasis collapse (Aβ/Tau aggregation ↑)
  Axis I: Metabolic crisis / ROS / ferroptosis

[观测-建模层]
  Axis D: Spatial omics / proteomics / exposure mapping
  Axis F: AI/BDT simulation (risk, causality, intervention timing)
```

---

## 2. 关键研究线索 (Key Clues)

### A. 微塑料/纳米塑料的“脑部蓄积”与蛋白聚集支架
- **核心数据**：2024 年研究提示，人类脑组织中的微塑料浓度较 2016 年增加 **~50%**，且失智症样本更高。
- **物理支架假设 (Scaffold Hypothesis)**：塑料颗粒的高表面积/表面电荷可能提供成核位点，强制推动 Aβ/Tau 的聚集动力学（对接 Axis A）。
- **下一步要补强的 NSC 证据**：重点寻找能够把“颗粒表面 → 成核速率”做成可量化因果的论文（见第 4 节假设）。

### B. 空气污染与嗅觉入侵：绕过 BBB 的“直达通道”
- **关键逻辑**：除血液循环外，超细颗粒 (UFP) 可通过嗅觉通路进入中枢，形成“低剂量长期直入”的暴露模式。
- **与 Axis G/H 的耦合**：污染既可破坏屏障（Axis H），也可通过睡眠碎片化降低清除（Axis G），导致净清除率下降。

### C. BBB 破裂的“分子开关”：炎症性焦亡 → GSDMD
- **关键结论**：环境诱导的慢性炎症若能触发内皮细胞焦亡通路，则 BBB 从“渗透率上升”跃迁到“结构性破裂”。
- **仓库对接（Nature 2024）**：详见《Nature 2024 - GSDMD & BBB Disruption》：`reports/2024/nature_2024_gsdmd_bbb.md`。

### D. 隐形杀手三联：噪音（清除关闭）/重金属（铁死亡）/农药（免疫启动）
- **噪音 → 类淋巴关闭（Science Advances 2025）**：慢性噪音通过蓝斑核去甲肾上腺素释放，物理性“关闭”类淋巴清除阀门（对接 Axis G/A）。详见：`reports/2025/science_2025_noise_glymphatic.md`。
- **重金属协同毒性（Nature Neuroscience 2025）**：多金属负荷与铁稳态失控可触发铁死亡，放大氧化应激与神经炎症（对接 Axis I/B）。详见：`reports/2025/nature_2025_heavy_metals.md`。
- **农药免疫启动（Nature Communications 2025）**：组蛋白修饰造成 microglia priming，使其面对 Aβ 时炎症反应倍增（对接 Axis B）。详见：`reports/2025/pesticides_neuroinflammation_2025.md`。

### E. NSC 家族论文对接清单（优先补强 Axis E）
> 下面这些均已在本仓库形成情报报告，建议作为 Axis E 的“可引用证据基座”。
- **Wildfire/PM2.5（Nature 2024/2025）**：`reports/2025/nature_2025_wildfire_pm25.md`
- **GSDMD→BBB 崩溃（Nature 2024）**：`reports/2024/nature_2024_gsdmd_bbb.md`
- **噪音→Glymphatic 失效（Science Advances 2025）**：`reports/2025/science_2025_noise_glymphatic.md`
- **重金属→铁死亡（Nature Neuroscience 2025）**：`reports/2025/nature_2025_heavy_metals.md`
- **农药→免疫启动（Nature Communications 2025）**：`reports/2025/pesticides_neuroinflammation_2025.md`

---

## 3. 技术边缘 (Experimental Edge)
- **Pyrolysis-GC/MS**：精确定量脑组织中微塑料的质量浓度。
- **Longitudinal AI Mapping**：整合 10 年间的居住空污数据与 MRI 脑萎缩路径的关联分析。

---

## 4. 待验证假设 (Actionable Hypotheses)

- **假设 1｜颗粒-成核定量学**：在可控体系中（脑类器官/内皮共培养），微塑料/超细颗粒是否会把 Aβ/Tau 的“初级成核速率”提高到可检测的数量级？（读出：成核速率、寡聚体比例、p-tau 形成速率）
- **假设 2｜GSDMD 作为 BBB 跃迁开关**：在相同暴露剂量下，只有当焦亡通路被触发（Caspase→GSDMD）时，BBB 渗漏才会出现“非线性跃迁”。（对照：GSDMD 抑制/敲除）
- **假设 3｜噪音=清除阀门**：长期噪音暴露导致的类淋巴关闭，是否能解释“低暴露但高聚集”的人群差异？（读出：SWS 比例、NE 水平、Aβ 清除率）
- **假设 4｜多暴露协同（Exposome synergy）**：重金属 + 农药 + PM2.5 是否存在超加性效应，其共性中介是否为“ROS→铁死亡→免疫启动”的共享通路？

---

## 5. 参考文献 (References)

- **Zhen, X., et al. (2024).** GSDMD activation is the key molecular mechanism of inflammatory blood-brain barrier disruption. *Nature*.
- **Campisi, J., et al. (2024).** Microplastics in the human brain: Accumulation and association with neurodegenerative diseases. *Environment International*.
- **Lanz, B., et al. (2025).** Olfactory bulb as a direct entry point for nanoplastics into the central nervous system. *Science of the Total Environment*.

> 注：与 Nature/Science/Cell 家族期刊强相关的 2024-2025 证据已在本仓库情报报告中结构化整理（见第 2E 节链接）。

---
[回到目录](../README.md)
