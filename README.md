# 🧠 Image Caption Generator using CNN-LSTM

An **Image Caption Generator** built with a deep learning architecture that combines **Convolutional Neural Networks (CNN)** for image feature extraction and **Long Short-Term Memory (LSTM)** networks for generating natural language captions.

Developed for **EC9170 – Deep Learning**, University of Jaffna.

---

## 📌 Features

- Preprocessing of captions and image data
- CNN feature extraction using **InceptionV3**
- Sequence modeling with **LSTM**
- Caption generation using greedy search
- Visualization of images alongside their generated captions

---

## 📁 Repository Contents

```
├── CNN-LSTM.ipynb          # Initial merged CNN + LSTM implementation
├── CNN-LSTM_final.ipynb    # Final training and inference notebook  ← start here
├── CNN-separate.ipynb      # CNN feature extraction run separately
└── README.md
```

The dataset is **not** committed to this repository. Before running, place it alongside the notebooks:

```
├── images/                 # 8,091 Flickr8k images
└── captions.txt            # 5 captions per image
```

---

## 🧰 Tech Stack

- Python 3
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib
- Scikit-learn
- Pretrained CNN: **InceptionV3**

---

## 📦 Dataset

- **Images**: 8,091 images from the Flickr8k dataset
- **Captions**: each image paired with 5 different captions
- Preprocessing: lowercasing, punctuation removal, tokenization

---

## 🚀 Model Workflow

1. **Caption preprocessing** — clean text (lowercase, strip punctuation, tokenize), wrap each caption in `<start>` and `<end>` tokens
2. **Image feature extraction** — pretrained InceptionV3 produces a 2048-dimensional feature vector per image
3. **Tokenization & sequencing** — captions converted to integer sequences and padded to uniform length
4. **CNN-LSTM model** — image features and partial text sequences are merged to predict the next word
5. **Caption generation** — greedy search decodes a caption word-by-word from the image features

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Jesuthan/Image-Caption-Generator-using-CNN-LSTM.git
   cd Image-Caption-Generator-using-CNN-LSTM
   ```

2. Install dependencies:

   ```bash
   pip install tensorflow numpy pandas matplotlib scikit-learn pillow
   ```

3. Add the dataset — download Flickr8k and place `images/` and `captions.txt` in the repository root.

4. Launch Jupyter and open the final notebook:

   ```bash
   jupyter notebook CNN-LSTM_final.ipynb
   ```

5. Run all cells in order.

---

## 🖼️ Example Output

```
Image: dog.jpg
Generated Caption: a dog is running in the field
```

---

## 🧪 Evaluation

Quantitative evaluation is **not yet implemented**. Captions are currently assessed qualitatively by inspecting generated output against the source image.

Planned metrics: BLEU, CIDEr, ROUGE, METEOR.

---

## 📈 Future Improvements

- Implement BLEU/CIDEr/ROUGE/METEOR scoring for measurable performance
- Replace greedy search with **beam search** for higher-quality captions
- Add attention (Show, Attend and Tell) over the CNN feature map
- Deploy as a web demo using Streamlit or Flask

---

## 📚 References

- Flickr8k dataset
- TensorFlow / Keras documentation
- Vinyals et al., *"Show and Tell: A Neural Image Caption Generator"* (2015)

---

## 👨‍💻 Authors

Built as a group project for EC9170 – Deep Learning:

- **Anushanth**
- **Harshini**
- **Jesuthan** ([@Jesuthan](https://github.com/Jesuthan))
