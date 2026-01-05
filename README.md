# Product Label Analysis using OCR and Vision Transformer

This project analyzes real-world product packaging images using OCR and Vision Transformer models.
It demonstrates how text-heavy product labels can be processed despite noisy layouts.

---

## 🚀 Features
* OCR text extraction from real product labels using EasyOCR
* Vision Transformer (ViT) for generic object recognition
* Handles food, medicine, and cosmetic product categories
* Designed for real-world packaging images (not clean datasets)

---

## 🧠 Tech Stack
* Python
* EasyOCR
* Vision Transformer (ViT)
* OpenCV
* PyTorch
* NumPy

---


## 📊 Dataset
Images are organized into category folders:
* `food/`
* `medicine/`
* `cosmetics/`

Only a **small sample** is included for demonstration purposes.

---

## ⚠️ Important Notes
* ViT is used as a pretrained model and outputs ImageNet object labels
* Domain-specific classification would require fine-tuning
* OCR output may be noisy due to real-world packaging layouts

---

## 🔮 Future Improvements
* Train a lightweight classifier head on top of ViT
* Improve OCR post-processing
* Add batch processing support
