---
title: "Spyder says: Let's contribute"
description: "In this video, you will learn how to contribute to open source by solving a simple issue with Spyder."
pubDate: "Sep 10 2022"
video: "https://www.youtube.com/embed/GizipMT1LvQ?si=CCEUP3RTfyYJyBPY" 
---

Has someone ever told you they are a software developer? 

A software developer? Yes, a software developer. I bet the first time you heard this, you were imagining something amazingly complicated. 

**BUUUUT** I think many software developers, including me, probably started with simple issues and learned a bunch of things along the way. It may feel like contributing to open source is beyond your skillset, but sometimes the hardest part is just getting started!

## 👋 Introduction

Hello everyone! I’m Juanita, one of the Spyder developers, and in this video I will teach you how to start contributing to open source by solving a simple issue with Spyder.

## 🔧 Step 1: (Fork the projects repo)

The first step is to fork the repository of the project you want to contribute to. You’ll need to sign in to your account on GitHub in order to do this, or create one if you don’t have one. Then, go to the project’s repository and click the “Fork” button at the top left of the page. This will create a copy of the repository in your own account. 

## 📥 Step 2: (Clone your fork)

On your new fork, click the green “Code” button and copy the link that appears there to get the URL for cloning it.

In case you don’t have Git set up on your computer, follow the instructions in the link below.  

🔗 [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Now, open your terminal (or Git Bash, if you’ve installed Git for Windows) and type the command ‘git clone’ followed by pasting the URL you just copied. With this, you now have a local copy of your fork.
Finally, change to the directory of the repo you just cloned with cd spyder, and add the Spyder repo as the “upstream” remote repository by typing the following:

```bash
git remote add upstream https://github.com/spyder-ide/spyder.git
```  

This will allow you to keep your local repo up to date with the latest changes in Spyder.

For a beginner guide on using Git, check the link below:

🔗 [Beginner Git Guide](https://rogerdudler.github.io/git-guide/)


## 🛠️ Step 3: (Set up your development environment)

Most open source projects have their own contributing guide, which explains the steps needed for setting up your development environment. You’ll find Spyder’s in the root directory of the repo. After opening it, follow the instructions under “Creating a Conda environment or virtualenv”. Here, I will guide you through the main steps using Conda. If you don’t have Anaconda installed, please download it from the link below.

🔗 [Install Anaconda](https://www.anaconda.com/products/individual)

To create and activate a new Conda environment for developing Spyder, type the following commands in your terminal (or Anaconda Prompt on Windows):

```bash
conda create -n spyder-dev python=3
conda activate spyder-dev
```

After you have created your new Conda environment, you need to install Spyder's necessary dependencies. The easiest way to do so with Conda is by running:

```bash
conda install -c spyder-ide/label/dev --file requirements/conda.txt
```

Now that your environment is ready, to start the Spyder’s development version, simply type:

```bash
python bootstrap.py
```

This will allow you to view the changes that you make in Spyder during your development process, because it starts Spyder from the code in your clone.


## 🧩 Step 4: (Pick an issue)

Now we need to select the issue we want to fix. For this demo, I will choose one from our issue tracker linked below.

🔗 [Issue Tracker](https://github.com/spyder-ide/spyder/issues)

For some ideas on easy issues to fix, click the “Label” dropdown and select the option “community:Easy”.

The issue we will fix now is [#13741](https://github.com/spyder-ide/spyder/issues/13741), which is about matching the PYTHONPATH tooltip with the title in its dialog.

## 🌱 Step 5: (Create a new branch for your changes)

To do so, you first have to create a branch for your work. If your change is small, like a bug fix or minor UI improvement, you should make it to the branch for the current version of Spyder, in this case “4.x”, instead of master. You need to base your new branch on the correct Spyder branch in order to avoid conflicts.  WARNING

For this, run:

```bash
git checkout 4.x
```

Then, you need to reset the spyder configuration file when switching between master and 4.x by running:

```bash
python bootstrap.py -- --reset
```

Next, create your branch from this one. Remember to give your branch a name (in our case, `pythonpath-tooltip`) that is related to your fix. For this, run the following command:

```bash
git checkout -b pythonpath-tooltip
```

## 🔍 Step 6: (Reproduce the issue)

Usually, when the issue is a bug, the first thing you need to do is try to reproduce the error by following the steps reported in the issue. If it includes a Python traceback, it will most likely include the file and line of the error in Spyder’s source code. This will usually allow you to find and fix the bug more easily. In this case, though, we are improving some text in the interface rather than resolving an error,  so we run Spyder in development mode to see the tooltip that we want to fix.

```bash
python bootstrap.py
```

We can see that the PYTHONPATH Manager tooltip doesn’t match the title of the dialog it triggers. 

## 🔎 Step 7: (Find the file and make the changes)

One of the hardest parts of the process often is finding the file where we are supposed to make the change. For this, what I usually do is search for a string that might help me find the file in Spyder’s repo. In this case, I will use the Find pane in Spyder’s stable version to search for the tooltip’s original message.

Now that we found the part of the code in charge of the PYTHONPATH manager tooltip, we have to change the string to match the dialog title.

## ✅ Step 8: (Confirm/test that the issue is solved in dev mode)

Open Spyder in development mode one more time to verify that the change was successfully applied.

## 📝 Step 9: (Commit your changes)

Now, you are ready to add and commit your changes with a descriptive message.

```bash
git commit -a -m "Change tooltip of PYTHONPATH manager to match title in dialog"
```

Finally, push your new branch with your changes to your fork on GitHub:

```bash
git push -u origin pythonpath-tooltip
```

Enter your GitHub username and password if requested.

## 🚀 Step 10: (Open PR in Spyder repo (4.x))

Now, you can submit your changes to Spyder’s repo. 

After you pushed your branch to your fork, go to the Spyder repository on Github, and you will see the option to open a Pull Request. Before submitting it, make sure that you read the template. Add “PR: ” to the title, describe the changes you made, upload a screenshot if possible, link the issue that you are solving, and finally typing your username to affirm you have the right to release your changes.

You also have to make sure that you select the correct branch to merge your changes. In this case, I based my changes on the branch 4.x, so I select it in my Pull Request.

## 👋 Goodbye

Now you are ready for contributing to Spyder, and even other open-source projects! 
Subscribe to our channel to watch more of our videos, and comment below to let us know if it helped you make your first pull request!

THANKS FOR WATCHING AND **HAPPY SPYDERING**!

