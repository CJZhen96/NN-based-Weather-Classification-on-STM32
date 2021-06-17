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
2. Click on "Choose File" to select images from computer.
3. Label the uploaded data accordingly based on categories.

![image](https://user-images.githubusercontent.com/82163697/122447067-ef9d9e00-cfd5-11eb-8004-83b78d04fbea.png)
4. Move to Impulse Design session. Change the image width and image height to 32 in Image Data Block.
5. In Processing block, select image.
6. Choose Neural Network(Keras) in learning block.
7. Next, click on "Save Impulse" to save the impulse setting.

