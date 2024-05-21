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

### Tracking

  For tracking players in video frame we need some relevant data like direction of movement, color of jersey and etc. Hence we need to assign bounding box to players with ids. For this we're using Byte Tracker. 
  There is lot happening on pitch hence box annotations will override many events. Hence instead of rectangular bounding box we will draw ellipse around player. 
  Ball interpolation -> As size of ball is small it's not getting detected in all frames. To solve this random and improper detection we use interpolation. Interpolation that ball will always move in one direction and in straight line and we can find interpolation to missing value of ball.

### Assignment

  We use K-means clustering of pixel value in bounding box of one player. Hence it will contain only two values one of grass in background and one of his jersey color. Hence according to color we're assigning team to that player.

  ## Input

  <iframe src="https://drive.google.com/file/d/1ExCWSpHMPpDDboDgA50VZh14OoNyhKIY/preview" width="640" height="480" allow="autoplay"></iframe>
