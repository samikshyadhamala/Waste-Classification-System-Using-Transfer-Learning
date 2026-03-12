# 🗑️ Smart Waste Classification System

A lightweight **waste classification system** using **MobileNetV2 transfer learning**, designed to run on **Raspberry Pi 4** for real-time waste sorting.

The model classifies waste into **5 categories**:

- Metal
- Organic
- Paper
- Plastic
- None (background)

The system performs **offline inference**, making it suitable for low-resource environments.

---

## Model Performance

| Model | Accuracy |
|------|------|
| Baseline | 71.2% |
| Augmented | **93.6%** |

Offline data augmentation significantly improved performance.

---

## How the System Works

<img width="1016" height="487" alt="image" src="https://github.com/user-attachments/assets/bcc65b0f-ac15-49ce-9111-455ed2e13ad0" />

## Hardware setup

<img width="485" height="273" alt="image" src="https://github.com/user-attachments/assets/aa39785e-2b4a-47c4-b059-839f0f8f0bcd" />

## Hardware integration result 

<img width="501" height="742" alt="image" src="https://github.com/user-attachments/assets/80254733-c9d6-40a5-a644-794e2ea1dc67" />

<img width="501" height="742" alt="image" src="https://github.com/user-attachments/assets/0cb5f610-385c-4e81-bbcd-6cdf66ed9d2d" />

**Pipeline**

1. Camera captures waste image  
2. Image processed by **MobileNetV2**  
3. Model predicts waste category  
4. Sorting mechanism directs waste to the correct bin  

---

## Project Structure
```
5catModel/
├── waste_classification.ipynb
└── 5cat_mobilenet_best.pth

Augmented5catModel/
├── au_train_waste.ipynb
└── aug_mobilenet_best.pth

metal/
none/
organic/
paper/
plastic/

train/
test/
```
