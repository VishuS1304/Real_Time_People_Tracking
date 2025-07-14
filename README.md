# 🧠 People Tracking in ROI using YOLOv11 + DeepSORT

A real-time and offline surveillance system to detect, track, and analyze people movements inside a specified Region of Interest (ROI) using **YOLOv8** and **DeepSORT**.

## 🎯 Key Features

- ✅ **YOLOv11 Person Detection** (`best3.pt`)
- ✅ **DeepSORT Multi-Person Tracking**
- ✅ **ROI-based Filtering with Polygon Mask**
- ✅ **Entry/Exit Line Crossing Detection**
- ✅ **Real-Time Stats Overlays**
- ✅ **CSV Logging of ID, Time, Duration**
- ✅ **Video Output with Annotations**
- ⚡ **Optimized using FP16 + Frame Skipping**

## 📁 Project Structure

```bash
people-tracking-yolov8/
├── yolov11_roi_tracker.py       # Main tracking script
├── best3.pt                    # YOLOv8 trained model weights
├── saved_chunks/               # Video input directory (RTSP or offline)
├── logs/                       # Output logs in CSV format
├── output_with_direction.mp4   # Final video with overlays
├── requirements.txt
├── LICENSE
└── README.md


---

## 📥 Installation

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/people-tracking-yolov8.git
cd people-tracking-yolov8

## Install dependencies
pip install -r requirements.txt


