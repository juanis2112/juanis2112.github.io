---
title: "First steps with Spyder - Part 1: Getting Started"
description: "Discover the basics of using the Spyder interface and get an introduction to its four main panes, along with a quick look at the others."
pubDate: "Sep 10 2022"
video: "https://www.youtube.com/embed/E2Dap5SfXkI?si=pFNG_bDy2mBUswSl" 
---

## Introduction to the Spyder Interface

Hello everyone! I'm Juanita, and in this video I'm going to show you how to open Spyder and go over the basics of Spyder's interface.

We will learn about Spyder's four panes that you'll likely be using most often, as well as briefly explore the others that are open by default.

If you don't have Spyder installed and would like to follow along, you can [download it here](https://www.spyder-ide.org/).


## Opening Spyder

The easiest way to open Spyder is by opening **Anaconda Navigator** and clicking on the Spyder application.

In case you have an older version of Spyder in Anaconda, open the command line (or the **Anaconda Prompt** in the case of Windows) and type the commands:

```bash
conda update anaconda
conda install spyder=4
```

To launch Spyder without opening Navigator, open your command line and type:

```bash
spyder
```

If you followed the [installation guide](/installation), you should have everything necessary to open Spyder 4.


## The Spyder Interface

This is what Spyder 4 looks like in its default configuration, though you can thoroughly customize it, which we'll get to in a later tutorial.

You can see that it is divided into three sections showing three different panes:

- **Editor**
- **IPython Console**
- **Help viewer**

These three, along with the **Variable Explorer**, are the four core panes you'll work with the most in Spyder.


### Core Panes

- **Editor (Left)**  
  Here you can open, edit, and run files.

- **IPython Console (Bottom Right)**  
  Use this both interactively and to run your code from the Editor. It also shows the version of Python you're using.

- **Help Pane (Above Console)**  
  Get more information and documentation for any object in the Editor or Console by pressing `Ctrl+I` (or `Cmd+I` on macOS). We'll see how to do this in our next video.

- **Variable Explorer (Top Right)**  
  View the name, type, size, and value of variables defined in the Editor or Console. You can even modify these values by double-clicking them in the Value column.


### Additional Panes

- **Plots Pane**  
  Displays figures generated with Matplotlib and other libraries.

- **Files Pane**  
  Lets you browse your file system and open files in the Editor with a click.

- **History Pane (Bottom Right)**  
  Shows the commands you've entered in the Console, including those from previous sessions.


I hope you're now familiar with the basics of using the Spyder interface.

In the next video, we will start working with Spyder's core panes.

**Happy Spydering!**
