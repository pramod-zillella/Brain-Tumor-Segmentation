
# Brain-Tumor-Segmentation
![Predicted](https://user-images.githubusercontent.com/63542593/118610533-798cf800-b7d9-11eb-97d5-44df8de6fb91.png)
## Background
Surge in cancer cases globally have led to increase in computer aided diagnosis and research in biomedical imaging and diagnostic radiology. The task of manual segmentation is rigorous, time-consuming and accurate tumor segmentation depends on the expertise of the pathologist, incorrect segmentation will cause in recurrent brain cancer or long lasting side-effects. 

For accessing the interactive notebooks:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Pramod04121999/Brain-Tumor-Segmentation/HEAD)

## Introduction
Automatic brain tumor segmentation is one such task which will assist, improve doctors and radiologists accuracy in detecting and delineating the tumor sub-type. Automated brain tumor segmentation is highly desirable as it will help doctors learn about the prognostic factors and monitor the progression of the tumor and plan for treatment. For this we propose a method based on modified 3DUNet architecture which produced state-of-the-art segmentation results on the [Brats 2020](https://www.med.upenn.edu/cbica/brats2020/data.html) Challenge.

## Network Architecture
![Project-architecture](https://user-images.githubusercontent.com/63542593/118623303-bd85fa00-b7e5-11eb-8b5d-02c255860e4e.jpg)

## Loss Function



The proposed model uses Modified soft dice loss to optimize the loss function. Individual dice loss for the three labels (Enhancing tumor, Whole tumor, and Tumor core) are computed and added for the final dice loss, and the optimization is performed on the individual dice loss of the labels.

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118627620-831e5c00-b7e9-11eb-9dd6-483672dc303e.png" width="700">             
</p>

In the above equations, ![CodeCogsEqn (3)](https://user-images.githubusercontent.com/63542593/118631424-1c02a680-b7ed-11eb-9c62-db6334b783ac.png) indicates the 3x144x144x128 matrix of the ground truth annotation and ![CodeCogsEqn (4)](https://user-images.githubusercontent.com/63542593/118631431-1dcc6a00-b7ed-11eb-83d6-6244f2c24035.png) indicates the 3x144x144x128 matrix of the predicted segmentation output by the network and  \mathbit{\epsilon} indicates the smoothing factor which set to 1

### Quantitative Results
We calculate the proposed methods results using the statistical parameters-Dice Coefficient, Sensitivity, Specificity and Hausdorff Distance for Enhancing tumor, Whole tumor and Tumor core for the validation set. 

| Parameters  | Dice_ET | Dice_WT | Dice_TC | Sensitivity_ET | Sensitivity_WT | Sensitivity_TC | Specificity_ET | Specificity_WT | Specificity_TC | Hausdorff95_ET | Hausdorff95_WT | Hausdorff95_TC |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | 
| Mean  | 0.80661  | 0.89414  | 0.85721  | 0.81519  | 0.9251  | 0.84795  | 0.99971  | 0.99884  | 0.99953  | 23.1904  | 5.56554  | 5.44695  |
| StdDev  | 0.23953  | 0.08177  | 0.12749  | 0.25155  | 0.07596  | 0.16678  | 0.00043  | 0.00116  | 0.0007  | 85.62448  | 10.87704  | 9.90171  |
| Median  | 0.87871  | 0.91993  | 0.91058  | 0.89553  | 0.94956  | 0.90561  | 0.99985  | 0.99918  | 0.9998  | 1.73205 | 3.16228  | 3  |
| 25quantile  | 0.80214  | 0.87042  | 0.82128  | 0.82766  | 0.90596 | 0.81328  | 0.99957  | 0.99858  | 0.9995  | 1  | 2.23607  | 1.73205  |
| 75quantile  | 0.92648  | 0.94299  | 0.93417  | 0.94811  | 0.97373 | 0.95586  | 0.99996  | 0.99958  | 0.9999  | 3  | 5.47723  | 5.47723  |

### [Brats 2020 Challenge Leaderboard](https://www.cbica.upenn.edu/BraTS20/lboardValidation.html)

Team - Zillella 
### Visualization Results
         
#### Axial View 

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/a961d3f519d7e1e441f5b18c0ae59cb631467a54/Views/Axial.gif" width="700">
</p>
&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

         
#### Coronal View  

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/main/Views/Coronal.gif" width="700">
</p>
 &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

         
#### Sagittal View

<p align="center">
<img src="https://github.com/Pramod04121999/Brain-Tumor-Segmentation/blob/main/Views/Sagittal.gif" width="700">  
</p>        
&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         Brain MRI &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground Truth &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Predicted Tumor

(Region in green indicates the whole tumor, region in  blue indicates the enhancing tumor region and the region in red indicates the tumor core)

## Conclusion
With the proposed modified 3DUNet architecture state-of-the-art segmentation results for Enhancing tumor were obtained with approximatelty 1% improvement in dice coefficient when compared to the winners of Brats 2020 Challenge. The model is computationally very efficient taking less than 2 seconds to segment brain tumors from the whole brain MRI scan. 
