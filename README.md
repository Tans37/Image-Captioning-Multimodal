# Image Captioning with T5 and EfficientNet

This project builds a compact yet effective image captioning pipeline using:
- 🧠 **EfficientNet** for visual feature extraction
- ✍️ **T5-small** for natural language generation

It combines computer vision and NLP into a streamlined, multimodal architecture — capable of generating human-like captions from image inputs.

---

## 🚀 Project Structure
```
image-captioning-t5/
├── models/                # Captioning model & feature extractor
├── scripts/               # Training, inference, evaluation, feature extraction
├── utils/                 # Dataset class, BLEU, captioning helpers
├── outputs/               # Model checkpoints (not included in repo)
├── notebooks/             # (Optional) end-to-end development notebook
├── requirements.txt       # Python dependencies
├── .gitignore             # Excludes weights and data
└── README.md              # This file
```
## Model Pipeline
![ChatGPT Image Apr 8, 2025, 02_47_27 AM (1)](https://github.com/user-attachments/assets/e2e84db2-5502-4ac4-ad99-733bd3caaf6c)

---

## 📦 How to Run
### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Prepare Dataset & Weights
Due to GitHub's file size limitations, the dataset and pretrained weights are **not included in this repository**. Please download them manually:

- 📁 **Flickr8k Dataset**: Download the image folder and captions file from [official source](https://github.com/goodwillyoga/Flickr8k_dataset?tab=readme-ov-file)
- 💾 **Model Weights**: If you wish to use pretrained `.pth`(T5 weights) or `.pkl`(Extracted Image Features using EfficientNet) files, store them locally in `outputs/model_checkpoints/` and `outputs/`, respectively.

### 3. Extract Image Features
```bash
python scripts/extract_features.py
```

### 4. Train the Model
```bash
python scripts/train.py
```

### 5. Evaluate BLEU Score & Test Loss
```bash
python scripts/evaluate.py
```

### 6. Run Inference
```bash
python scripts/infer.py
```

---

## 📊 Example Output

![482098572_e83153b300](https://github.com/user-attachments/assets/95c20904-f268-4c1d-aea6-86983d0eece9)

A man in a red jacket is riding a yellow kayak in the water.

![1827560917_c8d3c5627f](https://github.com/user-attachments/assets/ec730a05-09d1-47d8-9fb0-6bc07b5285eb)

A black and white dog is carrying a stick in its mouth.

---

---

## 📈 Quantitative Results
- **Final Validation Loss**: 1.19
- **Final Test Loss**: 1.20
- **BLEU-4 Score**: 0.2359 on the test set

### 📉 Training and Validation Loss Curve

![train vs val](https://github.com/user-attachments/assets/ac9d5c54-dadd-4f85-b48f-974a58552068)

---


## 🔍 Future Plans
- Real-time video captioning with OpenCV
- T5-base / BLIP2 / CLIP-based captioning
- Multilingual caption generation
- Deploy via Gradio or Streamlit

---

## 📚 Dataset Credits

The **Flickr8k** dataset is provided by the University of Illinois at Urbana-Champaign (UIUC).  
Original source and license details: http://cs.stanford.edu/people/karpathy/deepimagesent/

- Dataset creators: Micah Hodosh, Peter Young, and Julia Hockenmaier  
- Citation:  
  Hodosh, M., Young, P., & Hockenmaier, J. (2013).  
  *Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics*.  
  Journal of Artificial Intelligence Research, 47, 853–899.

---

Made by: [Tanishq Sharma](#)
