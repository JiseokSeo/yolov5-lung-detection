# yolov5-lung-detection
A repository that shares the weights of object detection of the lungs in chest X-ray images and guides you through their use.  
Weights was learned from the dataset from RSNA.  
Source and Permission information is located at the bottom of the repository.  

# Training Data
The dataset provided by the lowest permission information was obtained through the RSNA Pneumonia Detection Challenge of Kaggle.  
After sampling 200 images for each label in the trainset of the data provided, I labeled the lungs myself as a nurse.  
But I'm not a specialist in radiology, so you have to keep in mind that I can't be trusted academically.

After changing the DICOM format to a png format of (1024*1024) size, the lungs were labeled using the label-studio tool as shown below.  


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
