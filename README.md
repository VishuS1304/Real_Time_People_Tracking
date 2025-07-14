# 🔧 YOLOv11 Person Training Pipeline

End‑to‑end pipeline for custom person detection using Roboflow and Ultralytics YOLOv8.

## 🚀 Features

- 🔄 Download dataset from Roboflow via API  
- 📐 Custom `data.yaml` config (1 class: Person)  
- 🏋️‍♂️ Train on `yolov11n.pt` (nano model) or switch to `yolov11s/m.pt` for higher accuracy  
- ⚙️ Extensive augmentation: Mosaic, MixUp, HSV, rotation, scale, translate, shear  
- ⏱️ Early stopping, cosine LR scheduler, warmup epochs  
- 🧪 Quick inference script to test on images or video frames  

## 📁 Project Structure

```bash
people-tracking-yolov8/
├── train_person_yolov11.py     # Download + train script
├── yolov11_roi_tracker.py      # Main tracking script
├── data.yaml                   # Roboflow dataset config
├── best3.pt                    # YOLOv8 trained model weights
├── requirements.txt
├── .gitignore                  # ignore weights, caches, logs
├── LICENSE
└── README.md


---

## 📥 Installation

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/people-tracking-yolov11.git
cd people-tracking-yolov11

## Install dependencies
pip install -r requirements.txt

## 📄 Configuration (data.yaml)
yaml
Copy
Edit
names:
  - Persona
nc: 1
train: ../train/images
val: ../valid/images
test: ../test/images


## Parameters & Customization
ROI polygon: Edit roi_points in script

Entry/exit lines: Adjust entry_line, exit_line coords

Frame skipping: frame_skip = 2 (change to 1 for full processing)

Confidence: conf=0.3 in model.predict()

## 2. `people-tracking-yolov11/README.md`

```markdown
# 🧠 People Tracking in ROI using YOLOv11 + DeepSORT

Detect, track, and analyze people's movement within a Region of Interest (ROI) in video chunks.

## 🎯 Key Features

- 🔍 YOLOv11 (`best3.pt`) for person detection (FP16 + fused model for speed)  
- 🧠 DeepSORT for persistent multi-object tracking  
- 📐 Polygonal ROI filtering (overlap threshold)  
- ↔️ Entry & Exit line crossing detection via vector cross‐product  
- 🧾 CSV logging: ID, timestamps, duration, coords  
- ⚡️ Frame‐skipping & MJPG codec for faster processing  
- 📹 Annotated video output (`output_with_direction.mp4`)
