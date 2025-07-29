---
title: "Spyder says: Don't mix pip and conda"
description: "In this video you will learn how to fix some of the most common issues you can run into with Spyder, when you mix pip, Conda-Forge and Anaconda for package installation."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/Ul79ihg41Rs?si=p3S3bLw6Xk1vfm7h" 
---

## 🎬 HOOK

¿Have you ever messed up Spyder by trying to install a package?  
¿Does your IPython console give you a bunch of errors?  
¿Have you installed a python package and couldn’t get it to work?  
¿Has your Spyder died for apparently no reason and never come back to life again?  
¿Did you install Spyder and never got it working at all?

This video is for you!

## 👋 INTRODUCTION

Hello everyone, I’m Juanita, one of the Spyder developers and in this video I’ll help you fix some of the most common issues you can run into with Spyder, when you mix Pip, Conda-forge and Anaconda for package installation.  

If you have used any of these commands you may have broken your Spyder installation or other packages in your environment. 

```bash
pip install <package>
conda install <package>
```

But don’t worry, I will show you what’s the best way of fixing this.

This video is divided into two parts. In the first, we will go through a series of steps that hopefully help you solve the problems you are having and in the second, I’ll explain a safer way to install Python packages without breaking Spyder. If you haven’t had any issues yet, you can skip to part 2.

## PART 1: HOW TO UNMESS YOUR MESS

### 🔎 Step 1: Check GitHub Issues

The first thing you should do when you get an error with Spyder is checking if someone else has had the same issue and managed to solve it with some help.

To do this, go to our issue tracker linked below, delete the “is:open” text in the search field to be able to browse through all our issues and paste the last line of the error that appears in your error dialog or command line. Look for the most recent issues first.

[Spyder's issue tracker 🔗](https://github.com/Spyder-ide/Spyder/issues)

You will see that many of the people that reply these issues have the “member” tag which means they are part of Spyder’s developer team and you should follow their advice. Try not to follow advice from anyone without a member tag.  

### 🌐 Step 2: Search Stack Overflow

If this issue search is not successful, try googling the same last line of your error or the description of your problem and look for answers in Stack Overflow. Our lead maintainer Carlos Cordoba replies to many of the questions from users and one of his answers might be helpful. In this case I will also strongly suggest not following any advice that’s not from him.  

### 🪟 Step 3: Remove AppData Conflicts (Windows)

If you couldn’t solve your issue with the previous steps, there’s a few things more to try. If you’re not a Windows user, you can skip to step 4.

If you use windows, type the following path in the address bar of windows explorer:

```bash
%appdata%/python
```

If you find it, delete the content in it. Packages installed in this directory will override those installed by Anaconda and could break Spyder.

### 🧪 Step 4: Create New Environment with Spyder

If things are not fixed yet, you can try installing Spyder in a new environment. To do so, type these commands in the terminal or Anaconda prompt:

```bash
conda create -n spyder-env python=3 -y
conda activate spyder-env
conda install spyder -y
```

### 💣 Step 5: Uninstall and Reinstall Anaconda

Last thing you should do if none of the steps before worked is uninstalling anaconda and installing everything again which we will go over in Part 2. This process depends on your operating system so you should follow the instructions in the link below. 

[Uninstall Anaconda 🔗](https://docs.anaconda.com/anaconda/install/uninstall/)

However, I’m going to show you how to this on Windows. In the Control Panel, choose Add or Remove Programs, and then select Python 3.7 Anaconda and click the uninstall button.

Once you uninstalled everything, you are ready for part 2 where we’ll see how to do our Spyder and package installation right. 

## PART 2: HOW TO DO IT RIGHT

### ⬇️ Step 1: Download and Install Anaconda

The first thing you have to do to get Spyder working is download it using Anaconda. Go to the link I posted on the description and follow the instructions. 

[Install Anaconda 🔗](https://www.spyder-ide.org/#fh5co-download)

When downloading Anaconda, you also get many packages by default that you will find useful for working with Python. 

[Anaconda Package List 🔗](https://docs.anaconda.com/anaconda/packages/py3.7_win-64/)

### 📦 Step 2: Install Extra Packages with Conda

However, you might want to use a package that wasn’t included in your Anaconda installation like Pygame, or a more recent version of one, like Tensorflow or Pytorch. 

The first approach for installing an extra package should be using conda. Type:

```bash
conda install <packagename>
```

If you get an error, go to step 3.

### 🌍 Step 3: Install from Conda-Forge

If step 2 didn’t work, you should try installing your package from conda-forge.

To make sure your package is available in conda-forge, type its name in the search bar of the following link:  

[Anaconda Package Search 🔗](https://anaconda.org/)

If you don’t find it, go to step 4.

Otherwise you MUST create a new environment in which you can install your package from conda-forge.

Use the following commands to create and activate this new environment:

```bash
conda create -n <name> -c conda-forge python=3
conda activate <name>
```

Then, install the package you want using:

```bash
conda install -c conda-forge <packagename>
```

If your package installation was successful, you need to install Spyder kernels in this environment:

```bash
conda install -c conda-forge spyder-kernels
```

Now, you can jump to step 5. If it fails, go to step 4.

### 🧪 Step 4: Create New Environment with Spyder using pip

If installing from conda-forge didn’t do the trick, you should try using pip.  

But same as with conda-forge, you should do so in a new environment. **DO NOT MIX PIP AND CONDA**

Use the following commands to create and activate this new environment:

```bash
conda create -n <name> python=3
conda activate <name>
```

Install the package you want:

```bash
pip install <packagename>
```

Install Spyder kernels:

```bash
pip install spyder-kernels
```

### 🧭 Step 5: Change Python Interpreter in Spyder

To work in this new environment with Spyder, it is necessary to change Spyder’s default python interpreter. 

To do so, first go to your terminal, type:

```bash
conda info --envs
```

Copy the path from the environment you created.

In Spyder → Preferences → Python interpreter → paste the path and add `/bin/python` at the end for Mac and Linux or `/python.exe` in Windows.

### 🔁 Step 6: Restart Spyder

Finally, restart Spyder to make these changes take effect.

I hoped this video helped you bring YOUR Spyder back to life and learned some tips to keep it that way. Subscribe to our channel to watch more of our videos and comment below to let us know if it solved your issues.

THANKS FOR WATCHING AND **HAPPY SPYDERING!**
