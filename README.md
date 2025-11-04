# embedded-sentry
This is a repo that is intended to connect with a device "ST 32F429IDISCOVERY board" in Mbed framework. 

To run on VSCode, first install the PlatformIO extension. 
Clone the repo and run the main.cpp file. 
Connect the board to the computer running the program. 

Follow the instructions displayed on the board. Instructions should appear when the board is connected to the program and the app is running successfully. 
Long press (> 2 seconds) the button to initialize the movement that you want to use to unlock the board (create key). 
<img width="531" height="916" alt="recording complete" src="https://github.com/user-attachments/assets/3b1c96c4-3c17-46f4-a4fb-f1efac50764f" />

Short press (< 2 seconds) the button to try a new movement. When the same movement is created, the board should unlock. 
<img width="616" height="838" alt="unlock successful" src="https://github.com/user-attachments/assets/dc694698-5374-4907-ba8e-c2f440a13eb0" />

When a different movement is created, the board should remain locked. 
<img width="408" height="780" alt="unlock fail" src="https://github.com/user-attachments/assets/edd8917e-9a22-4cb2-8338-72f8d6d91f54" />

The program records the spatial location and velocity of the movements and uses Dynamic Time Warping to calculate the similarity between the key movement and the new movement. 
There is a "gesture tolerence" of 90 to account for movement error but keep classification error between lock/unlock minimal. 
