# Covid19-Face-Mask-Detection
### Goal: To create a face mask detector using Deep Learning and Computer Vision techniques.

### Libraries used: 
Tensorflow, Keras, VGG16, OpenCV, Haar Cascade Classifier. 

### About the Data set: 
The data set is downloaded from [Kaggle](https://www.kaggle.com/niharika41298/withwithout-mask). 
There are two folders, maskdata contains more images and masks2.0 contains a smaller number of images.
The dataset has images of both original and artificially created.
Artificially, images were created by:

1. Taking normal images of faces
2. Then creating a custom computer vision Python script to add face masks to them, thereby creating an artificial 
(but still real-world applicable) dataset.

The folders are further divided into train and test data, which are further divided in categories- with mask and without mask.
I have used the mask2.0 for validating the model as it is an unseen data for the model.

### Project Description:
1. Initially, I have combined all the images of the test data with the train data and I have used the train data folder only for traning the VGG16 model.
I did this step because I wanted to increase the number of images of both with and without mask for training the model in order to increase the accuracy.
Later, I have created a train test split taking 80% as the training data and 20% as test data.

2. In the data pre-processing step, the input path was set, images were loaded, read, resized and then categories and class were stored to a list. The list was shuffled
to reduce bias, seperated into labels and classes, and then converted into arrays. Then train test split was performed. 

3. Then, the VGG16 model was built by removing the final layer, trained on imagenet weights and tested.

4. Finally, the face mask detection model was built by combining three functions: one for detecting face mask that uses the 
VGG16 model, second, for displaying the text "Mask" or "No mask" and the third for detecting the face using Haar Cascade Classifier.

### Demo:

![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/75041273/137604890-d25b6691-326d-4f6f-b90f-6e57ddeaf357.gif)

### Installation:
The Code is written in Python 3.7.3 If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:

##### 1. First create a virtual environment by using this command:
```bash
conda create -n myenv python=3.7
```
##### 2. Activate the environment using the below command:
```bash
conda activate myenv
```
##### 3. Then install all the packages by using the following command
```bash
pip install -r requirements.txt
```
##### 4. Open the .ipynb file inside Jupyter Notebook and run the cells.

##### Make sure to change the directory to the root folder. The folder structure should be same as of this repository otherwise it will throw error. 

 
