# Anticipating Many Futures: Online Human Motion Prediction and Generation for Human-Robot Interaction
Code for 
Bütepage, Judith, Hedvig Kjellström, and Danica Kragic. "Anticipating many futures: Online human motion prediction and generation for human-robot interaction." 2018 IEEE International Conference on Robotics and Automation (ICRA). IEEE, 2018.
https://ieeexplore.ieee.org/abstract/document/8460651


This code contains code to track a human skeleton using a Kinect sensor and to predict / sample future trajectories using a conditional variational autoencoder. 

# Setup
The underlying tracking software is OpenNI and underlies the copyright of PrimeSense Ltd.    
To run this code, make sure to have installed all dependencies for OpenNI / PrimeSense and that everything is running with a Kinect V1 sensor.


# Use online
The main action happens in SkeletonTracker.cpp, which records and processes the pose data online and in Vaecoder.cpp, which is responsible for prediction. The integrator.cpp file makes sure that these two processes are synced. 

# Model training
To predict human joint trajectories, we use a conditional variational temporal autoencoder with feed-forward inference networks.
The model training is done in python, using theano. The basic code can be found in the python_model_training folder.

# Data
The collected data described in the paper can be found in the collected_data zip file. See the python code how to read in the data
and skeleton_helper.cpp which index matches the corresponding joint positions in the matrices.




