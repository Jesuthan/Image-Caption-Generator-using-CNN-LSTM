
# 🧠 Image Caption Generator using CNN-LSTM

This project implements an **Image Caption Generator** using a **deep learning architecture** that combines **Convolutional Neural Networks (CNN)** for image feature extraction and **Long Short-Term Memory (LSTM)** networks for generating natural language captions. This was developed as part of the **EC9170 - Deep Learning** course.

---

## 📌 Features

- Preprocessing of captions and image data
- CNN feature extraction using **InceptionV3**
- Sequence modeling with **LSTM**
- Caption generation using greedy search
- Visualization of images with generated captions

---

## 📁 Project Structure

```
├── Deeplearning.ipynb        # Main Jupyter notebook for training and testing
├── images/                   # Image dataset (8091 images)
├── captions.txt              # Text file with 5 captions per image
├── model/                    # (Optional) Trained model files
├── outputs/                  # (Optional) Generated captions and visualizations
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

- **Images**: 8091 images from the Flickr8k dataset (or similar)
- **Captions**: Each image is paired with 5 different captions
- Captions are preprocessed (lowercase, punctuation removal, tokenization)

---

## 🚀 Model Workflow

1. **Caption Preprocessing**
   - Clean text: lowercase, remove punctuation, tokenize
   - Add `<start>` and `<end>` tokens

2. **Image Feature Extraction**
   - Pretrained **InceptionV3** used to extract 2048-dimensional feature vectors

3. **Tokenization & Sequence Creation**
   - Captions are converted to integer sequences and padded

4. **CNN-LSTM Model**
   - CNN features and text input are merged to predict the next word

5. **Caption Generation**
   - Uses greedy search to generate a caption word-by-word from image features

---

## 🖼️ Example Output

```
Image: dog.jpg
Generated Caption: a dog is running in the field
```

---

## 🧪 Evaluation Metrics (Planned)

- BLEU
- CIDEr
- ROUGE
- METEOR

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/image-caption-generator.git
   cd image-caption-generator
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Open `Deeplearning.ipynb` and run all cells in order.

4. Make sure the following files exist:
   - `images/` folder with image dataset
   - `captions.txt` with image IDs and captions

---

## 📈 Future Improvements

- Add evaluation metrics for better performance insights
- Use **Beam Search** for improved caption generation
- Deploy model using Streamlit or Flask

---

## 📚 Reference

- Flickr8k dataset
- TensorFlow documentation
- Paper: “Show and Tell: A Neural Image Caption Generator” (Vinyals et al.)

---

## 👨‍💻 Developed by

**Your Name**  
Anushanth 
Harshini
Jesuthan

