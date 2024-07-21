# Introduction to Poseidon

## Today's goals

* Learning HPC basics
* Log-in via ssh
* Working on HPC with command lines
* Editing files via Vim
* Job submission via Slurm
* Hand-on example: Submitting a demo Matlab script via Slurm

*Disclaimer: This tutorial is aimed to be a guideline to help you start working on Poseidon. It might not have elaborated descriptions or definitions, but I will try to give as much resource to read after the class on your own as I can!*

### 1. Logging in to Poseidon

Start your command-line application, e.g., Terminal (MacOS), Windows terminal (Windows), etc. Type in `ssh` command as below (SSH = Secure Shell, Secure Socket Shell).
`ssh <username>@poseidon.whoi.edu`

Pro tips:
- Options can be added after ssh to make it has extra function. For example, I add -Y (or -X) to allow ssh to open my display if I want to see some result via `ncview`. (See on-screen demonstration.)

  `ssh -Y <username>@poseidon.whoi.edu`

- Poseidon has 2 login nodes: l1 and l2. We can select which node we would like to login. (Normally it's not needed, but in some case it might.)

    `ssh -Y <username>@poseidon-l1.whoi.edu`   `ssh -Y <username>@poseidon-l2.whoi.edu`
