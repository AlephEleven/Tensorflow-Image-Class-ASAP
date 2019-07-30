# Tensorflow-Image-Classification-ASAP
ASAP guide on how to setup Tensorflow/Keras for Image Classification for Windows 10* 

# *Disclaimer*:
This tutorial includes content that can be found online, the goal of this tutorial was to combine the content in order to make it easier for people who are completely new to programming neural networks or programming for that matter, but want to see what it's like to use one. What this means is, I went through the work of going through said content in order to make it easier for you to make what this tutorial has to offer and *I do not claim ownership to any of it*. The following content was used in order to make this tutorial:

Video by Jeff Heaton: (https://www.youtube.com/watch?v=SfNFz3dRloI) - Installation of Anaconda, Python, Tensorflow and Keras for Pycharm

Video by Chris Dahms: (https://www.youtube.com/watch?v=oXpsAiSajE0) - Image-Classification Walkthrough

Image-Recognition by Google (https://github.com/ArunMichaelDsouza/tensorflow-image-detection) - I.R program in the walkthrough

## In this guide, you'll learn how to do the following:

- Setup Pycharm

- Install Miniconda & make an anaconda file to store Tensorflow related projects

- Install Tensorflow, OpenCV, and other programs useful for ML/NN

- Create a Tensorflow-Python Interpreter for ML/NN

- Prepare the image classification program.

- Train & test a set of images in order to make your own image classifier.

## What this guide will *Not* teach you:

- Programming with python (Although heres an excellent resource by youtuber Corey Schafer: https://www.youtube.com/watch?v=YYXdXT2l-Gg&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU)

- How to make your own neural networks (Free introductory course on ML & NN by Google: https://developers.google.com/machine-learning/crash-course/ml-intro)

- How to use any of the other modules (Searching for a documentation/youtube tutorials should be good enough to learn them)

- Anything else unrelated to this tutorial

# 1) Installing Miniconda:

#### a) To install Miniconda you will need to go on the Miniconda Documentation (https://docs.conda.io/en/latest/miniconda.html) and install Python 3.7 64-bit (exe-installer)

![Miniconda Doc page for download](https://i.gyazo.com/85a1e3cdf6ae040b1387bca3da4226ca.png)

#### b) Once it has downloaded, the next thing to do is to run the installer, (In chrome you can do CTRL+J to check recent downloads then choose "Show in Folder", or just open the Downloads folder and find the installer)

#### c) Upon opening the installer, you should be greeted with a setup page similar to the image below, go through the download and make sure you do the following:

![Miniconda Installer page](https://katiekodes.com/images/screenshot-miniconda-02-execute.png)
  - Continue with the download
  - Agree with the Terms and Conditions
  - Choose "Just me" for Installation Type
  - Make sure your installation location is in the "User or Users" directory.
  - Choose "Register Anaconda as my default Python 3.7" for Advanced Options in order to make the Anaconda Prompt the terminal for Anaconda. 
  - Wait for the installation to complete, and then continue. Deselect the options for "Learn more about Anaconda cloud" and "Learn how to get started with Anaconda"
  
### What did you just complete:
- You now know how to install Miniconda with the proper settings for a Windows device.

# 2) Creating a new Anaconda environment & installing modules using Anaconda Prompt

#### a) After finishing the setup for Miniconda, search for "Anaconda Prompt" in the taskbar and open it.

![Anaconda Prompt in taskbar](https://chrisconlan.com/wp-content/uploads/2017/05/anaconda_prompt.png)

#### b) Then you will create a virtual environment to use for Tensorflow/Python, since TF currently supports up to Python 3.6, we will enter the following command into the Anaconda Prompt. This can be done by entering the following command:

```
conda create --name tensorflow python=3.6
```
![Command Prompt Conda Create](https://i.gyazo.com/e8df78ec1b1c405b0913803377baeb3f.png)


#### When it's done, it will ask you to Proceed, typing in "y" and Enter.


![Anaconda Proceed Y/N](https://i.gyazo.com/0d658b2a2c1e7d87f3ea02ae0e149c8a.png)







# LAST) Installing Pycharm:

a) In order you install Pycharm you will need to download it from the Jetbrains website: (https://www.jetbrains.com/pycharm/download/#section=windows)

For the sake of this tutorial, the Community edition is all thats needed. (This is a tutorial using pure python)

![Correct Pycharm download page](https://i.gyazo.com/40f28bd780ed7457a0befa156595fad5.png)

