# JetRacerPRO_ImageClassification
This repository provides files for training image classification models on the Jet Racer Pro AI robot on Waveshare. There is also a file for combining both the image classification model and the road following model that is provided when setting up the JetRacer.

For this project, you will need to have th JetRacer Pro AI Kit, not the 2GB one on Waveshare. For the road following and image classification file, you will see that I have audio files on my notebook. In order to include audio on your JetRacer Pro, you will need to buy a usb to audio sound card. The one I use is the USB to Audio USB Sound Card on Amazon by Waveshare. It is compatible with both the Jetson Nano and the Raspberry Pi.


The first part of creating an Image Classification Model is by collecting data. In my DataImage file, I make directories of the images that I want to collect. In this case, I made directories for different types of Traffic signs. 

The second part is training the data. I used ResNet18, and trained the model based on the classes I have. So another repository that I based this on was the collision avoidance on Jetracer Repository. However, the training is for two classes and with image classification, you want multiple, so this file accounts to that. 

I trained it for 10 epochs and then named and saved model.

The live demo file is just a basic code to check whether it works. It will display the image and write the prediction on the image so if you put a stop sign, it will say stop since that is the class or label name.

The Road Following and Image Classification file I have would be more simple had I not added the audio portions. I based the file on the roadfollowing.ipynb that the Jetson provides and the collision avoidance repository. It is very simple if statements, where if it sees the image, it will do something, and then if not, it will resume the road following. Feel free to change it however you like, mine is based on the dataset I made. 
