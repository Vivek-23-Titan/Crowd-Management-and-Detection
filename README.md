# Crowd-Management-and-Detection
The purpose of this repository is to improve the crowd density classification scores and detect/estimate number of people in crowded places such as commutators traveling via bus.
## Dataset
The dataset consists of a total of 6000 images i.e., 1200 images per class, out of which for each class 900 are used for training and remaining 300 for testing purpose.
The dataset is divided into 5 different classes namely, Very Low, Low, Moderate, High and Very High crowd density levels.
## Code
The Code is available in the Jupyter Notebook format. There are 2 different notebooks provided:
* Crowd density classification <a href="https://colab.research.google.com/github/Vivek-23-Titan/Crowd-Management-and-Detection/blob/master/Xception_Crowd_Control.ipynb" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
* People detection <a href="https://colab.research.google.com/github/Vivek-23-Titan/Person_Detection_in_Crowd_YOLOv4.ipynb" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

## Results
The results of the training history and confusion matrices are shown below.

### Training History
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Training_Curve_98.47.PNG" width=400>

### Confusion Matrix of Testing (f1-scores; 99.13% accuracy) and Training Data respectively
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_99.13.PNG" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Confusion_Matrix_train.PNG" width=400>
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/f1_score_99.13.PNG" width=400>

* The obtained performance is a 6% improvement with 99.13% as overall accuracy as opposed to 93.09% [IEEE Paper](https://ieeexplore.ieee.org/document/9155692).

## Person Detection in Crowd
For the purpose of person detection, pre-trained [pytorch](https://github.com/WongKinYiu/PyTorch_YOLOv4) version of YOLOv4 has been emplyed.

### Results (In increasing order of population density)
#### Class 0: Very Low (3 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryLow_0.2_3.jpg" width=400>
#### Class 1: Low (11 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Low_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Low_0.2_11.jpg" width=400>
#### Class 2: Moderate (20 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Moderate_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/Moderate_0.2_20.jpg" width=400>
#### Class 3: High (23 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/High_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/High_0.2_23.jpg" width=400>
#### Class 4: Very High (18 detections)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryHigh_0.2_og.jpg" width=400> <img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/VeryHigh_0.2_18.jpg" width=400>
* Notice that the Very High class consists of **severely occluded individuals** and hence making person detection difficult. Therefore, person detection in this senario does not yield the desired results and thus this class is only defined by classification results.

#### Box Plot (Classes in increasing order on X-axis and People detected on Y-axis)
<img src="https://raw.githubusercontent.com/Vivek-23-Titan/Crowd-Management-and-Detection/master/images/Images/BoxPlot.png" width=400>

## Citation
```
@article{bochkovskiy2020yolov4,
  title={{YOLOv4}: Optimal Speed and Accuracy of Object Detection},
  author={Bochkovskiy, Alexey and Wang, Chien-Yao and Liao, Hong-Yuan Mark},
  journal={arXiv preprint arXiv:2004.10934},
  year={2020}
}

@INPROCEEDINGS{9155692, 
  author={A. V. {Meghana} and V. {Sarode} and D. {Tambade} and A. {Marathe} and N. {Charniya}},
  booktitle={2020 International Conference on Electronics and Sustainable Communication Systems (ICESC)},
  title={Automated Crowd Management in Bus Transport Service},
  year={2020},
  volume={},  number={},  pages={104-109},
}
```
## Acknowledgements
* https://github.com/WongKinYiu/PyTorch_YOLOv4
* https://www.tensorflow.org/guide/keras/transfer_learning
