# GStreamer Live Streaming with YOLOv5 Integration

This project implements a real-time video streaming system using **GStreamer** for video capture and network streaming, paired with a **FastAPI-based REST API** for remote control. It simulates a media streaming service, allowing efficient, low-latency video transmission and external management through HTTP requests.

The core pipeline uses the **x264 encoder** for H.264 compression with zero-latency tuning. If x264 is unavailable, the system falls back to **vp8enc**. Captured video from a webcam is streamed via **UDP** to `localhost`. Two API endpoints—`/start` and `/stop`—let users initiate or stop streaming remotely.

A Python-based client application receives the stream, displaying it using **OpenCV** and offering GUI-based playback control through **Tkinter**. This makes the setup suitable for testing, demos, or internal streaming solutions.

## YOLOv5 Object Detection (Client-Side)

The client application now includes **YOLOv5 object detection** powered by **PyTorch**. It loads the `yolov5s` model from Ultralytics via `torch.hub` and detects only **persons** (`class 0`). Detection can be toggled on/off through the GUI. When active, each frame is processed in real-time, and detected persons are highlighted with bounding boxes and confidence scores.

This feature demonstrates how object detection can be seamlessly added to live video feeds, enhancing the system with intelligent analytics capability.

---

## Features

- Real-time video streaming via GStreamer
- FastAPI REST control (`/start`, `/stop`)
- x264 / vp8 encoding fallback mechanism
- Local GUI-based stream viewer (Tkinter + OpenCV)
- Optional person detection using YOLOv5

---

## Usage

### Requirements

```bash
pip install opencv-python-headless torch torchvision pillow fastapi uvicorn
# GStreamer Live Streaming with YOLOv5 Integration

This project implements a real-time video streaming system using **GStreamer** for video capture and network streaming, paired with a **FastAPI-based REST API** for remote control. It simulates a media streaming service, allowing efficient, low-latency video transmission and external management through HTTP requests.

The core pipeline uses the **x264 encoder** for H.264 compression with zero-latency tuning. If x264 is unavailable, the system falls back to **vp8enc**. Captured video from a webcam is streamed via **UDP** to `localhost`. Two API endpoints—`/start` and `/stop`—let users initiate or stop streaming remotely.

A Python-based client application receives the stream, displaying it using **OpenCV** and offering GUI-based playback control through **Tkinter**. This makes the setup suitable for testing, demos, or internal streaming solutions.

## YOLOv5 Object Detection (Client-Side)

The client application now includes **YOLOv5 object detection** powered by **PyTorch**. It loads the `yolov5s` model from Ultralytics via `torch.hub` and detects only **persons** (`class 0`). Detection can be toggled on/off through the GUI. When active, each frame is processed in real-time, and detected persons are highlighted with bounding boxes and confidence scores.

This feature demonstrates how object detection can be seamlessly added to live video feeds, enhancing the system with intelligent analytics capability.

---

## Features

- Real-time video streaming via GStreamer
- FastAPI REST control (`/start`, `/stop`)
- x264 / vp8 encoding fallback mechanism
- Local GUI-based stream viewer (Tkinter + OpenCV)
- Optional person detection using YOLOv5

---

## Usage

### Requirements

```bash
pip install opencv-python-headless torch torchvision pillow fastapi uvicorn
