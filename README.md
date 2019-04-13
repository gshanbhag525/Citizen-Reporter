# Citizen-Reporter
a social initiative against Potholes and Garbage 

This Repository shows you how to run an image classification model to classify garbage and potholes.
There are 3 directories :
1. Android
2. Website
3. Tensorflow 

Android directory consists of the android code which you can import in the android studio.

Website directory consists of the the website code which u can run using XAMPP on your localhost machine.

Tensorflow directory consists of a Retrained  model for classifying garbage and potholes specifically.

The instruction for each part is given each section.

# Usage
Clone the repository.

```
git clone https://github.com/gshanbhag525/Citizen-Reporter
cd Citizen-Reporter
```

#IN LINUX/ MACOS

create a virtualenv

```
pip intstall virtualenv
virtualenv -p python3.6 tenshub
source /tenshub/bin/activate
pip install tensorflow==1.8
```
##To test the model
```
python -m scripts.label_image  --graph=tf_files/retrained_graph.pb  --image=/Users/guneshs/Downloads/test1.jpg
```
