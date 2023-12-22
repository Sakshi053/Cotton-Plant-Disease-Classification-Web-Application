# Cotton Plant Disease Classification Web Application :herb:
This repository is about an end to end implementation of deep learning cotton plant disease classification web application using flask. 

## Dataset
The dataset is downloaded from [Kaggle](https://www.kaggle.com/janmejaybhoi/cotton-disease-dataset). and total size is 152 MB. The dataset contains 3 folders with 1951 train images, 106 test images and 253 validation images. Each folder is divided into four classes: diseased cotton plant (Fusarium Wilt), diseased cotton leaf (Leaf Curl Disease), fresh cotton plant (Healthy Plant) and fresh cotton leaf (Healthy Leaf). Each image has a size of 694x694 pixels in JPG format.
Here are the sample images of the dataset...  

<img src="https://github.com/myatmyintzuthin/Cotton-Plant-Disease-Classification-Web-Application/blob/main/assets/SampleImagesfromDataset.png" width=50% height=50%>

## DenseNet Model
Pretrained DenseNet121 model on ImageNet dataset is used. With the help of transfer learning, the last 8 layers of the model are tuned to solve the problem. The model is trained for 20 epoches and the accuracy is 97% on test data. 

<img src="https://i.imgur.com/O8ntGzS.png">

## Training Accuracy and Loss
<img src="https://github.com/myatmyintzuthin/Cotton-Plant-Disease-Classification-Web-Application/blob/main/assets/DenseNet121_plot.png">

## Confusion Matrix
<img src="https://github.com/myatmyintzuthin/Cotton-Plant-Disease-Classification-Web-Application/blob/main/assets/DenseNetConfusionMatrix.png" width=50% height=50%>

## Demo
<img src="https://github.com/myatmyintzuthin/Cotton-Plant-Disease-Classification-Web-Application/blob/main/assets/WebApplicationSample.png"  width=70% height=70%>

## Usage
- For model implementation and training, run [densenet121cottondisease.ipynb](https://github.com/Sakshi053/Cotton-Plant-Disease-Classification-Web-Application/blob/main/densenet121cottondisease.ipynb).
- You can also directly download [DenseNet121.h5](https://github.com/Sakshi053/Cotton-Plant-Disease-Classification-Web-Application/blob/main/DenseNet121.h5) without running the notebook.
- To run Flask app, run [app.py](https://github.com/Sakshi053/Cotton-Plant-Disease-Classification-Web-Application/blob/main/app.py).
- Make sure that you did not change any folder name in this repo.

## Cmds to run file
- Installing dependencies
```
pip install -r requirements.txt
```

- Model Training  
```
densenet121cottondisease.ipynb
```

- Inference

Model weight available at -  [DenseNet121.h5](https://github.com/Sakshi053/Cotton-Plant-Disease-Classification-Web-Application/blob/main/DenseNet121.h5) and store inside `/model` folder.

To run Flask, use:
```
python app.py
```

## Docker cmds
To build docker image, run:
```
docker build -t cotton .
```

Run docker image, using:
```
docker run --name cotton-app cotton
``` 

Stop docker, using:
```
docker stop cotton-app
```

## Credits
Thanks to my teammates [Myat Myint Zu Thin](https://github.com/myatmyintzuthin) and [Prachi Gupta](https://github.com/Prachigupta0305)
