## What This Is

Following the Same Error From nes-py, the gym-super-mario-bros repo forces installation of nes-py directly from the repo which does not work on mac m1. This repo fixes that issue by deleting the dependency requirement of nes-py, so that means that this repo WILL NOT WORK unless one has already installed nes-py. Assuming one is using a mac computer with the m1 processor, first check out my gym-super-mario-bros-macm1 repo to download nes-py. Once you follow those instructions, come back here to install gym-super-mario-bros.

## Installation

```shell
pip install git+https://github.com/ei5uke/gym-super-mario-bros-macm1
```

## To Check

Once you install, and follow the code given on gym-super-mario-bros pypi page, you should see the game pop up through python. However, it may cause an error that looks like this: 
``` shell
AttributeError: dlsym(0x100da7d80, class_getMethodImplementation_stret): symbol not found. 
```
In this case, one should install pyglet through this:
``` shell
pip install --user --upgrade git+http://github.com/pyglet/pyglet@pyglet-1.5-maintenance
```
This is the solution given in this GitHub discussion: https://github.com/pyglet/pyglet/pull/335 with the title: "Skip functions marked as OBJC_ARM64_UNAVAILABLE."