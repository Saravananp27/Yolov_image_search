# YOLO Image Search System

## ABSTRACT 
The YOLO Image Search System is a computer vision application developed using YOLOv11 for object detection and image retrieval. The system detects objects present in images, generates metadata from detection outputs, and allows users to search images using object-based filters. An interactive Streamlit interface is used to process images, visualize results, and perform intelligent image searches.

## Dataset & YOLO Model Details (COCO)
This project uses the COCO dataset classes, which contain 80 common object categories such as person, car, dog, cat, airplane, and banana. The detection model used is YOLOv11, chosen for its fast inference speed, improved accuracy, and real-time object detection capability. The model predicts object classes, bounding boxes, and confidence scores which are later converted into searchable metadata.

## Environment Setup
Before running the project, install:

### Prerequisites
Python 3.11

Anaconda / Miniconda

Visual Studio Code (VS Code)

NVIDIA GPU (Optional – for GPU acceleration)

### Open the project folder inside VS Code.

#### Required project files:
```
requirements.txt
instructions.txt
app.py
```
### Open terminal in VS Code:
```
View → Terminal
```

## GPU Installation Steps

### Step 1 – Create Conda Environment
```
conda create -n yolo-image-search-gpu python=3.11 -y
```
### Step 2 – Activate Environment
```
conda activate yolo-image-search-gpu
```
### Step 3 – Install PyTorch with CUDA Support
```
conda install pytorch torchvision pytorch-cuda=12.4 -c pytorch -c nvidia
```
### Step 4 – Install Project Dependencies
```
pip install -r requirements.txt
```
## How to Run in VS Code using Conda
### Activate Environment
```
conda activate yolo-image-search-gpu
```
### Launch the Streamlit interface
```
streamlit run app.py
```
### The terminal will display and Open Browser:
```
Local URL: http://localhost:8501
```
### Features Available in UI
Upload image dataset

Select YOLOv11 model

Process images

Generate metadata

Apply search filters

Display results grid

Export JSON output

## Output
### UI Screenshot
<img width="1901" height="900" alt="image" src="https://github.com/user-attachments/assets/c4f57d76-3979-4eee-9c10-a34fc93790a3" />

### Object Detection Output
<img width="1787" height="959" alt="image" src="https://github.com/user-attachments/assets/0f76f013-3e49-420f-9f2e-150deab2a886" />

<img width="1842" height="740" alt="image" src="https://github.com/user-attachments/assets/35c8f447-4ca8-47ae-8a7a-873608cbd94f" />

<img width="1817" height="1068" alt="image" src="https://github.com/user-attachments/assets/7f4a7dc0-50a9-4437-9e97-7398c771490c" />

### VS Code Terminal Output
<img width="1908" height="1199" alt="image" src="https://github.com/user-attachments/assets/8d3679dc-ba98-40bc-a60c-45891fc66380" />

<img width="1908" height="1199" alt="image" src="https://github.com/user-attachments/assets/087b9f78-ee0d-495c-a68e-7a676be0d485" />

## Enhancements
The system goes beyond basic object detection by introducing metadata-based image searching. Detection outputs are stored in JSON format, allowing fast querying without rerunning inference. The application also supports logical filtering using AND/OR conditions, threshold-based searches, and loading previously generated metadata for quicker execution. The modular pipeline improves scalability and maintainability.

## Result & Conclusion
The YOLO Image Search System successfully performs object detection, metadata generation, and image retrieval using YOLOv11. The Streamlit interface provides a simple and interactive user experience, while reusable metadata reduces repeated computation. Overall, the project demonstrates an effective combination of computer vision, metadata engineering, and UI deployment for building an intelligent image search system.
