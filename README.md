**# Air Pollution Classifier - Deep Learning Project**

## **Project Overview**
This deep learning project aims to build a robust air quality classifier from photos using two different deep learning architectures. The first model utilizes the **Functional API with MobileNet** as the feature extractor, combined with an **Artificial Neural Network (ANN)** for classification. The second model is based on a **Sequential API with VGG16**, applying **transfer learning** for Convolutional Neural Network (CNN) modeling.

Additionally, a **Flask-based web application** has been developed to allow users to classify air quality from photos using the **VGG16 model**.

---

## **Table of Contents**
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Models](#models)
  - [Functional API with MobileNet and ANN](#functional-api-with-mobilenet-and-ann)
  - [Sequential API with VGG16](#sequential-api-with-vgg16)
- [Web Application](#web-application)
- [Results](#results)
- [Dependencies](#dependencies)
- [How to Use](#how-to-use)
- [License](#license)

---

## **Project Structure**
```
Air-Pollution-Classification/
│-- data/
│-- models/
│   │-- FunctionalModel.h5
│   │-- VGG16.h5
│-- notebooks/
│   │-- functional_mobilenet_ann.ipynb
│   │-- model_testing.ipynb
│   │-- sequential_vgg16_transfer_learning.ipynb
│-- transformers/
│   │-- AQI_Class_le.pkl
│   │-- Location_le.pkl
│   │-- Pollution_le.pkl
│-- webapp/
│   │-- static/
│   │   │-- css/
│   │   │   │-- style.css
│   │   │-- img/
│   │   │   │-- cat.jpg
│   │   │   │-- poster.png
│   │   │-- js/
│   │   │   │-- script.js
│   │-- VGG16.h5
│   │-- app.py
│   │-- templates/
│   │   │-- index.html
│-- README.md
│-- requirements.txt
```

### **Folder & File Descriptions**
- **models/**: Contains H5 models for both deep learning architectures.
- **transformers/**: Includes pickle files for scalers and encoders.
- **notebooks/**: Contains Jupyter notebooks for model training and evaluation.
- **webapp/**: Flask-based web application for real-time air quality classification.
- **data/**: Holds dataset files and metadata.
- **requirements.txt**: Lists all dependencies required for the project.

---

## **Dataset**
This dataset contains images of **air pollution** from various cities in **India and Nepal**. The dataset is divided into two main folders:

1. **Combined_Dataset**
   - **All_img/**: Contains all collected images from different AQI classes.
   - **IND_and_NEP/**: Contains six subfolders representing six different AQI classes.
   - A CSV file is included with the following labeled parameters:
     - **Location, Filename, Year, Month, Day, Hour, AQI, PM2.5, PM10, O3, CO, SO2, NO2, AQI_Class**

You can also use your **own dataset** for training and evaluation by ensuring proper structure and labeling.

---

## **Models**
### **Functional API with MobileNet and ANN**
This deep learning model is built using the **Functional API**:
- **MobileNet** is used as a **pre-trained feature extractor**.
- A **fully connected Artificial Neural Network (ANN)** is added for classification.
- Suitable for **classifying air quality from images**.

### **Sequential API with VGG16 (Transfer Learning)**
This model is built using the **Sequential API**:
- Leverages the **pre-trained VGG16 architecture**.
- **Fine-tuned for air quality classification** using transfer learning.
- Achieves better performance due to **pre-trained weights** and hierarchical feature extraction.

---

## **Web Application**
The project includes a **Flask-based web application** that enables users to upload images and classify air quality using the **VGG16 model**.
- Provides a **user-friendly interface** for real-time air quality assessment.
- Helps in **environmental monitoring** and awareness.

To run the web application, follow the steps in the [How to Use](#how-to-use) section.

---

## **Results**
### **Model Performance**
- **Functional API with MobileNet and ANN**:
  - Achieved **20% accuracy** on the test dataset.
  - Performance can be improved with **hyperparameter tuning, increased dataset size, and alternative architectures**.

- **Sequential API with VGG16 (Transfer Learning)**:
  - Achieved **95% accuracy** on the test set.
  - The model benefits from **pre-trained architectures and fine-tuning** for specific tasks.

While the **Functional API model** shows lower accuracy, further **experimentation and optimizations** can help improve performance. Also, metrics such as **precision, recall, and F1-score** should be analyzed to address class imbalances.

The **integration of the VGG16 model into the web application** remains a **key feature**, providing users with real-time **air quality classification**.

---

## **Dependencies**
Ensure you have the following installed:
- **Python 3.x**
- **TensorFlow 2.x**
- **Flask**
- **PIL (Python Imaging Library)**
- **HTML, CSS, JavaScript** (for the web application)

Install all dependencies using:
```
pip install -r requirements.txt
```

---

## **How to Use**
1. **Clone this repository:**
   ```
   git clone https://github.com/nileshparab42/Air-Pollution-Classification.git
   ```
2. **Navigate to the project folder:**
   ```
   cd Air-Pollution-Classification
   ```
3. **Train and evaluate the deep learning models** using Jupyter notebooks in the `notebooks/` directory.
4. **If using a custom dataset**, place it inside the `data/dataset/` directory and ensure it is properly structured.
5. **Run the web application:**
   ```
   cd webapp
   python app.py
   ```
6. **Access the web app** by opening a browser and navigating to:
   ```
   http://localhost:5000
   ```

---

## **License**
This project is open-source and available for use and modification. Check the `LICENSE` file for more details.

---




