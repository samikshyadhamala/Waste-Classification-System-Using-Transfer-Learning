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
<img width="501" height="742" alt="image" src="https://github.com/user-attachments/assets/0cb5f610-385c-4e81-bbcd-6cdf66ed9d2d" />

## Hardware integration results

| Image 1 | Image 2 |
|---------|---------|
| ![](<img width="501" height="742" alt="image" src="https://github.com/user-attachments/assets/75d40c7b-ed38-4a42-9e0d-92fe3da0f1d7" />) | ![](<img width="501" height="742" alt="image" src="https://github.com/user-attachments/assets/43d38671-2731-43b4-ab26-667ab2f518b0" />) |


**Pipeline**

1. Camera captures waste image  
2. Image processed by **MobileNetV2**  
3. Model predicts waste category  
4. Sorting mechanism directs waste to the correct bin  

---

## Project Structure
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

