# Driver Drowsiness Detection Using Deep Learning

## Project Overview

This project presents a CNN-based driver drowsiness detection system using eye state classification. The system identifies whether the driver's eyes are open or closed from video frames. If the eyes remain closed for a consecutive period, the system generates a drowsiness alert.

## Problem Statement

Driver drowsiness is an important cause of road accidents. A driver may lose attention or fall asleep while driving. Therefore, a computer vision-based system can be used to monitor the driver's eye state and provide an alert when prolonged eye closure is detected.

## Objective

The main objectives of this project are:

* To detect the driver's eye region from video frames.
* To classify eyes as Open or Closed using a CNN.
* To identify prolonged eye closure.
* To generate a drowsiness warning.
* To demonstrate the system using a prerecorded driving video.

## Proposed System

The proposed system combines OpenCV and a Convolutional Neural Network (CNN).

### Working Process

Driving Video
↓
Eye Detection using OpenCV
↓
Eye Image Preprocessing
↓
CNN Eye State Classification
↓
Open Eyes / Closed Eyes
↓
Consecutive Closed-Eye Detection
↓
Drowsiness Alert

## Dataset

The project uses a publicly available eye-state image dataset containing:

* 2,000 Open Eyes images
* 2,000 Closed Eyes images
* Total: 4,000 images

The dataset was divided into:

* Training: 3,200 images
* Validation: 800 images

## CNN Model

The CNN consists of:

* Convolutional layers
* Max Pooling layers
* Flatten layer
* Fully Connected Dense layer
* Dropout layer
* Sigmoid output layer

The model was trained using:

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Epochs: 10
* Input Image Size: 128 × 128 pixels

## Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab

## Results

The trained CNN achieved an overall validation accuracy of:

**88.75%**

### Classification Results

| Eye State   | Precision | Recall | F1-Score |
| ----------- | --------- | ------ | -------- |
| Closed Eyes | 0.82      | 1.00   | 0.90     |
| Open Eyes   | 1.00      | 0.78   | 0.87     |

The model correctly detected all closed-eye samples in the validation set, giving a closed-eye recall of 100%.

## Output

The final video demonstration displays:

* Eye detection box
* Open Eyes / Closed Eyes status
* Driver Alert
* Drowsiness Alert when prolonged eye closure is detected

The demonstration was tested using a prerecorded driving video.

## Project Structure

```text
Driver-Drowsiness-Detection/
│
├── drowsiness_detection.ipynb
├── requirements.txt
├── README.md
└── results/
```

## Note

This project is an academic prototype for demonstrating computer vision and deep learning concepts. It is not intended to be used as a certified vehicle safety system.

## Future Scope

The project can be improved by:

* Using a larger and more diverse dataset.
* Detecting the face and both eyes more robustly.
* Using temporal models such as LSTM.
* Adding a buzzer or other hardware alert.
* Testing the system with real-time camera input.
