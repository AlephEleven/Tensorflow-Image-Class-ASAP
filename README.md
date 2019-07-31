# Tensorflow-Image-Classification-ASAP
ASAP guide on how to setup Tensorflow/Keras for Image Classification for Windows 10* 

# *Disclaimer*:
This tutorial includes content that can be found online, the goal of this tutorial is to to combine the content in order to make it easier for people who cannont program in Python, or have very little knowlege with neural networks for that matter, but want to see what it's like to use one. What this means is, I went through the work of going through said content in order to make it easier for you to make what this tutorial has to offer and *I do not claim ownership to any of the content I used to make this tutorial*. The following content was used in order to make this tutorial:

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

#### a) After finishing the setup for Miniconda, search for "Anaconda Prompt" in the taskbar and open it. WARNING: Make sure when you open the prompt that it says "*Anaconda Prompt*" and not "Command Prompt"!!!

![Anaconda Prompt in taskbar](https://chrisconlan.com/wp-content/uploads/2017/05/anaconda_prompt.png)

#### b) Then you will create a virtual environment to use for Tensorflow/Python, since TF currently supports up to Python 3.6, we will enter the following command into the Anaconda Prompt. This can be done by entering the following command:

```
conda create --name tensorflow python=3.6
```
![Command Prompt Conda Create](https://i.gyazo.com/e8df78ec1b1c405b0913803377baeb3f.png)


#### When it's done, it will ask you to Proceed, typing in "y" and Enter, This will create a completely new directory in order for you to run your Anaconda/Python programs under the base name "tensorflow"


![Anaconda Proceed Y/N](https://i.gyazo.com/0d658b2a2c1e7d87f3ea02ae0e149c8a.png)

#### Once it has made the new directory, you will activate it.

```
conda activate tensorflow
```
#### As long as you have been following the instructions properly, you should see that in place of (base), it should say (tensorflow).

![Correct base in prompt](https://i.gyazo.com/ef52b1ff655ab91596a637076399161e.png)

#### To make sure that you're using the correct Python version, type the command below:

```
python --version
```

#### It should return: *"Python 3.6.8 : : Anaconda Inc."*, atleast Python 3.6~

#### c) After that, it's time to install a bunch of packages necessary for Tensorflow related projects, simply type in the following one by one:

```
conda install scipy
pip install --upgrade sklearn
pip install --upgrade pandas
pip install --upgrade pandas-datareader
pip install --upgrade matplotlib
pip install --upgrade pillow
pip install --upgrade requests
pip install --upgrade h5py
pip install --upgrade psutil
pip install --upgrade opencv-python
```
If psutil does not work, thats absolutely fine, it is not required as the rest are.

#### Then you will specify the installation of Tensorflow that as of today, is currently stable.

```
pip install --upgrade tensorflow==1.12.0
```
#### In the case that there is a newer ver. of TF, or an error occurs, you can just get rid of the "==1.12.0"

#### And you will also install a specific version of Keras

```
pip install --upgrade keras==2.2.4
```

#### To make sure that Tensorflow has been installed, we will run the following:

```
python
```
#### This will change the prompt to a Python prompt, with it you will check if tensorflow is installed by doing:

```
import tensorflow as tf
print(tf.__version__)
```

#### If no errors have occured, and the prompt returns "1.12.0" after printing (unless you removed the =='s when installing tensorflow) you will be good to!

### What did you just complete:
- You now know how create a base directory, (tensorflow)
- You can now to install and specify packages for said directory
- You can verify that you have properly install a module by importing it in the Python Interpreter

# 3) Installing Pycharm:

a) In order you install Pycharm you will need to download it from the Jetbrains website: (https://www.jetbrains.com/pycharm/download/#section=windows)

For the sake of the tutorial, the Community edition is whats needed. Make sure that the "Released" on the download page says at least January 2019, or higher

![Correct Pycharm download page](https://i.gyazo.com/40f28bd780ed7457a0befa156595fad5.png)

