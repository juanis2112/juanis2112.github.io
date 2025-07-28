---
title: "Working with Spyder - Part 1: Beyond the main panes"
description: "Explore how to take advantage of Spyder’s functionality beyond just the four core panes."
pubDate: "Sep 11 2022"
video: "https://www.youtube.com/embed/NOu9JTkUuDg?si=-SBq1Avm1bR-nyAe"
---

## Exploring Additional Panes in Spyder

Hello everyone! I'm Juanita, and I am going to show you how to use some of the remaining panes available in Spyder beyond just the four primary ones.

## Plots Pane

Let's start with the **Plots pane**, which is open by default when launching Spyder.  
To see how it works, let's open a file that will generate a couple of plots from Matplotlib's documentation.

- You can view the generated plots in the Plots pane.
- Browse between them using the arrows or by clicking them in the sidebar.
- In the pane's options menu:
  - **Fit Plots to Window** is enabled by default. Disabling it lets you zoom in/out.
  - **Mute inline plotting** prevents the same figures from appearing in the IPython Console.
- Each time you run the code, new copies of the plots are generated.
  - Remove any by clicking the **X** button in the toolbar.
- The pane auto-updates to show plots from the currently active console.
- Use **Copy to Clipboard** to paste the plot elsewhere (e.g. Word).
- Save plots as PNG using the **save** icon.

## Files Pane

The **Files pane**, also open by default:

- Lets you browse directories, open files in the Editor, and perform file operations.
- Customize view (size, kind, date) in the options menu.
- As you change the top-level folder, the working directory updates and syncs with the active console.
- Double-click text files to open them in the Editor.
- Copy files to paste them as absolute or relative paths.
- Right-click for additional options.
- Open files in external apps or set custom file associations:
  - For example, associate `.csv` with **LibreOffice Calc** via Files > Preferences > File Associations.

## Outline Pane

The **Outline pane** helps navigate large files:

- Open it via **View > Panes**, as it's not visible by default.
- Lists all classes, methods, and functions.
- Click any to jump directly to it in the code.
- Expand classes to view their methods.
- Automatically highlights the object at the current cursor position.
- Enable **Show all files** in the options menu to navigate multiple open scripts/modules.

## Find in Files Pane

The **Find in Files pane** is useful for larger projects:

- Open via **View > Panes**.
- Search for strings or regex across the working directory, project, or a custom path.
- Example: searching `is_dark_font_color` finds all occurrences across files.
- Clicking a result opens the file in the Editor at the match location.

## Online Help Pane

The **Online Help pane** allows browsing documentation:

- Open it via **View > Panes**.
- Shows modules from the standard library and third-party packages (e.g. Numpy, Pandas, Matplotlib).
- Use the built-in browser to navigate pages.
- Use the **Get** field to directly load documentation for a known item.
- Use the **Search** field to find results by keyword.

Now that you're familiar with a wider array of Spyder's panes and features, you can accomplish a variety of common programming tasks with ease.

**Stay tuned for our next videos to further add to your scientific toolbox. And as always, Happy Spydering!**
