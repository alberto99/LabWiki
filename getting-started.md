<!-- TITLE: Getting Started -->
<!-- SUBTITLE: A quick summary of Getting Started -->

# Header
The basic workflow is that you will be working from a personal computer -- and from there you will be able to log in to other machines such as Hipergator or BlueWaters that will allow you to execute programs that require a lot of computer time. We use terminal aaplications to type commands that allow us to: visualize and modify files, execute them and trasnfer them between machines. To connect between different machines we use a secure shield protocol (ssh), more on that below.


Most of our work is done in the UF supercomputer, hipergator. First thing you will need is an account.
[Hipergator Account Request](https://www.rc.ufl.edu/access/account-request/)

Once you have that you will need to learn to login from your machine to the hipergator via ssh and command line instructions [Hipergator: Getting started](https://help.rc.ufl.edu/doc/Getting_Started). 

Hipergator provides help to familiarize you with the machine:

[Hipergator Help Wiki](https://help.rc.ufl.edu/doc/UFRC_Help_and_Documentation)

Here are some of the tools you should familiarize yourself with:
**Vi/vim** -- a powerful editor of files for us in terminals.  [vim.org](https://www.vim.org/docs.php)
To run vi type `vi example_file` in a terminal.
Running the following command on a terminal will give you a basic start on using vi.
`vimtutor`

**Setting up your environment**
Your home directory contains a bunch of configuration files that help set up your environment to execute the programs you need. For example, the [.bashrc file](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) is executed everytime you log into a machine that contains that file, it can be used to load modules, export variables or create aliases. 

modules are a quick way to access the environment variables that allow you to run different versions of a program. For example, python2 or 3 will need different modules loaded. 
`module list` will let you know which modules you have available
`module available` will tell you all the possible modules you can use

It is not recommended you preload all the modules you want in your bashrc file, but rather  you load them/unload them as needed. You can save configurations for modules you typically load together. For example:

Load some modules:

```text
module load  vmd/1.9.3  
module load ufrc   
module load  globus/2.1.3   
module load  cmake/3.12.3   
module load  cuda/10.0.130  
module load  swig/3.0.8   
module load  netcdf/4.2   
module load  intel/2019 
module load doxygen/1.8.3.1  
module load  openmpi/4.0.0
```

And now save an environment, which will go to your ~/.lmod.d/ directory
`module save intel_compilers`
Next time you want these modules you can do:
```
module purge
module restore intel_compilers
```

You can do the same for accessing a different set of Modules, for example the ones i use for OpenMM/Meld with gcc compilers:
 module list

Currently Loaded Modules:
  1) vmd/1.9.3   3) globus/2.1.3   5) cuda/10.0.130   7) netcdf/4.2   9) doxygen/1.8.3.1  11) python3/3.6.5
  2) ufrc        4) cmake/3.12.3   6) swig/3.0.8      8) gcc/7.3.0   10) mkl/2018.1.163   12) openmpi/3.0.0

 **Python virtualenvironments**
Notice that i loaded a python3 environment. We use python as the main scripting language due to its readability, and availability of packages for scientific research (numpy, pyplot, pytorch, scipi, ...) 
Most python modules you load will already give you access to system installed packages, but in cases you will need to upgrade them or install new ones. Since we canno access the place where they are installed (and it would be a mess if every user could!) a much more versatile way is to create your own virtual environment.

In your home directory cereate a Source direcory where you will have your scientific sotware and make a VirtualEnvironments directory inside it.
Navigate to it. And let's create a virtualenvironment:
```
python3 -m venv --system-site-packages name_of_your_environment
#To activate your environment:
source name_of_your_environment/bin/activate
#To deactivate your evnironment:
deactivate
```


![Screenshot 2019 06 08 17 58 39](/uploads/screenshot-2019-06-08-17-58-39.png "Screenshot 2019 06 08 17 58 39")
