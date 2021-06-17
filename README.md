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

![image](https://user-images.githubusercontent.com/82163697/122458620-9b4ceb00-cfe2-11eb-9403-7ff5dc75fe9f.png)
1. Go to Help > Manage embedded software packages. Select "From Local ..." and select the .pack file just downloaded. Accept the license agreement and the pack will be installed. The version number is automatically updated whenever the pack is exported.


![image](https://user-images.githubusercontent.com/82163697/122458846-d6e7b500-cfe2-11eb-8565-923e84929631.png)

2. Go back to .ioc file and go to "Pinout & Configuration". Click "Software packs" > "Select components". Select the project, expand the pack and add a checkbox under "Selection". Click OK to close the window.

![image](https://user-images.githubusercontent.com/82163697/122459861-064af180-cfe4-11eb-9884-0bf8c6faaefd.png)

3. Under "Pinout & Configuration", select "Software Packs" and click on project name. Place a checkbox next under 'Mode'.

![image](https://user-images.githubusercontent.com/82163697/122459363-6f7e3500-cfe3-11eb-816f-d571eda7f941.png)

4. Save the project and "Middlewares: folder will be included.

![image](https://user-images.githubusercontent.com/82163697/122459518-99375c00-cfe3-11eb-8c2f-29ca1921f23c.png)

5. In main.cpp, hardcoded the raw feature data into program.

![image](https://user-images.githubusercontent.com/82163697/122459673-c6840a00-cfe3-11eb-80c4-4d3d77d08f0e.png)

6. Under USER CODE BEGIN Includes type the code above.

![image](https://user-images.githubusercontent.com/82163697/122459767-e3b8d880-cfe3-11eb-9c5d-478653aec476.png)

7. Under USER CODE BEGIN Init, add the code above.

![image](https://user-images.githubusercontent.com/82163697/122459902-11058680-cfe4-11eb-9abf-dd368cdf92ca.png)

8. Under USER CODE BEGIN 0 add the functions above.

![image](https://user-images.githubusercontent.com/82163697/122460012-31354580-cfe4-11eb-88f5-1b315ea5436f.png)

9. In while(1) loop, add the code above.

![image](https://user-images.githubusercontent.com/82163697/122460075-47db9c80-cfe4-11eb-8c71-4e77666dd4b2.png)

10. The code above is added to print message in Putty terminal.

![image](https://user-images.githubusercontent.com/82163697/122460159-5e81f380-cfe4-11eb-8308-ae660dd3d032.png)
![image](https://user-images.githubusercontent.com/82163697/122460173-6477d480-cfe4-11eb-92dd-1c2ca45eb949.png)

11. Results show above are expected.


