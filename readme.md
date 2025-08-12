# How to get started

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
- install the default environment
```pixi install```
- add additional dependencies
```pixi add numpy notebook jpyterlab```
- add a *task* (*pixi task add <task_command> <terminal_command>*)
```pixi task add lab "jupyter lab" --description "Launch JupyterLab"

