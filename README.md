# Hi, I'm Virkha 👋

**Lead Research Engineer (Computer Vision & ML)** at Retrocausal AI, working remotely from Karachi, Pakistan.

I work on **video understanding and industrial computer vision**: making models work on real, messy production data, and figuring out *why* they fail.

---

## 🔬 What I work on

- **Temporal action detection**: real-time action detection for industrial assembly lines
- **Visual representations**: DINOv2 / SigLIP encoder ablations for scene- and object-level features
- **Data-centric CV**: dataset quality pipelines with self-supervised embeddings, PaCMAP, and HDBSCAN
- **Video models**: Video transformer fine-tuning (VideoMAE, InternVL)
- **Detection & deployment**: YOLO-based detection, edge deployment

---

## 📌 Selected projects

### [Few-Shot Auto-Annotation](https://github.com/virkha-kumari/Auto_Annotation_YOLO_formatted)
Label a few instances per class, auto-annotate the rest. No text prompts, no training, runs on an 8 GB GPU.
- **Pipeline A:** YOLOe visual-prompt proposals → SAM2 masks → DINOv2 masked-patch similarity → WBF
- **Pipeline B:** SAM3 cross-image few-shot via canvas-composite exemplars → DINOv2 gate → voting across exemplars
- Documented design history and negative results (OWLv2, SAM2/SAM3 auto-mask as proposers, averaged prototypes, full-crop CLS), with the reason each was dropped
- Evaluation harness on the public Construction-PPE dataset (fixed 150-image test split): per-class P/R/F1, AP@.50, mAP@.50:.95
- **Status:** the k-shot sweep (both pipelines, k = 15 to 100) is the next run, so the README results section is still pending. Numbers will be added once the runs finish.

### [Dataset Quality EDA](https://github.com/virkha-kumari/EDA_intra_class_variation)
Checks dataset quality before annotation, before training, and after training: diversity, outliers, intra-class variation, plus a detector-free check for likely missed labels on fixed-camera data.
- Embedding benchmark on a non-public industrial frame set: DINOv2 `[CLS ‖ patch-mean]` separated activities better than SigLIP pooled features (pair AUC 0.948 vs 0.917) and left fewer frames unclustered (39% vs 52%). The activity test is small (23 frames), so treat this as indicative, not conclusive.
- The missed-label check is not yet evaluated; a label-dropout test is planned.

---

## 🎓 University and learning projects

Earlier work from my undergraduate years and self-study. Kept public as a record of what I built along the way, not as current work.

- [Python Code Flow Graph Maker](https://github.com/virkha-kumari/python_codeflow_graph_maker): AST-based import and I/O dependency graphs
- [Explainable Recommender (KG + PGPR)](https://github.com/virkha-kumari/Explainable_RS_using_KG_and_PGPR): knowledge-graph recommender on MovieLens-1M
- [Image Embeddings From Scratch](https://github.com/virkha-kumari/Image-Embeddings-From-Scratch): Siamese network with contrastive loss
- [Speaker Diarization and Audio Transcription](https://github.com/virkha-kumari/Speaker-Diarization-and-Identification-Audio-Transcription)
- [Undergraduate coursework](https://github.com/virkha-kumari/personal-projects) and [data science internship tasks](https://github.com/virkha-kumari/OIB-SIP)

---

## 🎯 Research interests

Video understanding · Few-shot & self-supervised visual representations · Data-centric ML · Efficient / edge vision

---

## 🛠️ Stack

`PyTorch` · `Hugging Face Transformers` · `Ultralytics YOLO` · `DINOv2` · `SigLIP` · `SAM2 / SAM3` · `VideoMAE` · `HDBSCAN` · `PaCMAP` · `Gradio`

---

## 🎓 Education

**BS Computer Science**, FAST-NUCES · Magna Cum Laude
