# yolov5-lung-detection
A repository that shares YOLOv5 object detection weights for detecting lungs in chest X-ray images and provides guidance on their usage. I trained the weights on a dataset derived from the RSNA Pneumonia Detection Challenge. Please refer to the bottom of the repository for source and permission information.

# labeling  
I obtained the dataset, provided with the lowest permission information, through the RSNA Pneumonia Detection Challenge hosted on Kaggle. I sampled 200 images for each label (total 600) from the provided training set and annotated the lungs myself as a nurse. However, please note that the annotations may not be academically reliable, as I am not a radiology specialist.

I converted the DICOM format to a 1024x1024 PNG format and used the 'Label-Studio' tool to annotate the lungs as shown below. I marked the highest part of the upper lobe, the lowest part of the lower lobe, and the widest part of the lungs from side to side.  
<img width='30%' src='https://user-images.githubusercontent.com/103990167/228791194-9aa3775f-0ac7-4c9c-a6bf-380e90e0d04b.png'/>

# download weights
You can download the weights (lung_detection.pt) from the following link:
https://github.com/JiseokSeo/yolov5-lung-detection/releases  
Or you can check releases tab.

# how to use
This model is based on YOLOv5, so you should first clone the YOLOv5 repository:
https://github.com/ultralytics/yolov5.git  

```
$ git clone https://github.com/ultralytics/yolov5.git
```

Next, download the weights and place them in the recommended path:
```
…/yolov5/models/lung_detection.pt
```

You can now use the following command to perform lung detection. Refer to the YOLOv5 repository for more details:
```
$ cd .../yolov5
$ python detect.py --weight [weighs path] --source [object directory] --save-txt
```  

for example,
```
$ python detect.py --weight models/lung_detection.pt --source data/images --save-txt
```

This will generate result images and text files containing bounding box coordinates. The default output path is yolov5/run/detect/exp.

For more information on the various options supported by YOLOv5, see the YOLOv5 repository.

# result examples
<img width='100%' src='https://user-images.githubusercontent.com/103990167/228797350-a0df1839-8514-41ae-bca3-b4283776e2d3.png'/>  

# result-hard case
<img width='100%' src='https://user-images.githubusercontent.com/103990167/229259338-162b0939-ea48-45d1-b66e-ea908b670765.png'/>

---
For the NIH Chest X-ray Dataset from which the Pneumonia Detection Challenge datasets were drawn:  
• Provide a link to the NIH download site: https://nihcc.app.box.com/v/ChestXray-NIHCC  
• Include a citation to the CVPR 2017 paper:  
Xiaosong Wang, Yifan Peng, Le Lu, Zhiyong Lu, Mohammadhadi Bagheri, Ronald 
Summers, ChestX-ray8: Hospital-scale Chest X-ray Database and Benchmarks on 
Weakly-Supervised Classification and Localization of Common Thorax Diseases, 
IEEE CVPR, pp. 3462-3471, 2017
Acknowledge that the NIH Clinical Center is the data provider


For the RSNA-STR Pneumonia Detection Challenge image datasets and annotation files:  
• Provide a link to this download site:  
https://www.rsna.org/education/ai-resources-and-training/ai-image-challenge/RSNA-Pneumonia-Detection-Challenge-2018  
• Include a citation to the Radiology: AI 2019 paper:   
George Shih , Carol C. Wu, Safwan S. Halabi, Marc D. Kohli, Luciano M. Prevedello, 
Tessa S. Cook, Arjun Sharma, Judith K. Amorosa, Veronica Arteaga, Maya Galperin Aizenberg, Ritu R. Gill, Myrna C.B. Godoy, Stephen Hobbs, Jean Jeudy, Archana 
Laroia, Palmi N. Shah, Dharshan Vummidi, Kavitha Yaddanapudi, Anouk Stein, 
Augmenting the National Institutes of Health Chest Radiograph Dataset with Expert 
Annotations of Possible Pneumonia, Radiology: AI, January 30, 2019,
https://doi.org/10.1148/ryai.2019180041
