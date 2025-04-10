# Vyorius-Test

# 🦉 Real-Time Object Detection with OWL-ViT

This project demonstrates real-time **zero-shot object detection** using [Google's OWL-ViT model](https://huggingface.co/google/owlvit-base-patch32), webcam feed, and custom user-defined labels. 

It supports live label editing, frame-skipping optimization, and logs all detections with bounding box coordinates and confidence to a CSV file.

---

## 🔑 Features

This project implements **zero-shot object detection** using OWL-ViT in Python. Below are the core features:

### 🎥 1. Flexible Video Input
- Accepts input **from a webcam** (real-time) or **a local video file**.
- Uses **OpenCV** for video frame capture and display.

### 🧠 2. Zero-Shot Object Detection with Custom Prompts
- Accepts a list of **custom object categories** (e.g., `"a screwdriver"`, `"a bottle of sanitizer"`).
- Uses **pre-trained OWL-ViT (or CLIP-based)** model to detect those objects **without training**.

### 📦 3. Non-COCO Categories Only
- Ensures that **none of the detected objects** belong to the standard COCO dataset categories.
- Targets **custom/niche items** to showcase the power of **zero-shot detection**.

### 📏 4. Annotated Output
- Displays each frame with:
  - ✅ **Bounding boxes**
  - ✅ **Class labels**
  - ✅ **Confidence scores**
- Optionally logs detections to a `.csv` file with bounding box and confidence details.

### 🧹 5. Clean, Modular Codebase
- Fully implemented in **Python**
- Modular structure with:
  - **Model loading**
  - **Video processing**
  - **Detection pipeline**
  - **Prompt updating**
  - **CSV logging**
- Includes **in-line comments** for clarity and future extension.

### 💡 6. Real-Time Live Edits
- Press **`e`** during runtime to **edit labels dynamically** (bonus feature).
- Frame-skipping enabled for better FPS performance on lower-end machines.

### 🖥️ 7. Live Display or Console Mode
- Visual results shown in a **live OpenCV window**.
- Can be easily modified to print predictions in **console mode** if desired.

---


## ✨ Bonus Features Implemented

This project goes beyond basic detection! Here's what we added:

### ✅ 1. **Live Label Prompt Editing**
- Press **`e`** during runtime to **change the object labels on the fly.**
- No need to stop or restart the notebook.
- Useful for experimenting with different prompts dynamically.

### ✅ 2. **Frame Skipping for FPS Optimization**
- Performs detection **every N frames** (default: every 5th frame) to improve speed.
- Intermediate frames reuse previous detections to reduce computation.

### ✅ 3. **CSV Logging of Detected Objects**
- Every detection is **logged to `detection_log.csv`** with:
  - Timestamp
  - Label
  - Confidence score
  - Bounding box coordinates (`x1, y1, x2, y2`)
- Great for training logs, data analysis, or auditing predictions.

### ✅ 4. **On-Screen Visual Feedback**
- Bounding boxes and labels drawn in real-time on the webcam feed.
- Display updated labels and detection confidence.

---


# 🛠️ Setup Instructions

This project uses OWL-ViT for zero-shot object detection on custom object categories **not in the COCO dataset**, using real-time webcam input. The implementation is done entirely in a single Jupyter Notebook.

---

## 📁 I. Clone or Download the Project

You can either clone the repository:

```bash
git clone https://github.com/yourusername/owlvit-custom-detection.git
cd owlvit-custom-detection
```
Or simply download the notebook file OWLViT_Custom_Detection.ipynb and open it in your preferred Jupyter environment (Jupyter Notebook, JupyterLab, or Google Colab).


## ▶️ II. Run the Notebook
Launch Jupyter and run the notebook:

```bash
jupyter notebook OWLViT_Custom_Detection.ipynb
```
🖥️ The webcam will open automatically when you run the notebook.
🔁 Press e to edit detection labels live.
❌ Press q to quit the webcam stream.
