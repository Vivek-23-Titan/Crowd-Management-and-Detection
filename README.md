# Crowd-Management-and-Detection
The purpose of this repo is to improve the crowd density classification scores and detect/estimate number of people in crowded places such as commutators traveling via bus.
## Dataset
The dataset consists of 1200 images, out of which 900 are used for training and remaining 300 for testing purpose.
The dataset is divided into 5 different classes namely, Very Low, Low, Moderate, High and Very High crowd density levels.
## Results
The results of the training history and confusion matrices are shown below.

### Training History
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Training_Curve_98.47.PNG" width=400>

### Confusion Matrix of Testing (f1-scores) and Training Data respectively
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_99.13.PNG" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_train.PNG" width=400>
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/f1_score_99.13.PNG" width=400>

## Person Detection in Crowd
For the purpose of person detection, pre-trained pytorch version of YOLOv4 (source: https://github.com/WongKinYiu/PyTorch_YOLOv4) has been emplyed.

### Results (In increasing order of population density)
#### Very Low (3 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_3.jpg" width=400>
#### Low (11 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Low_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Low_0.2_11.jpg" width=400>
#### Moderate (20 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Moderate_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Moderate_0.2_20.jpg" width=400>
#### High (23 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/High_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/High_0.2_23.jpg" width=400>
#### Very High (18 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryHigh_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryHigh_0.2_18.jpg" width=400>
* Notice that the Very High class consists of severely occluded individuals and hence making person detection difficult. Therefore, person detection in this senario does not yield the desired results and thus this class is only defined by classification results.
