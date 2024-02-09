# Real-Time Face Mask Detection

Overview
Real-Time Face Mask Detection is a Python-based project that aims to detect whether individuals in a real-time video stream are wearing face masks or not. This project utilizes computer vision and deep learning techniques to achieve its objective. It leverages pre-trained models for face detection and face mask classification, enabling real-time monitoring of mask compliance, which is particularly relevant during the COVID-19 pandemic.

## Requirements
- Python 3.x
- OpenCV
- TensorFlow
- imutils

## Usage
1. Install the required dependencies: `pip install opencv-python tensorflow imutils`.
2. Download the pre-trained face detection model (`deploy.prototxt` and `res10_300x300_ssd_iter_140000.caffemodel`) and the pre-trained face mask detection model (`mask_detector.model`).
3. Update the file paths in the script to point to the downloaded models.
4. Run the script: `python mask_detection.py`.

## Functionality
- The script captures frames from the webcam in real-time.
- It detects faces in each frame using a pre-trained face detection model.
- For each detected face, it predicts whether the person is wearing a mask using a pre-trained face mask detection model.
- Bounding boxes are drawn around detected faces, and labels indicate "Mask" or "No Mask" based on predictions.
- Press 'q' to quit the application.

## Details
- The face detection model is based on the Single Shot MultiBox Detector (SSD) framework, providing fast and efficient face localization.
- The face mask detection model uses transfer learning with the MobileNetV2 architecture, fine-tuned on a dataset of masked and unmasked faces.
- The script supports real-time monitoring of mask compliance, aiding in public health measures during the COVID-19 pandemic.

 ## Models Used
Face Detection Model: The face detection model is based on the Single Shot MultiBox Detector (SSD) framework, which provides fast and accurate face localization capabilities.
Face Mask Detection Model: The face mask detection model utilizes transfer learning with the MobileNetV2 architecture. It has been fine-tuned on a dataset containing images of individuals with and without masks.

## References
- Face detection model: https://github.com/opencv/opencv/blob/master/samples/dnn/face_detector/deploy.prototxt
- Face detection model weights: https://github.com/opencv/opencv_3rdparty/raw/dnn_samples_face_detector_20180220_uint8/res10_300x300_ssd_iter_140000.caffemodel
- Face mask detection model: 
