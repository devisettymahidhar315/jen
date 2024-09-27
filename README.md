# TVM CPU optimisation for segformer-b0-finetuned-ade-512-512

## Introduction
We are optimizing the SegFormer semantic segmentation model using TVM with various CPUs as the target. In this repository, we first convert the PyTorch model to ONNX, then back to PyTorch, validating accuracy at each stage. Next, we convert the model to TVM for different targets, measuring inference time, CPU utilization, and accuracy for each CPU backend. After applying optimizations and tuning the model, we assess the inference time and accuracy again. The ADE-512-512 dataset is used for the entire process.

## Dataset
We have four images, consisting of two sets. Each set contains an original image (multi-dimensional) and a corresponding semantic image (1-dimensional).

## Main
As we above disscuused pytorch to onnx , onnx to pytorch and tvm without opmization and tvm with optmization ,we have the entire code in `main.py`.
- **Model** : I imported the model directly from the Transformers library.
- **Input Resolution** : I imported the images from the Hugging Face URL.
- **Input Preprocessing** : wrote the torchvision.transforms code to convert the image into a tensor of size (512,512).
- **Batch Size** : The demo is tested with a batch size of **1**.
- **Cpu targets** : llvm and llvm -mcpu=core-avx2
- **Tuners** : Random, Grid Search and Xgb

## Running
Run the entire code
```bash
Python models/segformer/main.py
```

## Expected Demo Results
<img width="211" alt="image" src="https://github.com/user-attachments/assets/365ce999-099c-4191-9cc0-57f8dbea4841">

<img width="281" alt="image" src="https://github.com/user-attachments/assets/029c8387-569f-4a99-afc9-b42902ea62af">



