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

<table>
  <tr>
    <th style="text-align:center"> Category </th>
    <th style="text-align:center"> Number of Patients </th>
    <th style="text-align:center"> Number of X-rays </th>
  </tr>
  <tr>
    <td style="text-align:center"> 0: Normal </td>
    <td style="text-align:center"> 1203 </td>
    <td style="text-align:center"> 1583  </td>
  </tr>
  <tr>
    <td style="text-align:center"> 1: Bacteria </td>
    <td style="text-align:center"> 931 </td>
    <td style="text-align:center"> 2786 </td>
  </tr>
  <tr>
    <td style="text-align:center"> 2: Viral </td>
    <td style="text-align:center"> 660 </td>
    <td style="text-align:center"> 1504 </td>
  </tr>
  <tr>
    <td style="text-align:center"> 3: COVID-19 </td>
    <td style="text-align:center"> 45 </td>
    <td style="text-align:center"> 76 </td>
  </tr>
</table>
  

I have split the original data to train/test folders with following distrubtuions. This categorized dataset can be downloaded at [Here](https://drive.google.com/drive/folders/1wHtxo0O0uZMZ-A71pK1PVRnC3hOvIF14?usp=sharing). I have also write a python [Script](https://github.com/zeeshannisar/COVID-19/blob/master/datasets/Read%20Dataset%20and%20Make%20Numpy%20Files.ipynb) to make the NumpyFiles for the train/test images but without any normalization so that one can normalize the data as per his/her need. These NumpyFiles can also be accessed at [Here](https://drive.google.com/drive/folders/1zpwOSHDtdSuGFHB9MosBK6EdyPfQp2Hv?usp=sharing).

<table align="center">
  <tr>
    <th style="text-align:center"> Category </th>
    <th style="text-align:center"> train </th>
    <th style="text-align:center"> test </th>
  </tr>
  <tr>
    <td style="text-align:center"> 0: Normal </td>
    <td style="text-align:center"> 1349 </td>
    <td style="text-align:center"> 234 </td>
  </tr>
  <tr>
    <td style="text-align:center"> 1: Bacteria </td>
    <td style="text-align:center"> 2540 </td>
    <td style="text-align:center"> 246 </td>
  </tr>
  <tr>
    <td style="text-align:center"> 2: Viral </td>
    <td style="text-align:center"> 1355 </td>
    <td style="text-align:center"> 149 </td>
  </tr>
  <tr>
    <td style="text-align:center"> 3: COVID-19 </td>
    <td style="text-align:center"> 66 </td>
    <td style="text-align:center"> 10 </td>
  </tr>
</table>



#### Dataset 02: 
[In Process and will be shared soon]()


### Pretrained Networks for COVID-19 Detection:
The core idea behind the Pretrained Networks and Transfer Learning can be studied in detail at my another GitHubRepository at [Here](https://github.com/zeeshannisar/Transfer-Learning-and-Fine-Tuning-with-Pre-Trained-Networks). I have used the following Pretrained Networks for COVID-19 Detection. Each Pretrained Network is also described with its train/test History and a Confusion-Matrix for better visualization of the Generalization of the Trained Network.

#### VGG-16:

#### VGG-19:
<table align="center">
  <tr>
    <td> 
      <img src="https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Accuracy/VGG19-Accuracy-Graph.png"
           alt="Drawing" style="width: 250px;"/>
    </td>
    <td> 
      <img src="https://github.com/zeeshannisar/COVID-19/blob/master/Train-Test%20History/Loss/VGG19-loss-Graph.png" alt="Drawing"
           style="width: 250px;"/>
    </td>
  </tr>
</table>



