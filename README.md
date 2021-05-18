# Brain-Tumor-Segmentation

## Background
Surge in cancer cases globally have led to increase in computer aided diagnosis and research in biomedical imaging and diagnostic radiology. The task of manual segmentation is rigorous, time-consuming and accurate tumor segmentation depends on the expertise of the pathologist, incorrect segmentation will cause in recurrent brain cancer or long lasting side-effects. 


## Introduction
Automatic brain tumor segmentation is one such task which will assist, improve doctors and radiologists accuracy in detecting and delineating the tumor sub-type. Automated brain tumor segmentation is highly desirable as it will help doctors learn about the prognostic factors and monitor the progression of the tumor and plan for treatment. For this we propose a method based on modified 3DUNet architecture which produced state-of-the-art segmentation results on the Brats 2020 Challenge.

## Network Architecture
![Project-architecture](https://user-images.githubusercontent.com/63542593/118623303-bd85fa00-b7e5-11eb-8b5d-02c255860e4e.jpg)

## Loss Function

![CodeCogsEqn](https://user-images.githubusercontent.com/63542593/118626550-97ae2480-b7e8-11eb-8c46-f7895c245615.gif)

### Quantitative Results
We calculate the proposed methods results using the statistical parameters-Dice Coefficient, Sensitivity, Specificity and Hausdorff Distance for Enhancing tumor, Whole tumor and Tumor core for the validation set. 

![image](https://user-images.githubusercontent.com/63542593/118609800-bc9a9b80-b7d8-11eb-9b43-245898712667.png)
### Visualization Results
         
#### Axial View 

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/a961d3f519d7e1e441f5b18c0ae59cb631467a54/Views/Axial.gif" width="700">
</p>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

         
#### Coronal View  

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/main/Views/Coronal.gif" width="700">
</p>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

         
#### Sagittal View

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/main/Views/Sagittal.gif" width="700">  
</p>        
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

(Region in green indicates the whole tumor, region in  blue indicates the enhancing tumor region and the region in red indicates the tumor core)

![Predicted](https://user-images.githubusercontent.com/63542593/118610533-798cf800-b7d9-11eb-97d5-44df8de6fb91.png)
