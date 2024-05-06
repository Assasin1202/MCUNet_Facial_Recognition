# MCUNet Facial Recognition on Raspberry Pi

This project implements and optimizes the Neural Network for Microcontrollers (MCUNet) for facial recognition, focusing on a dataset representative of the ethnic diversity within Indian demographics. Despite the memory constraints on our available STM32 board, we demonstrate the system using a Raspberry Pi.

## Project Objectives

- Implement MCUNet on resource-constrained platforms, demonstrating the system on a Raspberry Pi due to memory constraints.
- Optimize the network to improve performance specifically tailored to facial recognition.
- Deploy and evaluate a facial recognition system using the developed model and dataset, focusing on its applicability in real-world scenarios.

## Dataset Description

We use two datasets:
- **LFW Dataset Subset**: Standard dataset with 50 subjects, each represented by 10 images at a resolution of 256x256 pixels.
- **IITJ Faces of Academia Dataset (JFAD)**: Custom dataset with 400 images of 40 subjects, reflecting the diversity of the Indian population at IIT Jodhpur.

## Model Development and Conversion

- Models were developed using TensorFlow and optimized for low memory usage with TensorFlow Lite.
- Quantization reduced model sizes to less than 0.7MB for efficient deployment on microcontrollers.

## Setup and Installation

Ensure your Raspberry Pi is up to date with the following commands:
```bash
sudo apt update
sudo apt upgrade -y
```
Install necessary dependencies:
```bash 
sudo apt install python3-pip libatlas-base-dev
pip3 install numpy tflite-runtime
```

## Running the model
Transfer the model.tflite and labels.txt files to the Raspberry Pi. Use SCP, FTP, or a USB drive for file transfer.
Execute the prediction script provided in the repository to process input images and perform predictions.

## Testing and Results
The model was extensively tested using diverse test images, consistently making accurate predictions. Test results are included in the repository.

## Resources 
- GitHub Repository: https://github.com/Assasin1202/MCUNet_Facial_Recognition
- Custom Dataset: https://drive.google.com/drive/folders/1KslnsJhcKdOzZorUB3PkuTwpbW6kMUnk
- Demonstration Video: https://drive.google.com/drive/folders/1KslnsJhcKdOzZorUB3PkuTwpbW6kMUnk
