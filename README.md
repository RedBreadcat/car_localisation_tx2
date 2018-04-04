# Prereqs
Must install ROS. Also, I recommend you use "catkin build" rather than "catkin_make": http://catkin-tools.readthedocs.io/en/latest/installing.html

NOTE: if you're doing a fresh install of everything, then install the latest Nvidia JetPack (full OS reflash required!!!). It means you probably won't need to do the weird TensorFlow install method below. Also will require the Zed SDK to be updated, and the Zed camera driver to be updated.
It seems as though TensorFlow's repositories don't support the TX2, so follow these instructions if you're using the TX2: https://github.com/jetsonhacks/installTensorFlowJetsonTX
Install the wheel file for Python 2.7 because that's what ROS supports
Follow this to install TensorFlow Object Detection: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md

But instead put a line in the form of this into your .bashrc file:

export PYTHONPATH=$PYTHONPATH:/home/[USERNAME]/git/models/research/:/home/[USERNAME]/git/models/research/slim/


You want to install the models repo into /home/[USERNAME]/git/


# How to install Zed camera driver

Driver is from here: https://github.com/stereolabs/zed-ros-wrapper

Ensure that you pick a release (or pull latest version) that supports the Zed SDK you have installed. Each Zed SDK version requires a specific CUDA version. Changing the version of CUDA requires flashing the relevant JetPack (Full OS reinstall!!!)
