# Autonomous Car Simulator Neuarl Network Model / autonomous_car_sim_model

The goal of this project is to use the open-source [Udacity autonomous car simulator](https://github.com/udacity/self-driving-car-sim) to collect data, and train a neural network to control the simulation in the autonomous mode.

## Demo
https://github.com/iitz3bsmd/autonomous_car_sim_model/assets/112030326/2e62bcb3-bc4a-44a4-9e54-cbccadd0ebb1

## Architecture
In this project i decided to adopt the architecture used in the [End to End Learning for Self-Driving Cars](https://images.nvidia.com/content/tegra/automotive/images/2016/solutions/pdf/end-to-end-dl-using-px.pdf) paper from NVIDIA which consists of the follwing: 
![68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f313430302f312a5f414c4133433371655251674a6f68334c5a6e4653672e706e67](https://github.com/iitz3bsmd/autonomous_car_sim_model/assets/112030326/a5ae92d1-9ca6-40df-b454-0693c425cec7)
But I added some twists such as adding a pooling layer to reduce parametrs size (as my GPU was too old and I could only train on the CPU 😢) 
you can check out the full architecture in the Jupyter Notebook.

## Try it for yourself!
The simulation module is integrated into the notebook. as you see in the demo, you can run the autonomous mode server by running the `simulator autonomous mode` block.

## Problems
The model can't handle the bridge section of the map very well. I tried to address this issue by training the model on data for specifically the bridge section, but it only improved slightly. My guess is this can be improved by further training, but this needs to be tested.
