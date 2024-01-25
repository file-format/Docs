{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FIG File - MATLAB Figure File - What is .fig file and how to open it?",
  "description" : "Learn about MATLAB Figure File and how to open it.",
  "linktitle" : "FIG",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-fig",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## What is a FIG file?

A FIG file is a special file that holds picture or graph made using MATLAB program, which is used for doing math and analyzing data. This file holds information about pictures or graphs that MATLAB draws to help people see and understand data better. It is like a container that keeps all the details about graphs. 

.FIG is the default MATLAB figure file format. It stores complete figure, including all axes, labels, and settings. To save a figure in this format, you can use `savefig` function:

## About MATLAB Software - To open FIG file

MATLAB, short for "Matrix Laboratory," is powerful programming and numerical computing environment developed by The MathWorks. It is widely used for tasks such as data analysis, mathematical modeling, algorithm development, and scientific computing. MATLAB allows users to manipulate matrices, plot graphs, implement algorithms, and create user interfaces, making it a versatile tool for engineers, scientists, and researchers across various disciplines. Its intuitive syntax and extensive library of functions make it popular choice for solving complex mathematical problems and conducting simulations.

## How to create FIG file with MATLAB?

To make FIG file using MATLAB, follow these steps:

1.  **Select your data:** Pick variable you want to create a plot for from "Workspace" pane in MATLAB.
    
2.  **Choose plot type:** Head to "PLOTS" tab and click on type of plot you want.
    
3.  **Save the plot as FIG file:**
    
    -   Go to "File" menu.
    -   Choose either "Save" or "Save As."
    -   Provide name for your file and decide where you want to save it.
    -   Click "Save" to create your FIG file.

You can also save it as FIG file using `savefig` function. Choose filename and provide extension '.fig':

## How to open a FIG file?

To open FIG file in MATLAB, follow these steps:

1.  **Open MATLAB:** Start MATLAB on your computer.
    
2.  **Navigate to "PLOTS" tab:** Click on plot in "PLOTS" tab, selecting the type of plot you want.
    
3.  **Open FIG file:**
    
    -   Go to "File" menu.
    -   Choose "Open."
    -   Navigate to location where your FIG file is saved, select it, and click "Open."

Alternatively, you can use `openfig` function in MATLAB:

## References
* [MATLAB](https://en.wikipedia.org/wiki/MATLAB)
