# How to get started with this repo

1. Install pixi https://pixi.sh/dev/installation/
2. Clone this repo
3. navigate to the project folder you want (example)
4. run the start command with pixi 
```pixi run start```
5. a jupyter notebook should start

# To play around with this yourself

1. Install pixi https://pixi.sh/dev/installation/
2. Fork this repo
3. play around with pixi (init a new project and play)

This follows the workshop presented here: https://carpentries-incubator.github.io/reproducible-ml-workflows/pixi_intro.html

## Commands to get going

1. Update pixi
```pixi self-update```
2. Create a new project
```pixi init <folder-name>```
3. Add python to the lock file (we can add packages this way too)
```pixi add python```

You can also:

- clean your enviroment.
```pixi clean```
- install the default environment (and solve any unsolved changes to the .toml)
```pixi install```
- check the things that are installed
```pixi list```
- add additional dependencies
```pixi add numpy notebook jpyterlab```
- add a *task* (*pixi task add <task_command> <terminal_command>*)
```pixi task add lab "jupyter lab" --description "Launch JupyterLab"```
- to run this task
```pixi run lab```
- the *start* task is the expected starting point
```pixi task add start "" --depends-on lab```
- now we can run the default way to begin in this project. This will run *pixi run lab*, because this empty string command depends on it, and then an empty string command.
```pixi run start```
- more commands are available in the documentation https://pixi.sh/latest/getting_started/

When there are changes, we need to install
```pixi install```

After tasks are completed, it is easy to see what there is to do with this project:
```pixi task list```

## CUDA

- Adding a system requirement
```pixi workspace system-requirement add cuda 12```
- Setting up cuda for linux only (add cuda to the platform linux-64)
```pixi add --platform linux-64 cuda```
- Get pytorch (get gpu for linux)
```pixi add pytorch-gpu --platform linux-64```
- Fake as if I have cuda (run whatever command, like *pixi add pytorch-gpu*)
```CONDA_OVERRIDE_CUDA=12 pixi info```
- Get pytorch cpu for all other platforms
```pixi add pytorch-cpu``
