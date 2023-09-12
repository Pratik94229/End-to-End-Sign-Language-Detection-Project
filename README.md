# End-to-end Sign Language Detection using YOLOv5

![Sign Language Detection](https://news.uga.edu/wp-content/uploads/2019/09/nonverbal-signals-810x486.jpg)

## Introduction

Sign Language Detection is a project aimed at recognizing and interpreting hand gestures from sign language. This end-to-end solution employs the YOLOv5 object detection model to identify sign language phrases such as "Hello," "I love you," "Yes," "No," and "Please." The model can help bridge communication gaps and facilitate better understanding between individuals who use sign language and those who don't.

## Folder structure
```
├───data
├───docs
├───flowcharts
├───notebook
├───signLanguage
│   ├───components
│   │   
│   ├───configuration
│   │  
│   ├───constant
│   │   ├───training_pipeline
│   │   
│   ├───entity
│   │   
│   ├───exception
│   │   
│   ├───logger
│   │ 
│   ├───pipeline
│   │  
│   ├───utils
├───templates
└───yolov5
    ├───.github
    │   ├───ISSUE_TEMPLATE
    │   └───workflows
    ├───classify
    ├───data
    │   ├───hyps
    │   ├───images
    │   └───scripts
    ├───models
    │   ├───hub
    │   ├───segment
    │   └───__pycache__
    ├───runs
    │   └───detect
    │       ├───exp
    │       ├───exp2
    │       ├───exp3
    │       └───exp4
    ├───segment
    ├───utils
    │   ├───aws
    │   ├───docker
    │   ├───flask_rest_api
    │   ├───google_app_engine
    │   ├───loggers
    │   │   ├───clearml
    │   │   ├───comet
    │   │   └───wandb
    │   ├───segment
    │   │   └───__pycache__
    │   └───__pycache__
    └───__pycache__
```

## Model Architecture

The project utilizes the YOLOv5 object detection model, a popular and efficient deep learning model for real-time object detection. YOLOv5 comes in various sizes (small, medium, large, and extra-large) to cater to different computing capabilities. In this implementation, I have selected small model size that balances accuracy and speed while running on various devices.

## Dataset

The training dataset comprises a collection of annotated images and corresponding labels for the sign language phrases "Hello," "I love you," "Yes," "No," and "Please." The dataset is preprocessed and split into training, validation, and test sets to train and evaluate the YOLOv5 model effectively.

## Training

The YOLOv5 model is trained on the annotated dataset using transfer learning. By fine-tuning the pre-trained YOLOv5 model on our sign language dataset, we can leverage the model's knowledge from other object detection tasks and apply it to our specific domain. The training process involves optimizing the model's parameters to achieve accurate sign language detection.

## Inference

After training the YOLOv5 model, we can perform inference on new images or real-time video streams. The model predicts bounding boxes around the sign language phrases present in the input data and provides the corresponding class labels. This information is then used to interpret the detected gestures, making sign language accessible to a wider audience.

## Usage

To use this Sign Language Detection project, follow these steps:

1. Clone the repository to your local machine:
   ```
   git clone https://github.com/Pratik94229/End-to-end-Sign-Language-Detection.git
   ```
2. Created virtual enviorment using cmd in the cloned repository:
```
   conda create -p venv python==3.8
   conda activate venv/
```
3. Install the required dependencies by running:
   ```
   pip install -r requirements.txt
   ```

4. Run the notebook to train YOLOv5 model.

5. Run the application using the command:
   ```
   python app.py
   ```
6. Access the application: Open your web browser and go to http://localhost:8080 to access the text summarization service.

7. Select the image for which prediction is to be made.

8. The script will output the image or video with bounding boxes and class labels of detected sign language phrases.

9. For making prediction on video change route to to http://localhost:8080/live

## Results

The trained YOLOv5 model achieves high accuracy and real-time performance, allowing for seamless sign language detection in a variety of scenarios. The model's performance has been evaluated on the test set, and the results are presented in the project's documentation.

## Conclusion

Sign Language Detection using YOLOv5 is a promising project that empowers individuals who use sign language to communicate with the broader community. By leveraging the power of deep learning and computer vision, this project aims to make sign language more accessible and inclusive for everyone.

---

For any inquiries or questions, please feel free to contact me at pratik.941@gmail.com.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
