# Introduction to Poseidon - Hands-on experience

## Today's goals

* Learning HPC basics
* Log-in via ssh
* Working on HPC with command lines
* Editing files via Vim
* Job submission via Slurm
* Hands-on example: Submitting a demo Matlab script via Slurm

*Disclaimer: This tutorial is aimed to be a guideline to help you start working on Poseidon. It might not have elaborated descriptions or definitions, but I will try to give as much resource to read after the class on your own as I can!*

### 1. Logging in to Poseidon

To connect to Poseidon, we need to be on WHOI network. To get start, open your command-line application, e.g., Terminal (MacOS), Windows terminal (Windows), etc. Type in `ssh` command as below (SSH = Secure Shell, Secure Socket Shell).

`ssh <username>@poseidon.whoi.edu`

Then, type in your password.

Pro tips:
- Options can be added after ssh to make it has extra function. For example, I add -Y (or -X) to allow ssh to open my display if I want to see some result via `ncview`. (See on-screen demonstration.)

  `ssh -Y <username>@poseidon.whoi.edu`

- Poseidon has 2 login nodes: l1 and l2. We can select which node we would like to login. (Normally it's not needed, but in some case it might.)

    `ssh -Y <username>@poseidon-l1.whoi.edu`   `ssh -Y <username>@poseidon-l2.whoi.edu`

### 2. Check and load modules

2.1 Check preloaded modules by typing  `module list`.

2.2 Check the modules available on Poseidon by typing `module avail`

2.3 Today we will be loading MATLAB. Enter `module load matlab`. (Check with `module list` to see if it's there.)

Pro tips: `ncview` demonstration

### 3. Basic operations via command lines

3.1 `pwd` : Print working directory. Print out full path showing where we are. When first signed in, it should be `/vortexfs1/home/<username>`

>> `pwd`

3.2 `mkdir` : Make directory. We will create a directory in our home directory for using in this class.

>> `mkdir mathreview2024`

3.3 `cd` : Change directory. We will change our working directory to the one we have just created.

>> `cd mathreview2024`

### 4. Clone class materials and .tar.gz extraction.

4.1 Make sure that we are in the right directory. Then clone this whole github repository to your Poseidon's `mathreview2024` directory.

>> `git clone https://github.com/phadtaya/MITWHOI-ApplCoding.git`
