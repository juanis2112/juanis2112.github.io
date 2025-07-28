---
title: "First steps with Spyder - Part 2: Learning the basics"
description: "Learn the basics of using Spyder’s four main panes."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/WV9bm4ey7Cg?si=_WhPnm9Ir8QdLP5f" 
---

## Introduction to Spyder's Main Panes

Hello everyone! I'm Juanita, and in this video I will show you how to start working with Spyder's four main panes.

First, let's take a look at the **Editor**, which you can use to open, edit, and run files from your computer. I will open a short "Hello World" program for this demo, which you can [download here](https://drive.google.com/file/d/18Ai-XY9kIPm9x_7-0RBakV2a6dRVqh-L/view). Once you have it open in your Editor, you can execute it by pressing the green run button. We can see the output in the **Python Console** as well as the path of the file that we are running and the working directory where this code was run.

We can also run any Python code that is entered directly in the IPython Console. For example, we can type:

```python
print("Hello")
```

and see the output. Or, we can try some math operations and see the results here too. Note that for implicitly printed output, there is a red indication that differs from the output of the `print()` function.

Now, let's start defining some variables. We can do this both from the Editor or from the Console.

If I define a variable:

```python
a = 10
```

and then run this code, I can see its value in the console just by typing its name `a`. However, you can also assign any variable in the IPython console:

```python
b = 20
```

and its value will be stored too. In both cases, they can also be seen in the **Variable Explorer** pane, which shows the name, type, size, and value of each of the objects previously defined. In this case, we see variables `a` and `b`, both of type `int` and with size 1.

We can also define a list:

```python
l = [1, 2, 3]
```

and see that the type of the variable is `list` and the size is 3.

We can change the values of the variables in the Variable Explorer too by double-clicking them and typing their new value. Now, we can check their new value in the console. In the case of a more complex type like a list, double-clicking it will open a viewer in which you can modify each of its values separately, along with other more complex operations which we'll demonstrate in a future video.

We can remove a variable by right-clicking it and selecting the option **Remove**. After doing this, we can check in the IPython Console that the variable was actually deleted.

Finally, we are going to learn how to get help for objects in two different ways.

1. Press `Ctrl-I` (or `Cmd-I` on macOS) right after the name of an object written in the Editor or the Console, for example `numpy.array`. You can see that we obtain its documentation in the **Help** pane if it is available.
2. If we change the **Source** dropdown option to **Console**, we can type its name in the object box in the Help pane. Now we can get help for Numpy arrays.

You should now be ready to start using Spyder's four main panes. Check out our next video to continue learning and as always, **Happy Spydering!**