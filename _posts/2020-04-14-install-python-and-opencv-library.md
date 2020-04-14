---
layout: post
title: Install Python and OpenCV library
subtitle: In this guide, install python and opencv are implemented
gh-badge: [star, fork, follow]
comments: true
tags: [OpenCV, Python, Library]
---

## Install Python
We have 2 main versions of Python: Python 2.x and Python 3.x. **3.x** is more popular.
[(see the difference [1])](https://sebastianraschka.com/Articles/2014_python_2_3_key_diff.html)

**Install Python directly:**

- Access [Python Home page](https://www.python.org/) choose **Downloads** and consider your desire version. 

**Note:** Choose stable releases and compatible to your OS (Window, MAC or Linux), recommend for "executable installer".

- Download and install it, check in **"Add to PATH"** box to make sure that you can work more convenience through Command Prompt window.

- After finishing installation. Let' check it by accessing **Command Prompt** window and type **python**. when the prompt of the interactive Python interpreter **">>>"** appears, it is sucessful.

```
C:\Users\admin>python
Python 3.6.8 (tags/v3.6.8:3c6b436a57, Dec 24 2018, 00:16:47) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
Here, we can use Python IDLE (Integrated DeveLopment Environment) as an editor.

- Install OpenCV library: First, we have to install preliminary library.
```
pip install numpy
pip install matplotlib
```
**Note:** PIP is a package manager for Python packages, or modules.

Download and install through this [link](https://www.lfd.uci.edu/~gohlke/pythonlibs/) to get **.whl** file, this is wheel format as a standard build-package format for Python. At this site, many standard libraries are present.

- To check it, access Python type 2 command"
```
>>> import cv2
>>> cv2.__version__
```

**Install Python using Anaconda:***
[Anaconda] is an open-source distribution of Python and [R](https://en.wikipedia.org/wiki/R_(programming_language)). It aims to simplify package management and deployment.

Python conda can be installed in the process which sets up Ananconda.

- Access [Anaconda.com](https://www.anaconda.com/), choose **Downloads** label and consider your platform and Python version.

- Run installationn file and customize options. Add Anaconda to the system PATH environment for using directly on command prompt window. Otherwise, anaconda prompt is also useful. 

- To check the installation, type command `conda info` in command prompt window:

- Next, we create environment to manage package with command `conda create --name <your_env_name>`. This way will generate an environment and contain package library.

- Install OpenCV by command `conda install -c conda-forge opencv`. This solution is easier than install as a global library. However, access in environment is required in every single time we need that package.

### Conclusion
This

## References
[1]. [https://sebastianraschka.com/Articles/2014_python_2_3_key_diff.html](https://sebastianraschka.com/Articles/2014_python_2_3_key_diff.html)

[2]. [https://en.wikipedia.org/wiki/Anaconda_(Python_distribution)](https://en.wikipedia.org/wiki/Anaconda_(Python_distribution))

[3]. [https://en.wikipedia.org/wiki/R_(programming_language)](https://en.wikipedia.org/wiki/R_(programming_language))

[4]. [https://anaconda.org/conda-forge/opencv](https://anaconda.org/conda-forge/opencv)
