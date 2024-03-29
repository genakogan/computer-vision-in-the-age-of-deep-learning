# <div align="center"><center>Computer Vision In The Age Of DeepLearning</div>
## HW1
### Description
  In this project we use the Neighbor Nearest-k algorithm to classify images of letters from the 0_HHD database, which consists of handwritten Hebrew letters.<br />
  The program will execute the following steps:<br />
1.	The program will read the data into a dict variable structure, each “key” will represent the letter and the “value” will contain a “list” of images of that specific letter.<br />
2. Pre-processing step will “grayscale”  each image, we will pad each image with white borders and make it squared, after that we will resize the image to 32x32<br />
3. We will split the data randomly but equally distributed to three categories: Train, Validation and Test. With the sizes of 80% : 10% : 10% accordingly.<br />
4. We will use sklearn library for the KNN model and use it with “Euclidean distance” metric. The model will train on the “train” set, afterwards we will try to evaluate the model with the “validation” set and find the best K ( in range 1 to 15 with steps of 2) that provides the highest accuracy.<br />
5. We will save the  best model, accuracy and the processed data into a “pickle” file to shorten the progress in case we would like  to run the program again.<br />
6. The best saved KNN model could be loaded, now we can fit the “test” set and report the results.<br />
7. We will generate a “result.txt” file that will contain: <br />
o	Best K value<br />
o	The accuracy of each letter.<br /><br />
8. We will also provide a confusion matrix, that will be saved on scv file.<br />

### Requirements
  1. opencv-python<br />
  2. pandas<br />
  3. sklearn<br />
  4. matplotlib<br />
  5. seaborn<br />
  If you are managing Python packages (libraries) with pip, you can use the configuration file req.txt to install the specified packages with the specified version.<br />

### How to Run Your Program (Windows)
1. Open the Cmd, type the following command and press the enter button as shown in the below:<br />
```pip install virtualenv```<br />
2. Create a new virtual environment inside that project's directory to avoid unnecessary issues:<br />
```py -m venv env```<br />
  For more details about virtual environment, please follow the link below:<br />
  <a href="https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/" target="_blank">Virtual Environment</a><br />
3. To use this newly created virtual environment, we just need to activate it. To activate this isolated environment, type the following given command and press enter button as shown below:<br />
```.\env\Scripts\activate```<br />
4. A requirement.txt files include all types of the standard packages and libraries that are used in that particular project. To install all requirements type the following command and press the enter:<br />
```pip install -r HW2022\HW1\req1.txt```<br />
5. The program will be executed from the command line by next command:<br />
```python HW2022\HW1\knn_classifier.py .\HW2022\hhd_dataset```<br />
6. For leaving the virtual environment type the following given command and press enter button as shown below:
  ```deactivate```
### 	References
  1. Rouse, Margaret (September 2005). "What is aspect ratio?". WhatIs?. TechTarget. Retrieved 3 February 2013.
  2. Rouse, Margaret (September 2002). "Wide aspect ratio display". display. E3displays. Retrieved 18 February 2020.
  3. Smith, W. D., & Wormald, N. C. (1998, November). Geometric separator theorems and applications. In Proceedings 39th Annual Symposium on Foundations of Computer Science (Cat. No. 98CB36280) (pp. 232-243). IEEE.
  4. Hastie T., Tibshirani R., Friedman J. The Elements of Statistical Learning. — Springer, 2001.
  
## HW2
In this project, we use the Feedforward neural network to classify images of letters from the 0_HHD database, which consists of handwritten Hebrew letters.<br />
### Model configuration
Dropout: 0.5, Regularization L2: 0.01.
### Model accuracy
0.77<br />
### Requirements
  1. opencv-python<br />
  2. pandas<br />
  3. sklearn<br />
  4. matplotlib<br />
  5. seaborn<br />
  6. tensorflow <br />
### How to Run Your Program (Windows) 
1. ```pip install virtualenv```<br />
2. ```py -m venv env```<br />
3. ```.\env\Scripts\activate```<br />
4. ```pip install -r HW2022\HW2\req2.txt```<br />
5. ```python HW2022\HW2\nn_classifier.py .\HW2022\hhd_dataset```<br />
6. ```deactivate```
