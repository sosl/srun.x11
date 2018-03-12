== PURPOSE & USAGE ==

Interactive shell with X11 forwarding for SLURM.


Run srun.x11 with the usual sbatch arguments, but DO NOT give a program to run.
When your job starts, you'll find yourself usng an interactive shell which has
proper X11 forwarding enabled.


== Author & Credits ==

Scripts were written by  Pär Andersson (National Supercomputer Centre, Sweden)
and published in the SLURM FAQ.

==

After forking from https://github.com/jbornschein/srun.x11 Stefan Oslowski added
tiny tweaks to adjust these scripts for the OzStar supercomputer.

I also included a basic screenrc to slightly improve the user experience.
If you would like to use it copy it to your home directory and rename it to .screenrc:
```
mv screenrc .screenrc
```

Deploy the srun.x11 and _interactive and _interactive_screen in a directory and make sure they are executable:
```
chmod +x _interactive _interactive_screen srun.x11
```

Request interactive jobs by running, e.g.:
```
srun.x11 --ntasks 4 --time=1:0:0 --gres:gpu=1
```

to get 4 CPUs and one GPU for 1 hour
