# 🎥 YOLO Live — In-Browser Object Detection

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![TensorFlow.js](https://img.shields.io/badge/TensorFlow.js-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

A **single-file, fully client-side** real-time object detection demo. It runs
**YOLOv5s via ONNX Runtime Web** directly in the browser and automatically falls
back to **TensorFlow.js COCO-SSD** if no ONNX model is provided — no server, no
build step, no install. Everything (inference included) happens on-device.

## ✨ Features

- 🎥 **Live webcam detection** with bounding boxes and labels drawn on a canvas
- 🖼️ **Image-upload detection** for still images
- 🔁 **Automatic model fallback** — tries `./models/yolov5s.onnx` (ONNX Runtime
  Web), falls back to TF.js COCO-SSD if absent
- 🎚️ **Confidence threshold** control and live detection count
- 📸 **Screenshot** capture of the annotated frame
- 📱 **Multi-camera aware** — pick front/back camera (handy on mobile)

## 🚀 Run it

Because browsers only grant camera access over `http(s)` (not `file://`), serve
the folder with any static server:

```bash
# Python
python -m http.server 8000
# then open http://localhost:8000

# or Node
npx serve .
```

Allow camera access, choose a device, and click **Start**. To use YOLO instead
of the COCO-SSD fallback, drop a `yolov5s.onnx` file into a `models/` folder next
to `index.html`.

## 🧠 How it works

| Stage | Detail |
| ----- | ------ |
| Capture | Webcam frame or uploaded image drawn to a canvas |
| Preprocess | Letterbox resize to 640×640, normalised tensor |
| Inference | ONNX Runtime Web (`ort.min.js`) running YOLOv5s, or TF.js COCO-SSD |
| Postprocess | Confidence filtering + box scaling back to display size |
| Render | Boxes, class labels, and detection count overlaid live |

## 🧰 Tech stack

Vanilla JavaScript · HTML5 Canvas · ONNX Runtime Web · TensorFlow.js (COCO-SSD) ·
WebRTC `getUserMedia`

## 📄 File

Everything lives in a single self-contained [`index.html`](index.html).
