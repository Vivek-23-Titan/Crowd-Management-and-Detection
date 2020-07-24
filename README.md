# Crowd-Management-and-Detection
The purpose of this repo is to improve the crowd density classification scores and detection/estimate in crowded places such as the number of commutators inside a bus.
## Dataset
The dataset consists of 1200 images, out of which 900 are used for training and remaining 300 for testing purpose.
The dataset is divided into 5 different classes namely, Very Low, Low, Moderate, High and Very High crowd density levels.
## Results
The results of the training history and confusion matrices are shown below.

### Training History
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Training_Curve_98.47.PNG" width=400>

### Training Data Confusion Matrix
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_train.PNG" width=400>

### Testing Data Confusion Matrix (f1-scores)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_99.13.PNG" width=400>
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/f1_score_99.13.PNG" width=400>

## Crowd Detection
For the purpose of person detection, YOLOv4 has been emplyed.

### Results (In the increasing order of population density)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_3.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Moderate.jpg" width=500> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/High.jpg" width=500> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Very_High.jpg" width=500>
