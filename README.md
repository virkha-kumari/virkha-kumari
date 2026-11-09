# Hi, I'm Virkha 👋

**Lead ML Engineer (Computer Vision)** at Retrocausal AI, working remotely from Karachi, Pakistan.

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
- k-shot sweep on Construction-PPE (12 classes, 200 test images): **Pipeline B reaches the highest mAP@.50 (0.610) and recall (0.791) with 10 exemplars, but at low precision (0.356, F1 0.491) and 121 min per 200 images.** Pipeline A peaks at mAP@.50 = 0.542 with precision 0.656, F1 0.655 and 63 min, so it is the better choice when false positives are costly.
- Documented design history and negative results (OWLv2, SAM2/SAM3 auto-mask as proposers, averaged prototypes, full-crop CLS), with the reason each was dropped
- Evaluation harness: per-class P/R/F1, AP@.50, mAP@.50:.95. Full ablation and per-class tables in [docs/ablation.md](https://github.com/virkha-kumari/Auto_Annotation_YOLO_formatted/blob/main/docs/ablation.md)

### [Dataset Quality EDA](https://github.com/virkha-kumari/EDA_intra_class_variation)

Checks dataset quality before annotation, before training, and after training: diversity, outliers, intra-class variation, plus a detector-free check for likely missed labels on fixed-camera data.

- Embedding benchmark on an industrial frame set: DINOv2 `[CLS ‖ patch-mean]` separated activities better than SigLIP (pair AUC 0.948 vs 0.917) and left fewer frames unclustered (39% vs 52%)
- Per-class DBSCAN with data-driven eps from the k-distance curve knee; auto insights page covering outlier rate, cluster count and systematic noise
- USB missed-label flagging: reuses ground-truth box geometry as region proposals on fixed-camera data — no detector needed

### [YOLO Frame Review](https://github.com/virkha-kumari/YOLO-Frame-Review-Extract)

Pick training frames from hours-long videos, side by side with YOLO model output.

- Smooth on hours-long video: forward-grab instead of seeking, slider scrub on a background thread, stale frames dropped via generation counter
- Twin view pairs original and YOLO-rendered video frame-for-frame; saving always writes the clean original
- Smart Skip jumps to the next visually different frame; session tracking marks progress across videos
- Attach a whole YOLO folder and auto-pair by filename and frame count/FPS validation

### [Python Code Flow Graph Maker](https://github.com/virkha-kumari/python_codeflow_graph_maker)

Static analysis tool that parses Python codebases via AST to generate import and I/O dependency graphs with interactive visualisations.

---

## 🎓 University and learning projects

Earlier work from my undergraduate years and self-study. Kept public as a record of what I built along the way, not as current work.

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
