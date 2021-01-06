# **PyTorch Image Classifier**
Contacts: [g.nodjoumi@jacobs-university.de](mailto:g.nodjoumi@jacobs-university.de)

A simple image classifier demo-notebook based on resnet50, to be further developed and used to filter very large dataset before labeling for object detection / image segmentation

## **Dataset**
Dataset must be organized according the following structure:
- rootdir
    - class1
        - img1
        - img2
        - imgX 
        - ...
        
### **Example**     
**E.g. data provided and used for this notebook**
- ./Example_dataset
    - Background
        - ESP_011677_1655_RED_uint8_H0_V0__crop_H0_V1__cropped_cropped.png
        - ...
    - Craters
        - ESP_011386_2065_RED_uint8_H0_V0__crop_H0_V2__cropped_cropped.png
        - ...
    - Skylights
        - ESP_061680_1985_RED_print_H2_V0__crop_cropped.png
        - ...
        
## How it works

- All images are loaded and transformed
- All images indexes are splitted into three sub-dataset indexes
    - train (used for training)
    - valid (used for validate the training)
    - test (used to simulate real-world data)
- Data distributions for sub-datasets are shown in pie charts
- Train and valid indexes are used to load images and ingest into training routine
- Test index is used to load unseen data
- Test data are reandomly picked and predicted
