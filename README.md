# DEAR: Dual-Stream Entity Alignment for 3D Radiology Report Generation

**📌 This repository will be made publicly available upon the acceptance of our paper at AAAI 2026.**

## 📄 Paper Title
**Mitigating Entity Hallucinations in 3D Radiology Report Generation via Dual-Stream Alignment**  
*Accepted to AAAI 2026 (Camera Ready)*

## 🧠 Abstract
Entity hallucination poses a major challenge in radiology report generation (RRG), particularly for 3D CT scans where complex spatial contexts amplify factual errors.  
To address this, medical entity phrases serve as key carriers for multi-modal prompting, integrating expert knowledge into the vision-language model.  
Current methods use unified cross-attention for volume–phrase alignment, failing to account for anatomical specificity during the alignment process.

In this work, we introduce the **Dual-stream Entity Alignment Reporting network (DEAR)** that separately models organ and lesion entities to resolve anatomical bias. Specifically, the dual-stream entity aligner partitions medical entity phrases into organ and lesion streams, feeding them into separate cross-attention blocks to achieve fine-grained volume–phrase alignment.

- For structurally regular and spatially stable **organ** entities, we propose **Organ-Guided Cross-Attention (OGCA)** to enforce structural consistency by retrieving top-*k* voxel tokens via similarity and preserving spatial connectivity through morphological dilation.
- For structurally irregular and spatially variable **lesion** entities, we introduce **Lesion-Guided Cross-Attention (LGCA)** to enhance anomaly sensitivity via phrase-weighted attention and refine lesion boundaries using 3D residual Laplacian filtering.

🧪 Experimental results demonstrate that DEAR significantly reduces entity hallucinations and improves clinical factuality on 3D RRG benchmarks.

## 📢 Notice
The source code and pretrained models will be released after official acceptance by **AAAI 2026**.

Stay tuned!

---

📫 For inquiries, please contact: `scu_zly@stu.scu.edu.cn`
