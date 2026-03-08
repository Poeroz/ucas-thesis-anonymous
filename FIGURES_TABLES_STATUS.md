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
| `Img/figure_daspeech_decoding.tex` | `fig:daspeech_decoding` | `Img/decode_time.pdf` | DASpeech论文 Figure 2 左 (`Figures/figure_decoding_speed.tex`, `Figures/decode_time.pdf`) | **英文，需转中文**（坐标轴: Decoding Time, Length of Source Speech） | 待检查 |
| 内嵌于 `Tex/Chap_DASpeech.tex` | `fig:daspeech_tradeoff` | `Img/tradeoff.pdf` | DASpeech论文 Figure 2 右 (`Figures/figure_speedup.tex` 相关, `Figures/tradeoff.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, Speedup Ratio；图例全英文） | 待检查 |
| 内嵌于 `Tex/Chap_DASpeech.tex` | `fig:daspeech_batch` | `Img/daspeech_batch_speedup.pdf` | DASpeech论文 Appendix D Figure (`Figures/figure_speedup_png.pdf`) | **英文，需转中文**（坐标轴: Speedup Ratio, ASR-BLEU） | 待检查 |
| 内嵌于 `Tex/Chap_DASpeech.tex` (subfigure) | `fig:daspeech_graph_size` | 总图，含下面两子图 | DASpeech论文 Appendix E Figure | — | 待检查 |
| 　└ 子图(a) | `fig:daspeech_graph_size_s2t` | `Img/daspeech_graph_size_s2t.pdf` | DASpeech论文 Appendix E Figure 左 (`Figures/figure_graph_size_s2t.pdf`) | **英文，需转中文**（坐标轴: Phoneme-level BLEU, Size Factor） | 待检查 |
| 　└ 子图(b) | `fig:daspeech_graph_size_s2s` | `Img/daspeech_graph_size_s2s.pdf` | DASpeech论文 Appendix E Figure 右 (`Figures/figure_graph_size_s2s.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, Size Factor） | 待检查 |

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

### 表格

| 论文文件 | label | 原论文来源 | 中文化 | 布局 | 检查状态 |
|---------|-------|-----------|--------|------|---------|
| `Tables/comspeech_results.tex` | `tab:comspeech_main` | ComSpeech论文 Table 1 (`Tables/table_main_results.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/comspeech_blaser.tex` | `tab:comspeech_blaser` | ComSpeech论文 Table 3 (`Tables/table_blaser.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/comspeech_objectives.tex` | `tab:comspeech_objectives` | ComSpeech论文 Table 4 (`Tables/table_objectives.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/comspeech_pretrain.tex` | `tab:comspeech_pretrain` | ComSpeech论文 Table 5 (`Tables/table_pretrain.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/comspeech_gap.tex` | `tab:comspeech_gap` | ComSpeech论文 Table 2 (`Tables/table_gap.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/comspeech_adaptor.tex` | `tab:comspeech_adaptor` | ComSpeech论文 Table 6 (`Tables/table_adaptor.tex`) | 已完成 | 原始宽度 | 待检查 |

### 图片

| 论文文件 | label | 图片文件 | 原论文来源 | 图片语言 | 检查状态 |
|---------|-------|---------|-----------|---------|---------|
| `Img/figure_comspeech.tex` | `fig:comspeech` | `Img/ComSpeech.pdf` | 已替换为中期报告中文版 | 中文 | 通过 |
| `Img/figure_comspeech_training.tex` | `fig:comspeech_training` | `Img/ComSpeech_training.pdf` | 已替换为中期报告中文版，宽度调为0.9 | 中文 | 通过 |
| 内嵌于 `Tex/Chap_ComSpeech.tex` | `fig:comspeech_tts_data` | `Img/comspeech_tts_data_size.pdf` | ComSpeech论文 Figure 4 (`Figures/figure_data_size.crop.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, TTS Data Size） | 待检查 |
| 内嵌于 `Tex/Chap_ComSpeech.tex` | `fig:comspeech_s2tt_data` | `Img/comspeech_s2tt_data_size.pdf` | ComSpeech论文 Figure 5 (`Figures/figure_st_data_size.crop.pdf`) | **英文，需转中文**（坐标轴: ASR-BLEU, S2TT Data Size） | 待检查 |

### 英文图片翻译清单

需要你手动将以下图片中的英文转为中文：

1. **ComSpeech.pdf**（模型架构图）：
   - "S2TT Model" → "S2TT模型"
   - "Vocabulary Adaptor" → "词表适配器"
   - "TTS Model" → "TTS模型"
   - 其他标注根据实际内容翻译

2. **ComSpeech_training.pdf**（训练与推理流程图）：
   - 各阶段标签翻译为中文

3. **comspeech_tts_data_size.pdf**（TTS数据规模影响）：
   - 坐标轴和图例翻译为中文

4. **comspeech_s2tt_data_size.pdf**（S2TT数据规模影响）：
   - 坐标轴和图例翻译为中文

---

## 第四章 LLaMA-Omni

### 表格

| 论文文件 | label | 原论文来源 | 中文化 | 布局 | 检查状态 |
|---------|-------|-----------|--------|------|---------|
| `Tables/llamaomni_data.tex` | `tab:llamaomni_data` | LLaMA-Omni论文 Table 2 (`Tables/table_data.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/llamaomni_offline.tex` | `tab:llamaomni_offline` | LLaMA-Omni论文 Table 1 (`Tables/table_offline_result.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/llamaomni_streaming.tex` | `tab:llamaomni_streaming` | LLaMA-Omni论文 Appendix Table (`Tables/table_num_llama_omni.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/llamaomni_decode_time.tex` | `tab:llamaomni_decode_time` | LLaMA-Omni论文 Table 3 (`Tables/table_decode_time.tex`) | 已完成 | 原始宽度 | 待检查 |

### 图片

| 论文文件 | label | 图片文件 | 原论文来源 | 图片语言 | 检查状态 |
|---------|-------|---------|-----------|---------|---------|
| `Img/figure_llamaomni.tex` | `fig:llamaomni` | `Img/LLaMA_Omni.pdf` | LLaMA-Omni论文 Figure 1 左 (`Figures/figure_model.tex`, `Figures/llamas2s.pdf`) | **英文，需转中文** | 待检查 |
| `Img/figure_llamaomni_training.tex` | `fig:llamaomni_training` | `Img/LLaMA_Omni_training.pdf` | LLaMA-Omni论文 Figure 1 右 (`Figures/figure_model.tex`, `Figures/llamas2s_training.pdf`) | **英文，需转中文** | 待检查 |
| `Img/figure_llamaomni_streaming.tex` (subfigure) | `fig:llamaomni_streaming` | 总图，含4个子图 | LLaMA-Omni论文 Figure 3 (`Figures/figure_streaming.tex`) | **英文，需转中文** | 待检查 |
| 　└ 子图(a) | — | `Img/llamaomni_score.pdf` | ChatGPT Score vs Latency (`Figures/score.pdf`) | **英文，需转中文**（坐标轴、图例） | 待检查 |
| 　└ 子图(b) | — | `Img/llamaomni_asr-wer.pdf` | ASR-WER vs Latency (`Figures/asr-wer.pdf`) | **英文，需转中文** | 待检查 |
| 　└ 子图(c) | — | `Img/llamaomni_mos.pdf` | UTMOS vs Latency (`Figures/mos.pdf`) | **英文，需转中文** | 待检查 |
| 　└ 子图(d) | — | `Img/llamaomni_wps.pdf` | WPS vs Latency (`Figures/wps.pdf`) | **英文，需转中文** | 待检查 |
| `Img/figure_llamaomni_humaneval.tex` (两个minipage) | `fig:llamaomni_humaneval_helpful` / `fig:llamaomni_humaneval_natural` | 2张独立图 | LLaMA-Omni论文 Figure 5 (`Figures/figure_human_eval.tex`) | **英文，需转中文** | 待检查 |
| 　└ 帮助性 | `fig:llamaomni_humaneval_helpful` | `Img/llamaomni_humaneval_helpful.pdf` | Helpfulness (`Figures/humaneval_helpful.pdf`) | **英文，需转中文** | 待检查 |
| 　└ 自然性 | `fig:llamaomni_humaneval_natural` | `Img/llamaomni_humaneval_natural.pdf` | Naturalness (`Figures/humaneval_natural.pdf`) | **英文，需转中文** | 待检查 |

### 英文图片翻译清单

需要你手动将以下图片中的英文转为中文：

1. **LLaMA_Omni.pdf**（模型架构图）：
   - "Speech Encoder" → "语音编码器"
   - "Speech Adaptor" → "语音适配器"
   - "LLM" → 可保留
   - "Speech Decoder" → "语音解码器"
   - "Vocoder" → "声码器"
   - "Discrete Units" → "离散单元"
   - "Text Response" → "文本响应"
   - "Speech Response" → "语音响应"
   - 其他标注根据实际内容翻译

2. **LLaMA_Omni_training.pdf**（两阶段训练示意图）：
   - "Stage 1" → "第一阶段"
   - "Stage 2" → "第二阶段"
   - "Frozen" → "冻结"
   - "Trainable" → "可训练"
   - 其他标注根据实际内容翻译

3. **llamaomni_score.pdf / llamaomni_asr-wer.pdf / llamaomni_mos.pdf / llamaomni_wps.pdf**（流式结果4子图）：
   - X轴 "Latency (ms)" → "延迟（毫秒）"
   - Y轴分别为 "ChatGPT Score" / "ASR-WER" / "UTMOS" / "WPS" → 可保留英文指标名
   - 图例中模型名可保留英文

4. **llamaomni_humaneval_helpful.pdf / llamaomni_humaneval_natural.pdf**（人工评估）：
   - "Win" → "胜出"
   - "Tie" → "平局"
   - "Lose" → "败北"
   - 模型名可保留英文

---

## 第五章 LLaMA-Omni 2

### 表格

| 论文文件 | label | 原论文来源 | 中文化 | 布局 | 检查状态 |
|---------|-------|-----------|--------|------|---------|
| `Tables/llamaomni2_main.tex` | `tab:llamaomni2_main` | LLaMA-Omni2论文 Table 1 (`Tables/table_main.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/llamaomni2_ablation.tex` | `tab:llamaomni2_ablation` | LLaMA-Omni2论文 Table 2 (`Tables/table_ablation.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/llamaomni2_pretrain.tex` | `tab:llamaomni2_pretrain` | LLaMA-Omni2论文 Table 3 (`Tables/table_pretrain.tex`) | 已完成 | 原始宽度 | 待检查 |
| `Tables/llamaomni2_readwrite.tex` | `tab:llamaomni2_readwrite` | LLaMA-Omni2论文 Table 4 (`Tables/table_readwrite.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/llamaomni2_data.tex` | `tab:llamaomni2_data` | LLaMA-Omni2论文 Table 5 (`Tables/table_data.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |
| `Tables/llamaomni2_latency.tex` | `tab:llamaomni2_latency` | LLaMA-Omni2论文 Appendix Table (`Tables/table_latency.tex`) | 已完成 | `\resizebox{\linewidth}` | 待检查 |

### 图片

| 论文文件 | label | 图片文件 | 原论文来源 | 图片语言 | 检查状态 |
|---------|-------|---------|-----------|---------|---------|
| `Img/figure_llamaomni2.tex` | `fig:llamaomni2` | `Img/LLaMA_Omni2.pdf` | 已替换为中期报告中文版 | 中文 | 通过 |

---

## 更新日志

- 2026-03-03：创建文件，录入第二章 DASpeech 全部图表（4表3图）
- 2026-03-04：所有图表标题改为简短风格（参照师兄论文），表格符号注释移至表格底部脚注
- 2026-03-04：DASpeech模型架构图替换为中期报告中文版
- 2026-03-04：新增3张图（批量解码加速比、图尺寸对S2TT的影响、图尺寸对DASpeech的影响），均为英文待转中文；speaker表去掉分类标签斜体
- 2026-03-04：解码速度3图拆为独立图（不再合并为subfigure）；图尺寸2图改为正确subfigure结构（子图用caption，总图用bicaption）
- 2026-03-05：录入第三章 ComSpeech 全部图表（5表4图）
- 2026-03-07：图3-1/3-2替换为中期报告中文版；删除主结果表dagger脚注；图3-2宽度调为0.9
- 2026-03-08：录入第四章 LLaMA-Omni 全部图表（4表3图组）
- 2026-03-08：录入第五章 LLaMA-Omni 2 全部图表（6表1图）
