# NN-based-Weather-Classification-on-STM32

Group Members:
1. Chung Wei Hong
2. Chan Jia Zhen

# Proceduce for "The Weather Images Classification Based on Convolutional Neural Network using STM32 Microcontroller"
There are two part for this project:
1. Training part -Edge Impulse
2. Deployment on STM32 board

Training Part:
![image](https://user-images.githubusercontent.com/82163697/122446735-946bab80-cfd5-11eb-8f6a-937e81aa77dc.png)
1. In Dashboard, click on the "Let's Collect Some Data" to start training project.

![image](https://user-images.githubusercontent.com/82163697/122446906-c250f000-cfd5-11eb-9c91-7c859b4f84f6.png)
2. Click on "Choose File" to select images from computer. Next, label the uploaded data accordingly based on categories.

![image](https://user-images.githubusercontent.com/82163697/122447067-ef9d9e00-cfd5-11eb-8004-83b78d04fbea.png)
3. Move to Impulse Design session and then change the image width and image height to 32 in Image Data Block. In Processing block, select image. Next, choose Neural Network(Keras) in learning block. Finally, click on "Save Impulse" to save the impulse setting.


![image](https://user-images.githubusercontent.com/82163697/122457315-18776080-cfe1-11eb-954e-4b2f5e81e7df.png)

4. Choose "RBG" and click "Save Parameter".

![image](https://user-images.githubusercontent.com/82163697/122457354-2200c880-cfe1-11eb-8437-020dfa65a895.png)

5. Keep the default setting for training layer. The number of training cycle is set to 20, 0.0005 for learning rate and 0.60 for minimum confidence rating. After key in the setting, start the training.

![image](https://user-images.githubusercontent.com/82163697/122457567-5d02fc00-cfe1-11eb-9b31-c87183ff50ee.png)

6. Check on the accuracy.

![image](https://user-images.githubusercontent.com/82163697/122457622-6be9ae80-cfe1-11eb-9cdc-ad43e6a8a283.png)

7. In Model testing session, click "Classify All" to show the validation result for test data.

![image](https://user-images.githubusercontent.com/82163697/122457765-950a3f00-cfe1-11eb-8d4c-ef54dc6fb382.png)

8. Select Cube Mx CMSIS PACK in Deployment session. Next, click "Build" to download the trained model pack.


Deployment into board:


