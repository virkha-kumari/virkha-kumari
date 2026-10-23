# Hi, I'm Virkha 👋

**Lead Research Engineer (Computer Vision & ML)** at a Retrocausal AI, working remotely from Karachi, Pakistan. 

I work on **video understanding and industrial computer vision**: making models work on real, messy production data, and figuring out *why* they fail.

---

## 🔬 What I work on

- **Temporal action detection**: real-time action detection for industrial assembly lines
- **Visual representations**: DINOv2 / SigLIP encoder ablations for scene- and object-level features
- **Data-centric CV**: dataset quality pipelines with self-supervised embeddings, PaCMAP, and HDBSCAN
- **Video models**: VLMs fine-tuning
- **Detection & deployment**: YOLO-based detection, edge deployment

---

## 📌 Selected projects

### [Few-Shot Auto-Annotation](https://github.com/virkha-kumari/Auto_Annotation_YOLO_formatted)
Label 10–15 instances per class, auto-annotate the rest. No text prompts, fully local on an 8GB GPU.
- **Pipeline A:** YOLOe visual-prompt proposals → SAM2 masks → DINOv2 masked-patch similarity → WBF
- **Pipeline B:** SAM3 cross-image few-shot via canvas-composite exemplars → DINOv2 gate
- Documented ablations: why SAM2/SAM3 auto-mask and OWLv2 failed as proposal generators, why masked-patch pooling beats CLS on crops, why a per-crop prototype bank beats an averaged prototype
- Per-class P/R/F1/AP evaluation with failure analysis, plus a hypothesis on why visual-prompt detection trails supervised YOLO (classification head, not backbone)

### [Dataset Quality EDA](https://github.com/virkha-kumari/EDA_intra_class_variation)
Checks dataset quality before annotation, before training, and after training: diversity, outliers, intra-class variation. Benchmarked embedding choices, including why DINOv2 `[CLS || avg_patches]` outperformed SigLIP pooled features for scene-level separation.

### [Python Code Flow Graph Maker](https://github.com/virkha-kumari/python_codeflow_graph_maker)
Static analysis tool that builds dependency graphs for Python codebases via AST parsing, with I/O tracking and interactive visualizations.

---

## 🎯 Research interests

Video understanding · Few-shot & self-supervised visual representations · Data-centric ML · Efficient / edge vision

---

## 🛠️ Stack

`PyTorch` · `Hugging Face Transformers` · `Ultralytics YOLO` · `DINOv2` · `SigLIP` · `SAM2 / SAM3` · `VideoMAE` · `HDBSCAN` · `PaCMAP` · `Gradio`

---

## 🎓 Education

**BS Computer Science**, FAST-NUCES · Magna Cum Laude

---

📫 virkhakumarimulani@gmail.com
