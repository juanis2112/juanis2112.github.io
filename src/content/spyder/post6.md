---
title: "Working with Spyder - Part 3: Optimizing your code"
description: "Learn how to optimize your code using the profiler."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/4hcXa8aGu_c?si=teZS9ZkDQZ1wLixv"
---

## Optimizing Your Code Using the Profiler Pane

Hello everyone! I'm Juanita, and in this video we will learn how to optimize your code using the **Profiler**. To display it, click its name under **Panes** in the **View** menu.

The Profiler will determine the run time and number of calls for every function and method used in a file. There are three ways of profiling a file:

- We can browse for a file using the open button to the right of the Profiler's path box, which will run profiling over it automatically.
- We can also manually enter the path in the pane's path box, and then run the analysis on the file by pressing the **Profile** button.
- If we want to run the profiler for the file that is currently open in the Editor, we can click **Run --> Profile...** in the menu bar, or use the configurable shortcut `F10`.

We see that the results in the pane show us the different functions and methods in our file, with each sub-function listed hierarchically under the item that called them. The columns show the **total time** taken by each function and everything it called, while the **local time** includes only the time spent in that particular function.

For example, the function `values` in this file calls a function `internal_values`. `values` took a total of **482 µs** to run, with **338 µs** of that spent executing `internal_values` inside of it. Therefore, the total time for `values` is **482 µs**, but its local time is only **144 µs** as the rest was spent inside `internal_values`.

The **Calls** column displays the total number of times that function was called at that level. Finally, the numbers in the **Diff** columns for each of the three appear if a comparison is loaded, and indicate the change in runtime between the two measurements.

By double-clicking an item in the Profiler, we will be taken to the file and line in the Editor where it was called. If this function was not called in one of your open scripts, clicking it will open the file that contains it. We can click the down arrow button in the filename field to recall paths of previously profiled files.

Now that we know how to interpret the results of our profiling, let's optimize our code by finding the functions that take the longest time and making them faster. In this case, `to_datetime` takes **39 seconds** to run. The reason for this is **Pandas** has to parse the non-standard timestamp format and is not told to try to use a faster parser than the default.

We can reduce the time this function takes and compare it with the one before. For this, first we have to save the data as a `.Result` file with the **save** button in the pane. Now we have to figure out how to optimize the function, so let's search for it. We see that we can speed up this function by [manually specifying a datetime format](https://stackoverflow.com/questions/32034689/why-is-pandas-to-datetime-slow-for-non-standard-time-format-such-as-2014-12-31). So, we add the appropriate argument, `format="%Y-%m-%d %H:%M:%S.%f %z"`, to our function call.

Now, we run the profiling again to see how our script's performance has improved. If we want to see how much we lowered the time, we can load our previous result and take a look at the **diff** columns. Notice the difference is green because the time was reduced by three times, taking only **13 seconds** instead of **39**. Our code is now **26 seconds faster**!

Now that you've learned how to analyze the execution time of your code, you are ready to write more efficient programs with Spyder's help. Stay tuned for our next videos and as always, **Happy Spydering!**
