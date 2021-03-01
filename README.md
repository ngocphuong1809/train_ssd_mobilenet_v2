# train_ssd_mobilenet_v2
How to train a Custom Model for Object Detection 
Step 1. Download the full TensorFlow object detection repository located at https://github.com/tensorflow/models

Step 2. Download and extract SSD-MobileNet model you want to train in Tensorflow model zoo 

Step 3. Everything needed for trainning at folder models\research\object_detection 
  - Train and test images and their XML label files are placed in the \object_detection\images\train and \object_detection\images\test folders
  - train_labels.csv and test_labels.csv have been generated and are located in the \object_detection\images folder
  - train.record and test.record have been generated and are located in the \object_detection folder
  - labelmap.pbtxt file has been created and is located in the \object_detection\training folder
  - proto files in \object_detection\protos have been generated
  
  Copy file .config from the \object_detection\samples\configs folder to the \object_detection\training folder and make change
  - Change num_classes to the number of different objects you want the classifier to detect. 
  - Change batch_size The smaller batch size will prevent OOM (Out of Memory) errors during training.
  - Change fine_tune_checkpoint,  input_path, label_map_path 
  - Change num_examples to the number of images you have in the \images\test directory.
  
And then train on Google Colab with file .ipynb
