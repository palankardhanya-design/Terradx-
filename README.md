# Terradx- Plant 🌱 Disease 🐛 Detector 🔎

ML Powered website to assist farmers in crop disease detection and alerts.

## Product Walkthrough


https://user-images.githubusercontent.com/57388834/120083080-fd9d8480-c0e3-11eb-9f9e-0a3f114f6d78.mp4



## Download Product Apk **[here](https://drive.google.com/file/d/1OldNeNr5KRfFX5G56689_fnSCuSGvTCM/view?usp=sharing)**
## Machine Learning **[Python Notebook](https://github.com/nandakishormpai2001/Plant_Disease_Detector/blob/main/model/Plant_Disease_Identifier.ipynb)**

## Solutions

#### System to detect the problem when it arises and warn the farmers.


#### Solution to overcome the problem once it arises.

Remedy is suggested for the disease detected by the app using ML model.

#### Solution that will ensure that the problem will never occur in the future again

PDF report is generated on the disease predicted along with User Information. PDF can be used as a document to be submitted in nearby Krishibhavan thereby seeking help easily.



## Machine Learning Model

Multi-Class Image classifier Built on PyTorch framework using CNN architecture. Currently Project Detects 17 States of disease in 4 plants ( Aiming Kerala State ) namely Cherry, Pepper, Potato and tomato.

* Framework : PyTorch
* Architecture : Convolutional Neural Networks
* Validation Accuracy : 77.7%



#### How to train

Upload the **[Python notebook](https://github.com/nandakishormpai2001/Plant_Disease_Detector/blob/main/model/Plant_Disease_Identifier.ipynb)** to Google Colab and run each cell for training the model. I have included a demo dataset **[Kaggle Dataset](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset)** 

#### How It Works

The input image dataset is converted to tensor and is passed through a CNN model, returning an output value corresponding to the plant disease. Input image tensor is passed through four convolutional layers and then flattened and inputted to fully connected layers.

## API

API is built using Flask framework and hosted in Render. The API provides two functionalities, they are

- Plant Disease Detection

    Accepts a POST request with an image in the form of base64 string and returns plant, disease and remedy.
    


#### How to use

API has been built on this classifier. URL = "https://susya.onrender.com"

User has to send a POST request to the given api with Base64 string of the Image to be input. 

```python
import requests
url = "https://susya.onrender.com"
#imgdata = base64 string of image
r = requests.post(url,json = {"image":imgdata})
print(r.text.strip())
```
Output
```python
'{"disease":"Septoria leaf spot","plant":"Tomato","remedy":"Remove infected leaves immediately,......Fungonil and Daconil)."}'
```




#### Features


- User Profile page
- Uses camera or device media to get an image of the crop
- Preview the image and sends it to API, for disease detection
- Result page showing detected disease and remedy
- Generates a PDF report to save/share predicted disease details
- Option to send the generated result as a notification warning to other users


## Tech Stack Used

- Python
- Flask
- PyTorch


