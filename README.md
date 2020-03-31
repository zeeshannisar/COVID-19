# Detecting COVID-19 in X-ray Images Using Different Pretrained-Networks in Tensorflow 2.x.
The Corona Virus Disease 2019 (COVID-19) pandemic continues to have an upsetting effect on the health and well-being of the global population. A critical step in the fight against COVID-19 is effective screening of infected patients, with one of the key screening approaches being radiological imaging using chest radiography. It was found in early studies that patients present abnormalities in chest radiography images that are characteristic of those infected with COVID-19 as discussed in a recent [[Paper]](https://arxiv.org/abs/2003.09871). Therefore, in this Repository I have tested different Pretrained Networks for the detection of COVID-19 cases from chest radiography images that is open source and available to the general public. **Finally a Novel Method will be introduced to get the maximum of Positive Predicted Values from these Pretrained Networks.**

## Table of Contents
  + [Datset Description](#dataset-description)
    + [Dataset 01](#dataset-01)
    + [Dataset 02](#dataset-02)
  + [Pretrained Networks for COVID-19 Detection](#pretrained-networks-for-covid-19-detection)
    + [VGG19]
    + [AlexNet]
    + [Inception V3]
    + [ResNet-18]
    + [DenseNet-121]
    + [Google-Net]
  + [Visualization of Infectious Regions]
  
### Dataset Description:
#### Dataset 01:
[Dataset 01](https://drive.google.com/drive/folders/1wHtxo0O0uZMZ-A71pK1PVRnC3hOvIF14?usp=sharing) is the first version introduced by the authors of the [[Paper]](https://arxiv.org/abs/2003.09871). This dataset is comprised of a total of 5949 posetrior chest radiography images across 2839 patients. I have write a python script to categorize each X-ray image in the raw data folder to a separate Class as per corresponding label. The original data distribution was

| Category    | Number of Patients | Number of X-rays |
| --------    | ------------------ | ---------------- |
| 0: Normal   | 1203               | 1583             |
| 1: Bacteria | 931                | 2786             |
| 2: Viral    | 660                | 1504             |
| 3: COVID-19 | 45                 | 76               |

I have split the original data to train/test folders with following distrubtuions. This categorized dataset can be downloaded at [Here](https://drive.google.com/drive/folders/1wHtxo0O0uZMZ-A71pK1PVRnC3hOvIF14?usp=sharing). I have also write a python [Script]() to make the NumpyFiles for the train/test images but without any normalization so that one can normalize the data as per his/her need. These NumpyFiles can also be accessed at [Here](https://drive.google.com/drive/folders/1zpwOSHDtdSuGFHB9MosBK6EdyPfQp2Hv?usp=sharing).

| Category    | train | test |
| --------    | ----- | ---- |
| 0: Normal   | 1349  | 234  |
| 1: Bacteria | 2540  | 246  |
| 2: Viral    | 1355  | 149  |
| 3: COVID-19 | 66    | 10   |

#### Dataset 02: 
[In Process and will be shared soon]()


### Pretrained Networks for COVID-19 Detection:
The core idea behind the Pretrained Networks and Transfer Learning can be studied in detail at my another GitHubRepository at [Here](https://github.com/zeeshannisar/Transfer-Learning-and-Fine-Tuning-with-Pre-Trained-Networks).
