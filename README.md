
#Solar Panel Anomaly Detection and Shading Classification

#Overview

This repository focuses on detecting anomalies (specifically Hotspot-Single Bypassed) on solar panels and classifying shading patterns using machine learning models. The pipeline involves data preprocessing, augmentation, model training, and deployment on Roboflow and Ucloud platform and LightningAI.

#Datasets
The datasetets consist of RGB images captured by a drone . 

#Methodology
Preprocessing and Augmentation:(Preprocessing.ipynb)

A dataset for shading on PV solar panels was downloaded and processed.
Augmentation techniques were applied to enhance dataset diversity.
Model Training:

A supervised model, trained using Roboflow MDS COCO, was used for annotating shading classes on a dataset for anomaly detection.
This model annotates predicted shading classes found in another labeled dataset, which is also preprocessed and augmented.
Anomaly Detection:

The final dataset, incorporating both shading and anomaly classes (Hotspot-Single Bypassed), was prepared using Ucloud platform.(PVdataset.ipynb)
Model Details
Type: YOLOv10m trained on an A10G GPU using Lightning AI platform.
Training Insights: Metrics and training/validation logs are available at https://6006-01j0ypcxp6s35bxagy60bt6xh6.cloudspaces.litng.ai .(runs/detect/train2)

Challenges and Considerations
Shading Classification Accuracy: Initial training on the final dataset showed poor accuracy on shading classes, suggesting a need for synthetic data generation.
Sensor Considerations: Considering alternative sensors like electroluminescence and thermal imaging for improved anomaly detection effectiveness.
Anomaly Classification Difficulty: Anomalies are challenging to classify due to varying environmental conditions; efforts are ongoing to classify them effectively for robotic maintenance.




Future Steps
Investigate the effectiveness of electroluminescence and thermal imaging alongside RGB for anomaly detection.
Explore methods to improve shading class accuracy, potentially through synthetic data generation.
Enhance anomaly classification to facilitate targeted maintenance by ground robots.








