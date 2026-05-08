# Weapon Detection System using YOLOv8

## Overview
This project is a **weapon detection system** built using Deep Learning and Computer Vision. It detects **guns in images** using the YOLOv8 object detection model. The system is trained on a custom dataset named **weapon-detection-test**.

---

## Dataset
- Dataset Name: weapon-detection-test  
- Type: Labeled images dataset for weapon detection  
- Source: Kaggle-based dataset  

---

## Model Used
- YOLOv8
- Pre-trained weights fine-tuned on custom dataset
- Trained for **50 epochs**

---

## Training Details
- Epochs: 50  
- Task: Object Detection (Gun detection only)  
- Input: Images  
- Output: Bounding box around detected gun  

---

## Features
- Detects guns in images  
- High-speed inference using YOLOv8  
- Lightweight and efficient model  
- Can be extended for real-time detection  

---

## Model Files
- Trained YOLOv8 weights are used for prediction  
- Model stored externally due to size limits  

Download Model:
https://drive.google.com/file/d/1wJDPS5R7bhfx5uJORJ4ZPk4JG1VbvLGG/view?usp=sharing  

---

## How It Works
1. Input image is given to the model  
2. YOLOv8 processes the image  
3. Model detects presence of gun  
4. Output shows bounding box if weapon is found  

---

## Limitations
- Currently detects only guns (not other weapons)  
- Works only on images (not real-time video yet)  
- Performance depends on dataset quality  
- May fail on unseen environments or angles  

---

## Future Improvements
- Add real-time video detection  
- Extend to multiple weapon classes (knife, pistol, etc.)  
- Improve dataset diversity  
- Deploy as web or mobile application  
- Optimize for edge devices (CCTV systems)  

---

## How to Use

```python
from ultralytics import YOLO
import cv2

# Load trained model
model = YOLO("weapon_detector.pt")

# Load image
image_path = "test.jpg"
img = cv2.imread(image_path)

# Run detection
results = model(image_path)

# Show results
results[0].show()

# Optional: save output image
results[0].save("output.jpg")

---

## Conclusion
This project demonstrates a YOLOv8-based weapon detection system trained for 50 epochs. It provides a basic foundation for security-based AI applications and can be further improved for real-world deployment.
