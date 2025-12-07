
# **Web-Based Object Detection Using COCO Dataset**

This repository contains a web-based real-time object detection application powered by pre-trained COCO dataset models. The system is capable of detecting 80+ common everyday objects directly in the browser using client-side machine learning—no backend server or API required.

---

## **📌 Features**

* 🔹 Real-time object detection in browser
* 🔹 Uses pre-trained COCO models
* 🔹 No installation or backend server
* 🔹 Supports webcam and uploaded images
* 🔹 Bounding boxes, labels, and confidence scores
* 🔹 Lightweight, fast, and easy to deploy

---

## **🧠 Model Used**

This project uses **TensorFlow.js COCO-SSD** (Single Shot Multibox Detector) trained on the **COCO dataset**, which includes more than 80 object categories such as:
➡ Person, Car, Dog, Cat, Chair, Bottle, Bus, Laptop, etc.

---

## **🚀 How It Works**

1. Load TensorFlow.js COCO-SSD model in browser
2. Capture image frames using webcam or file input
3. Run detection on each frame
4. Draw bounding boxes and labels on canvas

---

## **📁 Project Structure**

```
├── index.html
├── script.js
├── style.css
└── assets/
```

---

## **▶ How to Run**

Simply open the **index.html** file in a browser:

📍 Drag and drop into Chrome/Edge
📍 OR use VS Code Live Server

No Python, no installation — just run and detect.

---

## **🌐 Live Demo (If you deploy)**

https://objectdetection-eight.vercel.app/
---

## **🛠 Technologies Used**

| Technology    | Purpose                |
| ------------- | ---------------------- |
| HTML/CSS      | UI/Layout              |
| JavaScript    | Logic & UI Control     |
| TensorFlow.js | ML Model               |
| COCO-SSD      | Object Detection Model |

---

## **📦 Future Enhancements**

* [ ] Add support for custom trained YOLO models
* [ ] Draw detection history and analytics
* [ ] Add voice alerts for detected objects
* [ ] Export detection results to file

---
