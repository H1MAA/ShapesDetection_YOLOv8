# Shapes Detection Using YOLOv8

### Task Description:
In this repository we will be using the popular Ultralytics YOLOv8 Object Detection model. We will be using the pretrained model on the Coco dataset and training it to recognize 2D Geometrical shapes on a [custom dataset](https://universe.roboflow.com/new-workspace-qsre9/geometry_shapes/dataset/1) found on Roboflow 



### Task Documentation:
-   Download the dataset from Roboflow. It contains **2,244 Images With 9 Classes8**
-   However the dataset is **not split**.
-   Now we reupload the dataset into Roboflow. Roboflow Automatically detects our images and annotations and it splits them into a 70/20/10 split
-   Additionally, a **5% noise filter** is applied , doubling our dataset and including noise is a helpful data augmntation tactic in the context of drone cameras
-   Using Google Colab, Start a new notebook and upload the dataset to the google drive.


### [Link To my Google Drive](https://drive.google.com/drive/folders/1Prp1y9v7p-kV8tcZbUFFVlCJ6Hs4p18O?usp=drive_link) containing the updated dataset and weights 

### Notebook Explanation

-   Install Ultralytics using `!pip install ultralytics`.
-   Unzip our file in colab using `!unzip /filepath/`
-   Start training our model using `!yolo task=detect mode=train data=path_to_data/yaml_file.yaml epochs=80 imgsz=640`
-   After the program is done training, we will be left with the updated weights and some other helpful info
-   Using the new weights file and the ultralytics library, we can then predict some shapes from images on the internet
