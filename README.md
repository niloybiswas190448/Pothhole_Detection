
# 🕳️ Pothole Detection & Segmentation using YOLOv11

<p align="center">
  <img src="demo.gif" alt="Pothole Detection Demo" width="70%">
</p>

## 🚀 One-Click Google Colab Demo

Run it in your browser (no setup needed):

- 📦 **YOLOv11 Detection + Segmentation Demo**  
  [Open in Google Colab](https://drive.google.com/file/d/18ZBRoLTUkpUXaOeeCplrQ0QxKVkFceH8/view?usp=sharing)

---

## 📂 Project Repository

[GitHub Repo - Pothole Detection](https://github.com/niloybiswas190448/Pothhole_Detection.git)

---

## 🔍 Overview

This project presents an automated solution for pothole detection and **segmentation** using the YOLOv11 architecture. It enables both **bounding box detection** and **pixel-level mask generation**, ensuring high accuracy and efficiency.

---

## 💡 Key Features

- 🛣️ Real-time pothole detection and shape segmentation  
- 🎯 Dual-output (bounding boxes + masks)  
- ⚡ 45 FPS inference on Tesla T4  
- 🧠 Built on YOLOv11 + custom segmentation head  
- 🗂️ Dataset of 700+ annotated road images  
- 📈 87.4% mAP@50 on validation set

---

## 📊 Model Performance

| Metric        | Bounding Box | Segmentation Mask |
|---------------|--------------|-------------------|
| Precision     | 0.882        | 0.874             |
| Recall        | 0.769        | 0.766             |
| mAP@50        | 0.875        | 0.870             |
| mAP@50–95     | 0.582        | 0.555             |

---

## 🧠 Model Architecture

- **Backbone**: YOLOv11 backbone (CSPDarknet with improved attention layers)  
- **Head**: Dual-head structure with detection and segmentation layers  
- **Loss Function**: Combination of Binary Cross-Entropy, Dice Loss, and IoU Loss

---

## 📸 Sample Output Results

### ▶️ Detection & Segmentation Example

<p align="center">
  <img src="result_detection.jpg" width="45%" alt="Detection Output">
  <img src="result_mask.jpg" width="45%" alt="Segmentation Mask">
</p>

---

## 🧰 Run Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/niloybiswas190448/Pothhole_Detection.git
cd pothole-detection
````

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run Inference

```python
from ultralytics import YOLO
model = YOLO("best.pt")
results = model("road.jpg", save=True)
```

---

## 🧪 Evaluation Approach

* Stratified 80/20 train-validation split
* Evaluated with COCO metrics using `pycocotools`
* Visual validation with mask overlay on original images

---

## 🖼️ Dataset Summary

* 📍 Source: Annotated via Roboflow
* 🖼️ Total Images: 700+
* 🔀 Split: 80% training / 20% validation
* 🎨 Augmentations: CLAHE, Blur, Rotation, Brightness/Contrast

<p align="center">
  <img src="dataset_samples.png" alt="Dataset Preview" width="70%">
</p>

---

## ⚙️ Inference Settings

* 🔍 Input Image Size: 640×640
* ⏱️ Speed: \~45 FPS on Tesla T4
* 🧠 Batch Size: 16
* 📦 Inference Time: \~0.022s per image

---

## 🔗 Applications

* 🛠️ Smart city road condition monitoring
* 🚗 Autonomous vehicle systems
* 🛣️ Municipal road inspection tools
* 📱 Mobile pothole reporting apps (future integration)

---

## 🔮 Future Work / Roadmap

* [ ] 🔄 Real-time video stream inference
* [ ] 🌍 Deploy as web app with Streamlit
* [ ] 📱 Build Android app with TFLite
* [ ] 🔁 Integrate temporal smoothing in video
* [ ] 📈 Add more datasets from different regions



## 📬 Contact

**Niloy Biswas**
Urban Planner | Deep Learning Enthusiast | Transportation Researcher

📧 Email: [niloyurp48@gmail.com](mailto:niloyurp48@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/niloy-biswas-92003b1b3)
📚 [ResearchGate](https://www.researchgate.net/profile/Niloy-Biswas-2?ev=hdr_xprf)

> *Empowering smart cities with intelligent road monitoring systems.*


