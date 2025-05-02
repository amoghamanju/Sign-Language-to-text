# Word-Level Sign Language Recognition: I3D vs. Pose-TGCN

This repository contains code and experiments for a comparative study of two approaches to American Sign Language (ASL) recognition using the WLASL dataset:

- **I3D Model** (Appearance-based): Learns spatiotemporal features from raw RGB video frames.
- **Pose-TGCN Model** (Pose-based): Uses 2D keypoints extracted via MediaPipe to model joint motion using Graph Convolutional Networks (GCNs).

## 📌 Project Highlights

- Evaluated on the WLASL100 dataset.
- Extracted MediaPipe landmarks (hands, face, pose) for pose-based graphs.
- Compared classification performance of I3D and Pose-TGCN.
- Visualized model architecture and top-k accuracy results.

## 🧠 Models

- `I3D`: Inflated 3D ConvNet pretrained on Kinetics, fine-tuned on WLASL100.
- `Pose-TGCN`: Temporal GCN with 20 stacked graph blocks over MediaPipe landmarks.

## 📊 Results

| Model | Top-1 | Top-3 | Top-5 | Top-10 |
|-------|-------|-------|-------|--------|
| I3D   | 37.0% | 63.0% | 68.0% | 74.0%  |
| TGCN  | 58.1% | 75.6% | 81.4% | 87.9%  |
