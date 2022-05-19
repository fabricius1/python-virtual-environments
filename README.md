# Description 

This file shows how to create and activate **virtual enviroments** in *Python* using the builtin module called ***venv***.

We recomend that you use a Python stable version equals or or higher than 3.10 in your projects.

My prefered terminal is GitBash, which allows me to write most Linux commands in my Windows Operational System (OS). Thus, some commands might need to be adapted to your other prefered terminals and OS. When we reach the point of activating the virtual environment, we will address this issue with more details. 

# How to create a virtual enviroment with *venv*

1. In your prefered terminal, create a folder to your new project (you can skip this step if your project folder already exists). Mine will be called `my_project_folder`:

```mkdir my_project_folder```

2. Move inside the folder:

```cd my_project_folder```

3. Run the command below to create the virtual environment.  I will call mine `.myenv` but you can name it whatever you want:

```python -m venv .myenv```

The last command will take a little longer to finish running. When that happens, A new folder `.myenv` (or whatever you called it) will be created inside your project folder. The `.myenv` folder has all the virtual environment files you need, including a copy from the Python version linked to the `python` alias you used in the command `**python** -m venv .myenv`

# How to activate virtual enviroments with *venv*

