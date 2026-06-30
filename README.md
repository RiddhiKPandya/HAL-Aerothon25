# 🚁 Team SkyLens  
## EO/IR Sensor Video Image Classification & Identification System  
### HAL Aerothon ’25  

An aerial surveillance system for detecting, classifying, and estimating drone-to-object distance and height using EO (RGB) and IR (Thermal) video input.

Built using YOLOv8 and trained on VisDrone + a custom aerial dataset with 35+ object classes.

---

## Watch demo here


---

## ✨ Features

- YOLOv8 model optimized for aerial top-down detection
- 35+ custom object classes:
  - Vehicles
  - People
  - Terrains
  - Structures
  - Incidences
- Drone-to-object distance estimation
- Drone-to-object height estimation
- RGB (EO) and Thermal (IR) support
- Post-mission processed output storage

---

## 📂 Project Structure

```
Team-SkyLens/
│
├── backend/
│   ├── processed/              # Processed output videos
│   ├── runs/                   # YOLO training runs
│   ├── uploads/                # Uploaded input videos
│   ├── app.py                  # Backend server (Flask/FastAPI)
│   ├── best.pt                 # Trained YOLO model (backend copy)
│   ├── process_video.py        # Detection + distance estimation pipeline
│   └── requirements.txt        # Backend dependencies
│
├── datasets/
│   ├── incidences/
│   ├── people/
│   ├── terrains/
│   └── vehicles/
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── package-lock.json
│
├── yolov8_VisDrone.ipynb       # Model training notebook
├── drone_to_object_height_and_distance.py
├── best (4) (1).pt             # Final trained weights
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### 1️⃣ Train the Model

Open and run:

```
yolov8_VisDrone.ipynb
```

This notebook:
- Installs YOLOv8
- Loads VisDrone dataset
- Trains on custom EO/IR dataset
- Saves best weights

---

### 2️⃣ Backend Setup

Navigate to backend:

```
cd backend
```

Install dependencies:

```
pip install -r requirements.txt
```

Run server:

```
python app.py
```

---

### 3️⃣ Frontend Setup

Navigate to frontend:

```
cd frontend
npm install
npm start
```

---

## 🛰️ How It Works

1. User uploads drone video (RGB or IR).
2. Backend runs YOLOv8 detection.
3. Bounding boxes are generated.
4. Distance & height are estimated using geometric calculations.
5. Processed output is saved in `backend/processed/`.

---

## 📊 Dataset

- 500+ annotated aerial images
- 35+ object classes
- Structured into:
  - People
  - Vehicles
  - Terrains
  - Incidences

---

## 🎯 Applications

- Defense reconnaissance
- Border surveillance
- Disaster monitoring
- Incident detection
- Infrastructure inspection

---

## 👨‍💻 Team SkyLens  
Developed for HAL Aerothon ’25
