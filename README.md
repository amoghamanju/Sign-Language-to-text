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

## 🔧 Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/sign-language-recognition-I3D-TGCN.git
   cd sign-language-recognition-I3D-TGCN
2. Install requirements:
pip install -r requirements.txt

3.Download the WLASL dataset and place it in the data/ directory.

4. For Pose-TGCN:
-  Run extract_pose.py to generate features using MediaPipe.
- Train or test with train_tgcn.py or test_tgcn.py.

5. For I3D:
 - Use train_i3d.py or test_i3d.py on RGB video data.

🧾 Citation
@inproceedings{li2020word,
  title={Word-Level Deep Sign Language Recognition from Video: A New Large-Scale Dataset and Methods Comparison},
  author={Li, Dongxu and Rodriguez, Cristian and Yu, Xin and Li, Hongdong},
  booktitle={WACV},
  year={2020}
}
