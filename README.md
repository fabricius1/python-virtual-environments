# Description

This tutorial shows how to create and activate **virtual enviroments** in *Python* using the builtin module called ***venv*** (check its [documentation here](https://docs.python.org/3/library/venv.html)).

We recomend that you use a Python stable version equals or or higher than 3.10 in your projects.

My prefered terminal is GitBash, which allows me to write most Linux commands in my Windows Operational System (OS). Thus, some commands might need to be adapted to your other prefered terminals and OS. When we reach the point of activating the virtual environment, we will address this issue with more details. 

# How to create a virtual enviroment with *venv*

1. In your prefered terminal, create a folder to your new project (you can skip this step if your project folder already exists). Mine will be called `my_project_folder`:

>  ```mkdir my_project_folder```

2. Move inside the folder:

>  ```cd my_project_folder```

3. Run the command below to create the virtual environment.  I will call mine `.myenv` but you can name it whatever you want:

>  ```python -m venv .myenv```

The last command will take a little longer to finish running. When that happens, A new folder `.myenv` (or whatever you called it) will be created inside your project folder. The `.myenv` folder has all the virtual environment files you need, including a copy from the Python version linked to the `python` alias you used in the command `**python** -m venv .myenv`. 

# subfolders created with `python -m venv .myenv`

1. In Windows, the name of `.myenv` subfolders will be:
1.1. `Include`
1.2. `Lib`
1.3. `Scripts`

2. In my Linux Ubuntu 20.4 (running in WSL), the following subfolders were created:
2.1. `bin`
2.2. `include`
2.3. `lib`
2.4. `lib`
2.5. `share`

I recommend that you explore this subfolder in the future a little more, especially checking where the virtual environment Python local version is installed and where the future modules, installed with pip when the virtual environment is activated, will be saved in the `.myenv` folder.

A very important note to make is that both the `Scripts` folder (in Windows) and `bin` (in Linux) contain the binary files that will be used latter to activate and deactivate the virtual environment.

# How to activate virtual enviroments with *venv*





