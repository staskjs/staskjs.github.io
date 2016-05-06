---
layout: default
permalink: /ctrlh
---

I am constantly using Vim as my main editor and I also recently integrated tmux into my workflow.
Usually I work through ssh on a VPS and I use mobaxterm on one of my computers.

I have encountered a problem with Ctrl-H key binding. In my Vim it is mapped to Previous buffer, so I use it constantly,
but tmux interprets that as a Backspace.
It has something to do with legacy support for Backspace key which was `^H`, but now `^?` is a standard, from what I understand.

After some googling I found a solution that worked for me. Just put `stty erase '^?'` inside your `.bashrc` or `.zshrc` 
or whatever else you use to remap Backspace to what it should be.
