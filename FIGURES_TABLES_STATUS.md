# 论文图表状态跟踪

> 本文件记录论文中所有图表的状态、来源映射和检查进度。
> 状态说明：待检查 | 通过 | 需修改（附说明）

---

## 第二章 DASpeech

### 表格

| 论文文件 | label | 原论文来源 | 中文化 | 布局 | 检查状态 |
|---------|-------|-----------|--------|------|---------|
| `Tables/daspeech_results.tex` | `tab:daspeech_main` | DASpeech论文 Table 1 (`Tables/table_main_result.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/daspeech_multilingual.tex` | `tab:daspeech_multilingual` | DASpeech论文 Table 2 左半 (`Tables/table_multilingual.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/daspeech_path_ablation.tex` | `tab:daspeech_path` | DASpeech论文 Table 2 右半 (`Tables/table_best_expect_path.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/daspeech_speaker.tex` | `tab:daspeech_speaker` | DASpeech论文 Table 3 (`Tables/table_speaker.tex`) | 已完成 | 原始宽度 | 待检查 |

### 图片

| 论文文件 | label | 图片文件 | 原论文来源 | 图片语言 | 检查状态 |
|---------|-------|---------|-----------|---------|---------|
| `Img/figure_daspeech.tex` | `fig:daspeech` | `Img/DASpeech.pdf` | DASpeech论文 Figure 1 (`Figures/figure_model.tex`)，已替换为中期报告中文版 | 中文 | 待检查 |
| `Img/figure_daspeech_decoding.tex` (左) | `fig:daspeech_decoding` | `Img/decode_time.pdf` | DASpeech论文 Figure 2 左 (`Figures/figure_decoding_speed.tex`, `Figures/decode_time.pdf`) | **英文，需转中文**（坐标轴: Decoding Time, Length of Source Speech） | 待检查 |
| `Img/figure_daspeech_decoding.tex` (右) | `fig:daspeech_tradeoff` | `Img/tradeoff.pdf` | DASpeech论文 Figure 2 右 (`Figures/figure_speedup.tex` 相关, `Figures/tradeoff.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, Speedup Ratio；图例全英文） | 待检查 |

| 内嵌于 `Tex/Chap_DASpeech.tex` | `fig:daspeech_batch` | `Img/daspeech_batch_speedup.pdf` | DASpeech论文 Appendix D Figure (`Figures/figure_speedup_png.pdf`) | **英文，需转中文**（坐标轴: Speedup Ratio, ASR-BLEU） | 待检查 |
| 内嵌于 `Tex/Chap_DASpeech.tex` (左) | `fig:daspeech_graph_size_s2t` | `Img/daspeech_graph_size_s2t.pdf` | DASpeech论文 Appendix E Figure 左 (`Figures/figure_graph_size_s2t.pdf`) | **英文，需转中文**（坐标轴: Phoneme-level BLEU, Size Factor） | 待检查 |
| 内嵌于 `Tex/Chap_DASpeech.tex` (右) | `fig:daspeech_graph_size_s2s` | `Img/daspeech_graph_size_s2s.pdf` | DASpeech论文 Appendix E Figure 右 (`Figures/figure_graph_size_s2s.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, Size Factor） | 待检查 |

### 英文图片翻译清单

需要你手动将以下图片中的英文转为中文：

1. **DASpeech.pdf**（模型架构图）：
   - "Target Mel-spectrogram" → "目标梅尔谱"
   - "Non-autoregressive Acoustic Decoder" → "非自回归声学解码器"
   - "Expect-Path Training" → "期望路径训练"
   - "Inference" → "推理"
   - "Directed Acyclic Graph" → "有向无环图"
   - "Non-autoregressive Linguistic Decoder (Self-Attn + Cross-Attn + FFN)" → "非自回归语言解码器（自注意力 + 交叉注意力 + 前馈网络）"
   - "Speech Encoder" → "语音编码器"
   - "Conformer Encoder" → "Conformer 编码器"
   - "Subsampler" → "下采样模块"
   - "Target Phoneme" → "目标音素"
   - "Linear + Softmax" → 可保留英文
   - "Positional Embeddings" → "位置编码"
   - "Attn" → 可保留

2. **decode_time.pdf**（解码延迟柱状图）：
   - Y轴 "Decoding Time (ms/sample)" → "解码时间（毫秒/样本）"
   - X轴 "Length of Source Speech (#Frames)" → "源语音长度（帧数）"
   - 图例中模型名可保留英文

3. **tradeoff.pdf**（质量-速度权衡散点图）：
   - Y轴 "ASR-BLEU" → 可保留
   - X轴 "Speedup Ratio" → "加速比"
   - 图例中模型名可保留英文

---

## 第三章 ComSpeech

（待写作时补充）

---

## 第四章 LLaMA-Omni

（待写作时补充）

---

## 第五章 LLaMA-Omni 2

（待写作时补充）

---

## 更新日志

- 2026-03-03：创建文件，录入第二章 DASpeech 全部图表（4表3图）
- 2026-03-04：所有图表标题改为简短风格（参照师兄论文），表格符号注释移至表格底部脚注
- 2026-03-04：DASpeech模型架构图替换为中期报告中文版
- 2026-03-04：新增3张图（批量解码加速比、图尺寸对S2TT的影响、图尺寸对DASpeech的影响），均为英文待转中文；speaker表去掉分类标签斜体
