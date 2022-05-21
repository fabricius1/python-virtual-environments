<h1 align="center">Virtual environments in Python with the <em>venv</em> module</h1>

<br />

# Table of contents

1. [Introduction](#Introduction)
2. [How to create a virtual environment](#how-to-create-a-virtual-environment)
3. [About the subfolders created with `python -m venv .myenv`](#about-the-subfolders-created-with-python--m-venv-myenv)
4. [How to activate/deactivate a virtual environment](#how-to-activatedeactivate-a-virtual-environment)
5. [Code example](#code-example)
6. [Techs used in this tutorial](#techs-used-in-this-tutorial)

# Introduction

This tutorial shows how to create and activate a **virtual environment** in *Python* using the built-in module ***venv*** (check its [documentation here](https://docs.python.org/3/library/venv.html)).

I recommend using a Python stable version equal to or higher than 3.10 in your projects.

My preferred terminal is GitBash, which allows me to write most Linux commands in my Windows Operational System (OS). Thus, some commands shown here might need to be adapted to your other favorite terminals and OS. 

# How to create a virtual environment

1. In your terminal, create a folder for your new project (you can skip this step if your project folder already exists). I will call mine `my_project_folder`:

>  ```mkdir my_project_folder```

2. Move inside the folder:

>  ```cd my_project_folder```

3. Run the command below to create the virtual environment.  I will call mine `.myenv`, but you can name it whatever you want:

>  ```python -m venv .myenv```

The last command will take a little longer to finish running. Then a new folder `.myenv` (or whatever you called it) will be created inside your project folder. The `.myenv` folder has all the virtual environment files you need, including a copy from the Python version linked to the `python` alias you used in the command `python -m venv .myenv`.

# About the subfolders created with `python -m venv .myenv`

1. In Windows, the `.myenv` directory will have the following subfolders:

    i. `Include`

    ii. `Lib`
 
    iii. `Scripts`

2. In my Linux Ubuntu 20.4 (running in WSL), the following subfolders were created:
  
    i. `bin`
  
    ii. `include`
  
    iii. `lib`
  
    iv. `lib64`
    
    v. `share`

I recommend that you explore these subfolders in the future, especially checking where the Python local version for the virtual environment is installed and where the future modules, to be installed with `pip` when the virtual environment is activated, will be saved inside the `.myenv` structure.

A very important note is that both the `Scripts` folder (in Windows) and `bin` (in Linux) are very similar and contain the files that will be used later to activate and deactivate the virtual environment.

# How to activate/deactivate a virtual environment

1. To activate a virtual environment, choose the correct command for your OS and terminal, provided in the table below, where `<env>` must be replaced by your virtual environment folder name.

<br />
<div align="center">

Plataform  | Shell | Command to activate virtual environment
--- | --- | ---
POSIX | bash/zsh | $ source \<venv\>/bin/activate
&nbsp; | fish  | $ source \<venv\>/bin/activate.fish
&nbsp; | csh/tcsh | $ source \<venv\>/bin/activate.csh
&nbsp; | PowerShell Core | $ \<venv\>/bin/Activate.ps1
Windows | cmd.exe | C:\\> \<venv\>\Scripts\activate.bat
&nbsp; | PowerShell | PS C:\\> \<venv\>\Scripts\Activate.ps1
&nbsp; | GitBash | source \<venv\>/Scripts/activate
    
</div>
<br />
    
This table was copied from the [venv documentation](https://docs.python.org/3/library/venv.html), with the addition of the command for GitBash. Notice how this last one is very similar to their Linux counterparts, but it looks for the `activate` executable inside the `Scripts/` folder instead of `bin/`.

2. After running the correct activate command, your virtual environment name will appear between parentheses on your command line prompt (check the image example below in the [code example](#code-example) topic).

3. To deactivate a virtual environment, just run this command:
> ```deactivate```
    
**Important note 1**: The virtual environment will be activated only in your current terminal tab. If you want to work in multiple terminal tabs, don't forget to activate the virtual environment there too.
    
**Important note 2**: no third-party modules will be installed inside your virtual environment. So, use `pip install <package_name>` or `pip install -r requirements.txt` to install the packages you need.

# Code example
  
<p align="center">
    <img align="center" src="terminal_commands.png" alt="example code" width="850px" />
</p>

# Techs used in this tutorial

* Python 3.10.2
* venv module
* Gitbash
* pip
