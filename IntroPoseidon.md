# Introduction to Poseidon - Hands-on experience

## Today's goals

* Learning HPC basics
* Log-in via ssh
* Working on HPC with command lines
* Editing files via Vim
* Job submission via Slurm
* Hands-on example: Submitting a demo Matlab script via Slurm

*Disclaimer: This tutorial is aimed to be a guideline to help you start working on Poseidon. It might not have elaborated descriptions or definitions, but I will try to give as much resource to read after the class on your own as I can!*

## Part 1: Preparation

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

### 3. Basic operations via command lines

3.1 `pwd` : Print working directory. Print out full path showing where we are. When first signed in, it should be `/vortexfs1/home/<username>`

  `pwd`

3.2 `mkdir` : Make directory. We will create a directory in our home directory for using in this class.

  `mkdir mathreview2024`

3.3 `cd` : Change directory. We will change our working directory to the one we have just created.

`cd mathreview2024`

### 4. Clone class materials and .tar.gz extraction.

4.1 Make sure that we are in the right directory. Then clone this whole github repository to your Poseidon's `mathreview2024` directory.

    `git clone https://github.com/phadtaya/MITWHOI-ApplCoding.git`
    

4.2 Change directory to the newly cloned `MITWHOI-ApplCoding`. List the contents of the directory. Look for the .tar.gz file (tarball).

`ls` or `ls -l, ll`

My favorite one: `ls -ltrh`

4.3 Extract the tarball. Change directory to `poseidon_codes` directory.

    `tar -xzvf poseidon_codes.tar.gz`


This command will extract the tar ball. Tips: When want to create a tarball (with GZip compression), use `tar -czvf <filename>.tar.gz <dirname>`. If seeing `.tar` files (without `.gz`), do the same without `-z` option in the command.

Now, we have the demo codes ready!

*Commands we have learned: `ssh` login, `pwd`, `cd`, `mkdir`, `ls`, `module` commands, `git clone`, `.tar` and `.tar.gz` extraction and creation*

## Part 2: Job submission

### 5. Read and prepare our MATLAB codes with Vim text editor.

5.1 Open the file.

`vi hello_world.m`

Tips: Type `vi h` + press `tab` to get the full filename.

5.2 Edit the file to display the texts you want.

### 6. Explaning `job.slurm`, a Slurm job submission script.

Slurm is the job scheduler used on Poseidon. To run any job (except code compiling) on Poseidon, we have to submit it via Slurm and wait in the queuing system.

6.1 Line-by-line explanation & editing the file.

`vi job.slurm`

### 7. Job submission

`sbatch job.slurm`


### 8. Check status

`squeue -u <username>`

### 9. Check output

### 10. Your turn now!

To do:

* Open the `Testplot_20240722.m`. Read it through, change the function and output filename to your desired filename. Save and exit the file.
* Open `job.slurm` and edit the command to run this matlab script. Save and exit.
* Submit the job.
* Check for the results.

### 11. Learn about Go... > Connect to server (mac)

















