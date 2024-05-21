# FootballYOLOTrack
We utilize computer vision techniques OpenCV and YOLO object detection algorithm, to track various elements within a football game. 

### Dataset
  
  We get dataset from Kaggle which contains clips or eagle eye camera pointed view. 
  [Link](https://www.kaggle.com/competitions/dfl-bundesliga-data-shootout/data)

### Object Detection
  
  Object detection is a computer vision technique that involves identifying and locating objects within an image or video. It not only classifies objects into predefined categories but also determines their positions by drawing bounding boxes around them.

### YOLO

  YOLO, which stands for "You Only Look Once," is a state-of-the-art, real-time object detection system. Unlike traditional methods that repurpose classifiers or localizers to perform detection, YOLO frames object detection as a single regression problem, straight from image pixels to bounding box coordinates and class probabilities.

  Shortcomings -> Here we use YOLO to detect and classify players, ball and other with their probablities. Football is rarely getting detected due to it's size hence we need precision in that. Also, people outside of pitch like managers, side refs and coaches are also getting detected as well. For this shortcoming we use Roboflow dataset as it's provide with proper data, labels and annotations too.

### Roboflow

  Roboflow is a platform designed to streamline and simplify the process of building and deploying computer vision models. It provides tools for managing image datasets, annotating images, and training machine learning models for object detection, classification, and segmentation tasks. 
