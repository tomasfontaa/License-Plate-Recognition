# 🚗 License Plate Recognition with YOLOv8 and PaddleOCR

This project shows how to detect and read car license plates using deep learning. It uses **YOLOv8** for plate detection and **PaddleOCR** for text recognition.

## 📌 Goal

The goal is to create a full pipeline that:
- Detects where a license plate is in a car image.
- Crops and corrects the image perspective.
- Uses OCR to read the plate number.
- Compares the result with the real plate (from the file name).
- Calculates accuracy metrics.

## 🧰 Tools Used

- **YOLOv8** from Ultralytics for object detection.
- **PaddleOCR** for reading text from the cropped license plate.
- **Albumentations** for data augmentation.
- **OpenCV** and **Matplotlib** for image processing and visualization.
- **Scikit-learn** for dataset splitting.
- **Pandas** for results and metrics.

## 📁 Project Structure

- `images/` – Original images
- `annotations/` – XML labels (Pascal VOC format)
- `labels/` – Converted YOLO format labels
- `augmented/` – Augmented images and labels
- `train/`, `val/`, `test/` – Training, validation, and test datasets
- `data.yaml` – Configuration file for YOLO training
- `License_Plate_Recognition.ipynb` – Main notebook

## 🚀 Main Steps

1. **Load and preview the dataset**
2. **Convert XML annotations to YOLO format**
3. **Apply data augmentation**
4. **Split the dataset into train, val, and test**
5. **Train YOLOv8 model to detect plates**
6. **Use PaddleOCR to read text from detected plates**
7. **Evaluate predictions and calculate accuracy**

## 📊 Results

- **Exact match rate**: 86.96%
- **Character-level accuracy**: 93.48%

These results were calculated by comparing predictions with real plate numbers found in the image filenames.

## 🧠 Final Thoughts

- The model works well in most images.
- Performance drops when plates are very rotated or low quality.
- Future improvements:
  - Use a model to enhance image resolution.
  - Improve perspective correction for better OCR results.

## ✅ How to Run

1. Open the notebook: `License_Plate_Recognition.ipynb`
2. Follow each cell step by step
3. Make sure to upload the dataset ZIP file when asked
4. All predictions and metrics will be shown directly

---

Made by Tomás Fonta
