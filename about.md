## 🧠 How It Works

This project uses **OWL-ViT (Open-World Vision Transformer)**, a zero-shot object detection model from Google, to detect objects in real time using a webcam. Unlike traditional models trained on fixed classes (like COCO), OWL-ViT takes **free-text prompts** (e.g., *"a black pen"*, *"a pair of headphones"*) and detects matching objects in the video stream. 

The model processes every Nth frame to balance speed and accuracy. It draws **bounding boxes** and **confidence scores** for each detected object and **logs predictions to a CSV file**. The system also allows **live editing of detection labels during runtime**, making it dynamic and adaptable.

---

## 🚧 Challenges

Some challenges included **low frame rates during live inference** due to the heavy model and high processing load, especially on CPU-only setups. Implementing real-time detection while ensuring smooth display and responsiveness required optimization techniques like **frame skipping**.

Another issue was that OWL-ViT may **struggle with objects that are not visually distinctive** or when the **prompt isn't specific enough**, reducing detection accuracy.

---

## 🔧 What Could Be Improved or Added Next

Future enhancements could include:

- **ONNX or TorchScript acceleration** to significantly boost frame processing speed.
- **Video file input support**, in addition to webcam, for offline detection tasks.
- A **graphical UI** for easier live editing of detection labels instead of console input.
- **Voice commands** to add or change prompts dynamically for hands-free operation.
- A **tracking module** to persist object identities across frames, improving the continuity of detection.
- Integration with a lightweight **dashboard or analytics tool** to visualize detection stats over time.
