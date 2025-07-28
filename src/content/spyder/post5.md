---
title: "Working with Spyder - Part 2: Improving your code quality"
description: "Learn how to improve the quality of your programs using code analysis."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/JnljnAjdO_w?si=r1_225XpOkk8aSAV"
---

## Improving Code Quality with the Code Analysis Pane

Hello everyone! I'm Juanita, and in this video we will learn how to improve your code quality using the Code Analysis pane. To display it, we can click its name under **Panes** in the **View** menu.

This pane detects style issues, bad practices, potential bugs and other quality problems in your code, without having to execute it. There are three ways of running code analysis:

- To analyze a file that is open in the Editor, we can press the configurable shortcut, `F8` by default, or select **Source --> Run code analysis** from the menu bar.
- We can also select a file to analyze by browsing for it using the file button next to the path box. This will start the analysis automatically.
- The third way is to manually enter the path of a file we'd like to check in the path entry box in the pane's toolbar, and click the **Analyze** button in the pane.

Based on these results, the code analysis shows an overall score of **4.34/10**, which allows us to track improvements in our code quality. We can also expand or collapse one or all the sections in the pane to be able to see the **Pylint** errors, warnings and messages identifying the issues with our code.

For example, the results tell us that there is a warning on line 20. To go directly to this line in the Editor, just click the message. Here, the code analysis says there is a `bad-whitespace` issue. To understand what this means, open the Pylint documentation. On the [Pylint docs page](https://pylint.pycqa.org/en/stable/index.html), click on *Pylint features* and search for the code of the message.

```
bad-whitespace [C0326]:

%s space %s %s %s Used when a wrong number of spaces is used around an operator, bracket or block opener.
```

We can fix the error by adding one space before and after the operator in this variable assignment. If we run the analysis again, we can see the error isn't shown any more on this line.

We can click the dropdown arrow in the filename field to view the list of previous analyses. Clicking one of them will show us the results.

Sometimes, it is useful to turn certain messages off. We can do that in three different ways:

1. We might want to silence warnings on only one line; for example, this "unused" import that is still necessary for the code execution. For this, type `# pylint: disable=unused-import` as a comment at the end of the line. Running the analysis again will show us that the error is no longer visible.

2. If we want to silence a message in the whole file, we can do it by writing the disable command at the beginning of the file. For example, we can disable the `invalid-name` warning that appears several times in this file. If we run the analysis again, all of these warnings are gone.

3. Finally, we can suppress specific messages for all files by editing the `.pylintrc` configuration file in your user folder. If it doesn't exist, we can generate it by opening our terminal (or the Anaconda Prompt if you're using Windows) and running:

```
pylint --generate-rc > .pylintrc
```

Now, we can go to the `MESSAGE CONTROL` section in this file and add the corresponding Pylint message name, for example `no-name-in-module`. If we run the analysis one more time, we see that the `no-name-in-module` warnings don't appear anymore.

We can see that the score of our file increased to **7.63/10**, a big improvement over the previous **4.34**.

Now that we've learned how to improve the quality of our code, you are ready to write cleaner and more correct programs using Spyder. Stay tuned for our next videos and as always, **Happy Spydering!**
