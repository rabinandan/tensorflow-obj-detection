This implementation is based up on below resources:

 #https://www.edureka.co/blog/tensorflow-object-detection-tutorial/
 #https://www.mygreatlearning.com/blog/object-detection-using-tensorflow/
 
 
 Objective:
 ...........
    
      To detection an object inside a image frame.
      
 Cloning and getting code
 ......
 Clone/download tensorflow models from here: https://github.com/tensorflow/models
 and modify it's name to 'models'
 Make a folder 'Tensorflow' and put this 'models' folder inside. later when you download protoc also put it inside 'Tensorflow'
 OK, Now, go inside Tensorflow/models/research and replace all files with files of this repository ( this repo only contains complete files of 'research' folder.
    
 
 
 Installation 
 .............
Note: I am using Mac with virtual environment ( you can use any env) and python3.

To use of virtual environment:
   pip install virtualenv
   python3 -m venv /path-to-new-virtual-environment
   source /path-to-new-virtual-environment/bin/activate

install tensorflow 
pip install tensorflow
pip install tensorflow-gpu

Install some required packages

pip install Cython
pip install contextlib2
pip install  pillow
pip install lxml
pip install jupyter
pip install user matplotlib

.... 
Some more packages
pip install tf_slim

Note : One error fix:
AttributeError: module 'tensorflow' has no attribute 'GraphDef'
…
In TF-2 this is not supported :https://github.com/tensorflow/models/issues/7703
FIX is here: In [12]: import tensorflow.compat.v1 as tf


Tricky part
..........

 Need to install Protocol Buffers and put py inside object detection model  ( you dont have to do this step if you are cloning this repositort beacuse, I have already added it here.
 ...
 two methods are there 
     1. install protoc: 
       brew install protobuf
     2. download protoc and place it proper folder 
        for this step please refer instruction here:
          https://www.edureka.co/blog/tensorflow-object-detection-tutorial/
     
Now need to create .py file for all files present in your protoc object_detection/protos/ directory ( i already added in current repository)
   Just use command ( so tricky): protoc object_detection/protos/*.proto --python_out=.
   
So, we are all set to go.
 
Running model
...........
 I have created python file here called 'obj_detection.ipynb'
 To have deep understanding of it please refer: https://www.mygreatlearning.com/blog/object-detection-using-tensorflow/
 Use Jupyter to execute this file. 
 When execute it. It detects objects of an image present at 'research/object_detection/test_images'
 
 
 

  

 
 
