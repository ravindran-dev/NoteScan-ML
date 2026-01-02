<p align="center">
  <img src="https://img.shields.io/badge/NoteScan-OCR%20&%20Deep%20Learning-blueviolet?style=for-the-badge" />
</p>

This notebook presents a complete experimental and implementation workflow for **Handwritten Text Recognition (HTR)** using a transformer-based OCR model. It is designed for academic, research, and project submission purposes, and documents each stage of the pipeline clearly and reproducibly.



## Objective

The primary objective of this notebook is to convert handwritten text images into accurate, machine-readable digital text using a deep learning model. The notebook demonstrates how modern transformer architectures can be applied to handwritten document understanding.



## Scope of the Notebook

This notebook covers the full HTR pipeline, including:

* Loading a pretrained handwritten OCR model
* Image preprocessing and enhancement
* Line-level text segmentation
* OCR inference using a transformer
* Text normalization and post-processing
* Quantitative evaluation using standard metrics
* Optional PDF-based document processing



## Model Used

The notebook uses **TrOCR (Transformer-based Optical Character Recognition)**, a vision-encoder-decoder model provided by Microsoft and released through Hugging Face.

* Vision Encoder: Vision Transformer (ViT)
* Text Decoder: Transformer language model
* Training Data: Handwritten text corpora

The model is used in inference-only mode without fine-tuning.



## Environment and Dependencies

The notebook is executed using **Python 3.10** in a virtual environment. The key dependencies include:

* PyTorch
* Transformers (Hugging Face)
* OpenCV
* Pillow
* NumPy
* SentencePiece
* Protobuf
* JiWER (for evaluation)
* Pandas and TQDM

All dependencies are expected to be installed inside a dedicated virtual environment to ensure reproducibility.



## Workflow Overview

### 1. Environment Setup

Initial setup includes importing required libraries and configuring the runtime environment.

### 2. Device Selection

The notebook automatically selects a GPU if available, otherwise defaults to CPU execution.

### 3. Model and Processor Loading

The TrOCR processor and model are loaded from pretrained checkpoints. A slow tokenizer is explicitly used to ensure compatibility and stability.

### 4. Image Preprocessing

Input images are preprocessed using classical computer vision techniques such as grayscale conversion, noise reduction, and normalization to improve recognition accuracy.

### 5. Line Segmentation

Text regions are segmented into individual lines using horizontal projection profiles. This improves OCR accuracy for multi-line handwritten documents.

### 6. OCR Inference

Each segmented text line is passed through the TrOCR model to generate textual predictions.

### 7. Post-Processing

The raw OCR output is cleaned using normalization and spelling correction techniques. Domain-specific corrections are optionally applied to improve readability.

### 8. Evaluation

The notebook evaluates OCR performance using:

* Character Error Rate (CER)
* Word Error Rate (WER)

Ground-truth transcriptions are provided through a labeled CSV file.

### 9. PDF Processing (Optional)

Multi-page handwritten PDFs can be converted into images and processed page by page using the same OCR pipeline.



## Input and Output

### Input

* Handwritten image files (PNG, JPG)
* Optional handwritten PDF documents
* CSV file containing ground-truth transcriptions for evaluation

### Output

* Recognized text printed in the notebook
* Quantitative evaluation metrics (CER and WER)
* Optionally exported text documents (DOCX or PDF)



## Evaluation Methodology

Evaluation is performed by comparing OCR predictions with manually annotated ground-truth text. The notebook computes CER and WER across the dataset to measure recognition accuracy.

Lower values of CER and WER indicate better OCR performance.


## Limitations

* Performance depends heavily on handwriting quality
* Complex layouts and tables are not fully supported
* The model is not fine-tuned on custom handwriting styles



## Possible Extensions

* Fine-tuning the model on custom datasets
* Support for multilingual handwriting
* Layout-aware document understanding
* Integration with web or mobile applications



## Usage Notes

This notebook is intended for:

* Academic coursework
* Research experiments
* Proof-of-concept development
* Integration into larger OCR systems

Users are encouraged to review each section sequentially to understand the complete pipeline.





## License

This notebook is provided for educational and research use. Any pretrained models used are subject to their respective licenses.

##  Author - **Ravindran S** 


Developer • ML Enthusiast • Neovim Customizer • Linux Power User  

Hi! I'm **Ravindran S**, an engineering student passionate about:

-  Linux & System Engineering  
-  AIML (Artificial Intelligence & Machine Learning)  
-  Full-stack Web Development  
-  Hackathon-grade project development  




## 🔗 Connect With Me

You can reach me here:

###  **Socials**
<a href="www.linkedin.com/in/ravindran-s-982702327" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white">
</a>


<a href="https://github.com/ravindran-dev" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-111111?style=for-the-badge&logo=github&logoColor=white">
</a>


###  **Contact**
<a href="mailto:ravindrans.dev@gmail.com" target="_blank">
  <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white">
</a>


