---
title: "Spyder FAQ: How do I use additional packages if I downloaded Spyder from the standalone installers?"
description: "In this video, you will learn how to use an extra package within Spyder if you downloaded it using the standalone installers."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/i7Njb3xO4Fw?si=Sf0pgrDwH1Z9L8yI" 
---

Spyder’s installers come with several Python packages such as Pandas, Matplotlib and Numpy to use within Spyder. Here, I will teach you how to use other modules that are not part of our installers but can be useful for your work. I will use Scikit-learn as an example. 

The first thing you need to do is install Miniconda (or Anaconda) from the links below. 

[🔗 Miniconda download page](https://docs.conda.io/en/latest/miniconda.html)  
[🔗 Anaconda download page](https://www.anaconda.com/products/individual)

If you already have any of these two, you don’t need to install them again!

I will show you how to do this using Miniconda because it’s faster and takes much less space. First, find your operating system, click the link depending on the Python version you want to use and follow the instructions.  
[click link in the Miniconda website and show interactive installer]

For Spyder to recognize it, the installation should be done in one of the default paths shown in the following table. Make sure that the Anaconda or Miniconda distributions are in one of these paths so that you can easily connect their environments with Spyder. Otherwise, you’ll have to set your environments manually.

| Windows                         | macOS                              |
|--------------------------------|-------------------------------------|
| C:\Users\<username>\Anaconda   | /Users/<username>/opt/anaconda     |
| C:\Users\<username>\Miniconda  | /Users/<username>/opt/miniconda    |
| C:\Users\<username>\Anaconda3  | /Users/<username>/opt/anaconda3    |
| C:\Users\<username>\Miniconda3 | /Users/<username>/opt/miniconda3   |
| C:\Anaconda                    | /opt/anaconda                      |
| C:\Miniconda                   | /opt/miniconda                     |
| C:\Anaconda3                   | /opt/anaconda3                     |
| C:\Miniconda3                  | /opt/miniconda3                    |
| C:\ProgramData\Anaconda        |                                     |
| C:\ProgramData\Miniconda       |                                     |
| C:\ProgramData\Anaconda3       |                                     |
| C:\ProgramData\Miniconda3      |                                     |

The next thing to do is create a new conda environment with the modules that you want to use within Spyder and include `spyder-kernels` in it. For example, if you want to use `scikit-learn`, open your terminal or the Anaconda prompt on Windows and run the following commands:

```bash
conda create -n spyder-env -y
conda activate spyder-env
conda install spyder-kernels scikit-learn -y
```

Finally, you need to connect Spyder with this environment by changing Spyder’s default Python interpreter. To do this, click the name of the current environment in the status bar, and then click "Change default environment in Preferences".

This will open the Preferences dialog in the Python interpreter section. Here, select the option "Use the following Python interpreter", and use the dropdown below to select your preferred environment. If it is not listed, use the text box or the "Select file" button to enter the path to the Python interpreter you want to use.

Click "Restart kernel" in the Consoles menu for this change to take effect. Then, check in the console that you can successfully use this package.

