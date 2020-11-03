## Working with Bokeh on your local machine


### Installation without a virtual environment
- It is recommended that you use `conda install` when installing Bokeh on your local mahchine since conda will take care of all the dependencies that Bokeh requires for you. 
- If you have conda already installed on your computer, simply open you terminal and type in `conda install bokeh`. If you do not have conda installed, here is a guide on how to [install conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/#regular-installation). 
- If you don't want to install conda, You can also use `pip install bokeh` since pip should already be installed if you are using Python 3.4 and above. You can check whether you have pip installed by typing in `pip --version` in your terminal. However, if you want to use pip to install Bokeh, you need to make sure that [all the required dependencies](https://docs.bokeh.org/en/latest/docs/installation.html) are also installed.

### Installation with a virtual environment
Using a virtual environment gives you the ability to created an isolated environment for your project. Think of it as a drawer that contains all the packages you need for your current project and that project only. This is nice because you can keep your system (think of it as your room) organized, and the content of this particular drawer will not affect things in other drawers. It is often beneficial to use a virtual environment, so we will walk you through how to set up a vitual environment for this project.

- If you are using Python3, you should already have the `venv` module installed. If not, you should be able to install it with `python3 -m pip install --user virtualenv` on MacOS or `py -m pip install --user virtualenv` on Windows. 
- Next, make a directory for our project.
- We need to specify which packages we want to install for our project. Instead of typing in the packages one by one, we can create a "requirements.txt" file. For this project, we have made the requirements file for you [here](/requirements.txt). It contains all the packages you need to set up Bokeh and some packages specific for this lab like GeoPandas. Simply copy everything from the link above, make a `requirements.txt`file in your **project directory**, and paste everything in.
- Now that we have our `requirements.txt` file, let's create our virtual environment. Navigate into the project directory from your terminal. Type in `python3 -m venv env` for MacOS and `py -m venv env` for Windows to set up a virtual environment. Now if you go to your project directory, you should see a new folder named "env".
- You should still be in your project directory. To activate your virtual environment, type in `source env/bin/activate`. 
  - To check that you have successfully activated your virtual environment, type in `which python` for MacOS or `where python` for Windows and you should see a return statement that ends in "...env/bin/python".
- Finally, we can install our packages for this project. With your virtual environment activated, typed in `pip install -r requirements.txt`. If the installation is successful, you should be all good to go!

To run a `.py` file, use the command `source env/bin/activate` and type in `python3 <the name of your file>` as you would normally. To get out of the virtual environment, use the command `deactivate`. Note that your python file might not execute outside of the virtual environment since the dependencies might not be installed, so always activate your virtual environment before running the file!

### Out putting Bokeh plots as an HTML file
Change the line `output_notebook()` to `output_file('<the_name_of_your_html_file>.html')`. After you run the Python file, you should see an HTML file being added to your project directory!

### Closing Thoughts
In this lab, we were only able to touch upon a small portion of Bokeh's functionalities. However, if you are interested, we really encourage you to take a look at Bokeh's [user guide](https://docs.bokeh.org/en/latest/docs/user_guide.html) and [gallery](https://docs.bokeh.org/en/latest/docs/gallery.html) to see all the cool things you could do with Bokeh, such as streaming data or linking graphs together!

And [here](https://realpython.com/python-virtual-environments-a-primer/#:~:text=At%20its%20core%2C%20the%20main,dependencies%20every%20other%20project%20has.) is an article that goes more in depth into what virtual environments are and how to set them up.
