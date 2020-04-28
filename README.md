# Detecting and Visualising the Infectious Regions of COVID-19 in X-ray Images Using Different Pretrained-Networks in Tensorflow 2.x.
The Corona Virus Disease 2019 (COVID-19) pandemic continues to have an upsetting effect on the health and well-being of the global population. A critical step in the fight against COVID-19 is effective screening of infected patients, with one of the key screening approaches being radiological imaging using chest radiography. It was found in early studies that patients present abnormalities in chest radiography images that are characteristic of those infected with COVID-19 as discussed in a recent [[Paper]](https://arxiv.org/abs/2003.09871). Therefore, in this Repository I have tested different Pretrained Networks for the detection of COVID-19 cases from chest radiography images that is open source and available to the general public. **Finally a Novel Method will be introduced to get the maximum of Positive Predicted Values from these Pretrained Networks.**

## Table of Contents
  + [Datset Description](#dataset-description)
    + [Dataset 01](#dataset-01)
    + [Dataset 02](#dataset-02)
  + [Pretrained Networks for COVID-19 Detection and Visualization of Infectious Regions](#pretrained-networks-for-covid-19-detection)
    + [VGG-16](#vgg-16)
    + [VGG-19](#vgg-19)
    + [DenseNet-121](#densenet-121)
    
### Dataset Description:
#### Dataset 01:
[Dataset 01](https://drive.google.com/drive/folders/1wHtxo0O0uZMZ-A71pK1PVRnC3hOvIF14?usp=sharing) is the first version introduced by the authors of the [[Paper]](https://arxiv.org/abs/2003.09871). This dataset is comprised of a total of 5949 posetrior chest radiography images across 2839 patients. I have write a python script to categorize each X-ray image in the raw data folder to a separate Class as per corresponding label. The original data distribution was

| Category    | Number of Patients | Number of X-rays |
| ----------  | -------------      | -------------    |
| 0: Normal   | 1203               | 1583             |
| 1: Bacteria | 931                | 2786             |
| 2: Viral    | 660                | 1504             |
| 3: COVID-19 | 45                 | 76               |

I have split the original data to train/test folders with following distrubtuions. This categorized dataset can be downloaded at [Here](https://drive.google.com/drive/folders/1wHtxo0O0uZMZ-A71pK1PVRnC3hOvIF14?usp=sharing). I have also write a python [Script](https://github.com/zeeshannisar/COVID-19/blob/master/datasets/Read%20Dataset%20and%20Make%20Numpy%20Files.ipynb) to make the NumpyFiles for the train/test images but without any normalization so that one can normalize the data as per his/her need. These NumpyFiles can also be accessed at [Here](https://drive.google.com/drive/folders/1zpwOSHDtdSuGFHB9MosBK6EdyPfQp2Hv?usp=sharing).

| Category    | Train | Test |
| ----------  | ----- | ---- |
| 0: Normal   | 1349  | 234  |
| 1: Bacteria | 2540  | 246  |
| 2: Viral    | 1355  | 149  |
| 3: COVID-19 | 66    | 10   |

#### Dataset 02: 
[Dataset 02](https://drive.google.com/drive/folders/1NLjyns6qJcQE8zZ8OZ-xfNMatcLLnMJO?usp=sharing) is the second version introduced by the authors of the [[Paper]](https://arxiv.org/abs/2003.09871). One can follow the steps given [Here](https://github.com/lindawangg/COVID-Net/blob/master/docs/COVIDx.md) to generate this dataset. The NumpyFiles for this data can also be accessed at [Here](https://drive.google.com/drive/folders/1NLjyns6qJcQE8zZ8OZ-xfNMatcLLnMJO?usp=sharing). The distribution of these Numpy files are as followed.

| Category    | Train | Test |
| ----------  | ----- | ---- |
| 0: Normal   | 8751  | 100  |
| 1: Pneumonia | 5936  | 100  |
| 2: COVID-19 | 92    | 10   |

### Pretrained Networks for COVID-19 Detection:
The core idea behind the Pretrained Networks and Transfer Learning can be studied in detail at my another GitHubRepository at [Here](https://github.com/zeeshannisar/Transfer-Learning-and-Fine-Tuning-with-Pre-Trained-Networks). I have used the following Pretrained Networks for COVID-19 Detection. Each Pretrained Network is also described with its train/test History and a Confusion-Matrix for better visualization of the Generalization of the Trained Network.

#### VGG-16:
[Code: Google Colab Notebook](https://github.com/zeeshannisar/COVID-19/blob/master/Vgg16-Transfer%20Learning-COVID19.ipynb)


##### Statistical Results:

|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Accuracy/VGG16-Accuracy-Graph.png "Accuracy") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Loss/VGG16-loss-Graph.png "Loss") |
|:---:|:---:|
| Pretrained-VGG16 Accuracy-Graph | Pretrained-VGG16 Loss-Graph |


|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG16-cm.png "Confusion Matrix") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG16-roc.png "ROC Curve") |
|:---:|:---:|
| Pretrained-VGG16 Confusion Matrix | Pretrained-VGG16 ROC |

##### Visualization:
<p align="center">
    <img src="https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG16-visualization.png", width=55%, height=55%>
</p>


#### VGG-19:

##### Implementation:
[Code: Google Colab Notebook](https://github.com/zeeshannisar/COVID-19/blob/master/Vgg19-Transfer%20Learning-COVID19.ipynb)


##### Statistical Results:

|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Accuracy/VGG19-Accuracy-Graph.png "Accuracy") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Loss/VGG19-loss-Graph.png "Loss") |
|:---:|:---:|
| Pretrained-VGG19 Accuracy-Graph | Pretrained-VGG19 Loss-Graph |


|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG19-cm.png "Confusion Matrix") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG19-roc.png "ROC Curve") |
|:---:|:---:|
| Pretrained-VGG19 Confusion Matrix | Pretrained-VGG19 ROC |

##### Visualization:
<p align="center">
    <img src="https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/VGG19-visualization.png", width=55%, height=55%>
</p>


#### DenseNet-121:
[Code: Google Colab Notebook](https://github.com/zeeshannisar/COVID-19/blob/master/DenseNet121-Transfer%20Learning-COVID19.ipynb)


##### Statistical Results:

|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Accuracy/DenseNet121-Accuracy-Graph.png "Accuracy") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Loss/DenseNet121-loss-Graph.png "Loss") |
|:---:|:---:|
| Pretrained-DenseNet121 Accuracy-Graph | Pretrained-DenseNet121 Loss-Graph |

|![alt-text-1](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/DenseNet121-cm.png "Confusion Matrix") | ![alt-text-2](https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/DenseNet121-roc.png "ROC Curve") |
|:---:|:---:|
| Pretrained-DenseNet121 Confusion Matrix | Pretrained-DenseNet121 ROC |

##### Visualization:
<p align="center">
    <img src="https://github.com/zeeshannisar/COVID-19/blob/master/ReadMe%20Images/DenseNet121-visualization-0.png", width=55%, height=55%>
</p>

