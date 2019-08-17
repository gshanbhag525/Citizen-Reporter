# Citizen-Reporter
## Created in a Hackathon called ACELATHON for a social initiative against Potholes and Garbage

This Repository shows you how to run an image classification model to classify garbage and potholes.
There are 3 directories :
- Android
- Website
- Tensorflow 

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

# IN LINUX/ MACOS

create a virtualenv

```
pip intstall virtualenv
virtualenv -p python3.6 tenshub
source /tenshub/bin/activate
pip install tensorflow==1.8
```
## To test the model
```
python -m scripts.label_image  --graph=tf_files/retrained_graph.pb  --image=/Users/guneshs/Downloads/test1.jpg
```

It will display the match as pothole or garbage.

>(fortf1dot8) SecurityNinja:tensorflow guneshs$ python -m scripts.label_image  --graph=tf_files/retrained_graph.pb  --image=/Users/guneshs/Documents/garbage.jpg 

>Evaluation time (1-image): 0.228s

>garbage (score=0.99994)
>pothole (score=0.00006)

# Website

you can just paste the contents of website directory in XAMPP/htdocs directory.
Start the mysql and apache server from XAMPP control panel

import the database.sql file from the website directory int phpmyadmin.

On the website, admin would see all the photos taken by the user.

# Android App

First, the user has to register and login. Then in the next Screen, A listView of all the different images posted by other users would be displayed along with the location. 
A user can take a picture from Camera App or can select the image from gallery.
An inference would be run on the android app itself. 
Instead of sending the image to cloud for processing we implemented the client side image processing using TensorflowLite.
This saves a lot of time and works Offline too.

We trained the model using mobilenet and transfer learning.

Hope this App Saves Our Environment and many lives too.
