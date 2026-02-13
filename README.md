# Urban Scene Segmentation with SegFormer – Transfer Learning & Explainable AI

## Overview

This repository contains the implementation used in the research paper:

**“Evaluating Architecture Scalability and Transfer Learning in Urban Scene Segmentation Using Explainable AI.”**

The project investigates how different **SegFormer variants (B3, B4, B5)** scale on smaller datasets and how well they transfer to geographically different driving environments using transfer learning.

The notebook implements:

* Transformer-based semantic segmentation
* Cross-dataset transfer learning
* Evaluation using mIoU and class-level metrics
* Explainable AI through confidence heatmaps

---

## Paper Reference

**Authors:** Tanmay Sunil Hatkar, Abhinv Pandey, Saad B. Ahmed
**Affiliation:** Department of Computer Science, Lakehead University, Thunder Bay, Canada

**Abstract Summary**

* Evaluates SegFormer scalability on CamVid.
* Transfers learned weights to KITTI and IDD datasets.
* SegFormer-B5 achieved **82.4% mIoU on CamVid**.
* Transfer learning improved KITTI performance by **+2.57% mIoU**.
* Confidence heatmaps provide visual interpretability.

---

## Model Architecture

The project uses the **SegFormer transformer architecture**, which includes:

* Hierarchical encoder
* Lightweight decoder
* No positional embeddings
* Efficient global context modeling

Variants tested:

* SegFormer-B3
* SegFormer-B4
* SegFormer-B5

---

## Datasets

Base Dataset:

* CamVid

Transfer Learning Targets:

* KITTI (structured driving environment)
* IDD (unstructured urban environment)

---

## Features

✔ Transformer-based semantic segmentation
✔ Cross-dataset transfer learning pipeline
✔ Class-wise performance evaluation
✔ Explainable AI visualization using confidence maps
✔ Scalable architecture comparison

---

## Installation

Clone the repository.
Install dependencies.

---

## Usage

Run the main notebook:

```bash
SegFormer_B3_KITTI.ipynb
```

Typical workflow:

1. Load dataset
2. Initialize SegFormer variant
3. Train on CamVid
4. Transfer weights to KITTI / IDD
5. Evaluate and visualize predictions

---

## 📊 Results

| Model             | Dataset | mIoU               |
| ----------------- | ------- | ------------------ |
| SegFormer-B5      | CamVid  | 82.4%              |
| Transfer Learning | KITTI   | +2.57% improvement |

---

## 🖼️ Adding Output Images (Predictions / Heatmaps)

Create a folder in your repo such as:

```
/results
/assets
/images
```

Example structure:

```
repo/
 ├── SegFormer_B3_KITTI.ipynb
 ├── README.md
 └── results/
      ├── prediction_example.png
      ├── confidence_heatmap.png
```

Then display them inside this README using markdown:

```md
## Example Predictions
![Prediction](results/prediction_example.png)

## Confidence Heatmap
![Heatmap](results/confidence_heatmap.png)
```

You can rename the folder anything — just update the image path.

---

## Explainable AI

The notebook generates **confidence heatmaps** that visualize model certainty at pixel level, helping interpret segmentation predictions in real-world scenarios.

---

## Citation

If you use this work, please cite:

```
Hatkar, T.S., Pandey, A., Ahmed, S.B.
Evaluating Architecture Scalability and Transfer Learning in
Urban Scene Segmentation Using Explainable AI.
Lakehead University.
```

---

## 👨‍💻 Authors

* Tanmay Sunil Hatkar
* Abhinv Pandey
* Saad B. Ahmed

---

## Acknowledgements

This work explores practical deployment of transformer-based segmentation models for autonomous driving and interpretable AI research.
