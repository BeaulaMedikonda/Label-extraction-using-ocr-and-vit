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

## 🔢 Understanding Vision Transformer (ViT) Output Codes

During inference, the Vision Transformer (ViT) model outputs **numeric class IDs** such as: 720, 692, 916, 922, 912

These values are **ImageNet class indices**, not errors or random numbers.

### Why do these numbers appear?
* The ViT model used in this project is **pretrained on the ImageNet dataset**, which contains **1000 generic object classes**.
* Since the model is **not fine-tuned** on domain-specific categories (food, medicine, cosmetics), it outputs the **closest matching ImageNet object label** based on visual features.

### What do these codes represent?
Each numeric ID corresponds to a predefined ImageNet object label. For example:

* **720** → packet  
* **692** → bakery  
* **916** → soap dispenser  
* **922** → pill bottle  
* **912** → carton  

These predictions describe the **generic object or packaging type** detected in the image.

### Why are ImageNet labels useful here?
* They confirm that the Vision Transformer correctly captures **global visual structure**.
* They demonstrate the model’s ability to recognize **packaging-level features** such as packets, bottles, and dispensers.
* Mapping these generic object labels to domain-specific categories would require **fine-tuning or an additional classifier head**.

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
