#Yolov7 Demo

## Introduction
**YOLOv7** is a cutting-edge deep learning architecture designed for real-time object detection tasks, offering both high speed and accuracy. By employing an optimized convolutional neural network (CNN) backbone, YOLOv7 effectively detects objects in images with remarkable efficiency. It utilizes advanced feature extraction techniques and novel model scaling strategies, which enable it to capture both small and large objects in diverse scenes with minimal computational overhead.

## Folder Structure

```plaintext
models/
└── yolov7/
    ├── reference/
    │   ├── yolov7.py                 # yolov7 model implementation
    │   ├── yolov7_utils.py           # Utility functions for yolov7
    |   ├── yolov7_config.py          # Yolov7 model architecture
    ├── tests/
    │   ├── test_yolov7.py            # Unit tests for Yolov7 model
    │   ├── test_demo_yolov7.py       # Whole Model test Setup
    └── README.md                         
```

# Details

- **Implementation Source**: (https://github.com/WongKinYiu/yolov7)

- The reference model is implemented in `yolov7/reference/yolov7.py`. Utility methods are included in `yolov7/reference/yolov7_utils.py`.Model architecture is included as config file in`yolov7/reference/yolov7_config.py`.

- Each sub-module of this reference model is validated against the original Transformers package using the **Pearson Correlation Coefficient (PCC)** metric to ensure accuracy.

- Unit tests for sub-modules are located in `yolov7/tests/test_yolov7.py` for input resolutions of Images - `(733*733),(512*512)` with `batch size of 1`.

- This reference implementation uses pre-trained model weights from the github repo(https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt)

## Commands to Run

### To run all the tests with logging output:

```pytest models/yolov7/```

This will return both the test results.

### To run the demo test alone:

```pytest models/yolov7/tests/test_demo_yolov7.py -s```


### To run sub-module tests alone:

```pytest models/yolov7/tests/test_yolov7.py```

## Expected Demo Results

```The runs folder will be created inside the tests folder. For reference, the model output will be stored in reference_output, while the Torch model output will be stored in torch_output.```
