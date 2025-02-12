# Air-pollution-classifier
Air Quality Classifier - Deep Learning Project
Cover image

Project Overview
This deep learning project focuses on building a robust air quality classifier from photos using two different deep learning architectures. The first model utilizes the Functional API with MobileNet as the feature extractor, combined with an Artificial Neural Network (ANN) for classification. The second model is based on a simple Sequential API with VGG16, applying transfer learning for Convolutional Neural Network (CNN) model. Additionally, a web application has been developed to allow users to classify air quality from photos using the VGG16 model.

Table of Contents
Project Structure
Dataset
Models
Functional API with MobileNet and ANN
Sequential API with VGG16
Web Application
Results
Dependencies
How to Use
License
Project Structure
|-- Air-Pollution-Classification/
    |-- data/
    |-- models/
        |-- FunctionalModel.h5
        |-- VGG16.h5
    |-- notebooks/
        |-- functional_mobilenet_ann.ipynb
        |-- model_testing.ipynb
        |-- sequential_vgg16_transfer_learning.ipynb
    |--transformers/
        |--AQI_Class_le.pkl
        |--Location_le.pkl
        |--Pollution_le.pkl
    |-- webapp/
        |--static/
            |--css
                |--style.css	
            |--img
                |--cat.jpg
                |--poster.png
            |--js
                |--script.js	
	    |--VGG16.h5
        |-- app.py
        |-- templates/
            |-- index.html
    |-- data/
        |-- dataset.docx
    |-- README.md
    |-- requirements.txt
models/: This directory contains H5 models for the two deep learning models.
transformers/: This directory contains pickle files for the two scalers and encoders.
notebooks/: This directory contains Jupyter notebooks for the two deep learning models.
webapp/: Contains the code for the web application built using Flask.
data/: This directory can contain the dataset used to train and evaluate the models.
README.md: This file (the current document) providing an overview of the project.
requirements.txt: This file contains all requirements versions for of the project.
Dataset
This dataset contains images of Air Pollution for different cities in India and Nepal. The dataset is divided into two folders: Combined_Dataset and Country_wise_Dataset. Total number of image dataset: 12,240

The combined dataset folder contains two subfolders.

All_img: This subfolder contains all the collected images from all AQI classes.
IND_and_NEP: This subfolder contains six different subfolders representing six different classes of AQI. The csv file in this folder contains all the data and its parameters. It is labeled as
Location, Filename, Year, Month, Day, Hour, AQI, PM2.5, PM10, O3, CO, SO2, NO2, and AQI_Class
You can use your own dataset for training and evaluation. Ensure that it is appropriately structured and labeled. If you need a sample dataset for testing, you can find public datasets related to air quality and images.

Models
Functional API with MobileNet and ANN
Functional api

The first deep learning model is built using the Functional API. MobileNet is used as a pre-trained model for feature extraction, and an Artificial Neural Network (ANN) is added on top of it for classification. This model is suitable for classifying air quality from images.

Sequential API with VGG16
Transfer Learning

The second model is constructed using the Sequential API and utilizes the VGG16 architecture with transfer learning. This approach is effective for leveraging pre-trained weights from VGG16 and fine-tuning them for air quality classification.

Web Application
Web App

The project includes a web application built with Flask, allowing users to upload images and classify air quality using the VGG16 model. The web application provides a user-friendly interface for real-time air quality assessment.

Results
Cover image

In the air quality classifier project, we observed varying levels of accuracy between the two deep learning models employed:

Functional API with MobileNet and ANN: While this model, combining MobileNet for feature extraction and an Artificial Neural Network (ANN) for classification, demonstrated reasonable performance, it achieved an accuracy of 20% on the test dataset. Although the accuracy might be lower than desired, it is essential to consider fine-tuning hyperparameters, increasing the dataset size, or exploring alternative architectures to potentially improve the model's performance further.

Sequential API with VGG16: The Sequential API model, using the pre-trained VGG16 architecture with transfer learning, performed well, with an accuracy of 95% on the test set. This model's robust performance showcases the advantage of leveraging pre-trained architectures and fine-tuning them for specialized tasks.

While the Functional API model may have exhibited lower accuracy, it is important to note that deep learning model performance can be highly sensitive to factors such as hyperparameters, data quality, and dataset size. Further experimentation and optimization may lead to improvements in its classification accuracy. Additionally, model evaluation metrics beyond accuracy, such as precision, recall, and F1-score, can provide a more comprehensive view of the model's performance, especially if class imbalances exist in the dataset.

The integration of the VGG16 model into the web application remains a valuable feature, providing users with real-time air quality classification and serving as a practical tool for environmental monitoring. Further refinements and enhancements can be made to both models to continually improve their accuracy and usability in real-world scenarios.

Dependencies
Python 3.x
TensorFlow 2.x
Flask
PIL (Python Imaging Library)
HTML/CSS/JavaScript (for the web application)
You can install Python dependencies using pip with the provided requirements.txt file.
pip install -r requirements.txt
How to Use
Clone this repository to your local machine.
git clone https://github.com/nileshparab42/Air-Pollution-Classification.git
cd Air-Pollution-Classification
Train and evaluate the deep learning models using the Jupyter notebooks provided in the models/ directory.

If you have your own dataset, place it in the data/dataset/ directory. Ensure that your dataset is organized correctly.

To run the web application, navigate to the webapp/ directory and execute app.py.

cd webapp
python app.py
Access the web application by opening a web browser and going to http://localhost:5000.
