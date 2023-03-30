# yolov5-lung-detection
A repository that shares the weights of object detection of the lungs in chest X-ray images and guides you through their use.  
Weights was learned from the dataset from RSNA.  
Source and Permission information is located at the bottom of the repository.  

# labeling  
The dataset provided by the lowest permission information was obtained through the RSNA Pneumonia Detection Challenge of Kaggle.  
After sampling 200 images for each label in the trainset of the data provided, I labeled the lungs as a nurse.  
But I'm not a specialist in radiology, so you have to keep in mind that I can't be trusted academically.

After changing the DICOM format to a png format of (1024*1024) size, the lungs were labeled using the 'Label-Studio' tool as shown below.  
I checked the highest part of the upper lobe, the lowest part of the lower lobe, and the widest part of the lungs from side to side.  
<img width='30%' src='https://user-images.githubusercontent.com/103990167/228791194-9aa3775f-0ac7-4c9c-a6bf-380e90e0d04b.png'/>

# download weights
You can download weights(lung_detection.pt) from the link below.  
https://drive.google.com/file/d/1-7Lyt3SDAUUt1acR9DeiLHPoCTk9ZOJI/view?usp=share_link

# how to use
This weight was trained through YOLOv5, so you should clone the repository below.  
https://github.com/ultralytics/yolov5.git  

```
$ git clone https://github.com/ultralytics/yolov5.git
```

Download the weights.  
The recommended paths are as follows.  
```
…/yolov5/models/lung_detection.pt
```

You can use the following commands to perform lung detection.  
See the yolov5 repository for more information.  
```
$ cd .../yolov5
$ python detect.py --weight [weighs path] --source [object directory] --save-txt
```

The result image and txt with bounding box coordinates are generated.  
The default path is run/detect/exp.  

For more information about the various options that yolov5 supports, see the yolov5 repository.  

# result examples
<img width='100%' src='https://user-images.githubusercontent.com/103990167/228797350-a0df1839-8514-41ae-bca3-b4283776e2d3.png'/>

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
