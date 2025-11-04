# embedded-sentry
This is a repo that is intended to connect with a device "ST 32F429IDISCOVERY board" in Mbed framework. 

To run on VSCode, first install the PlatformIO extension. 
Clone the repo and run the main.cpp file. 
Connect the board to the computer running the program. 

Follow the instructions displayed on the board. Instructions should appear when the board is connected to the program and the app is running successfully. 
Push the buttom to initialize the movement that you want to use to unlock the board (create key). 
When the same movement is created, the board should unlock. When a different movement is created, the board should remain locked. 

The program records the spacial location and velocity of the movements and uses Dynamic Time Warping to calculate the similarity between the key movement and the new movement. 
There is a "gesture tolerence" of 90 to account for movement error but keep classification error between lock/unlock minimal. 
