# Shapes Detection Using YOLOv8

### Task Description:
In this repository we will be using the popular Ultralytics YOLOv8 Object Detection model. We will be using the pretrained model on the Coco dataset and training it to recognize 2D Geometrical shapes on a custom (Dataset)[https://universe.roboflow.com/new-workspace-qsre9/geometry_shapes/dataset/1] found on Roboflow 



### Task Documentation:
-   Download the dataset from Roboflow. It contains 2,244 Images With 9 Classes
-   However the dataset is not split.
-   Running a custom python script, We quickly split the dataset into into 70,20,10 Split
-   Now we reupload the dataset into Roboflow. Roboflow Automatically detects our images and annotations and it splits them into a 70/20/10 split
-   Using Google Colab, Start a new notebook and upload the dataset to the google drive.

### Notebook Explanation

-   Install Ultralytics using `!pip install ultralytics`.
-   Unzip our file in colab using `!unzip /filepath/`
-   Start training our model using `!yolo task=detect mode=train data=/yaml file path/ epochs=80`
-   After the program is done training, we will be left with finished image detection model and some other helpful info

-   If we head into `runs/detect/train/` we will find a file called best.pt. This is our finished product that we can use to detect the coins.
-   There are also some `png` in `runs/detect/` with some info about our model's accuracy, recall, precision, etc.
