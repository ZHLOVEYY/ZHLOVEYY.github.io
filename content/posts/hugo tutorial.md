---
title: hugo tutorial
description: my tutorial of setting up my blog center
date: 2026-02-01T02:45:56.914Z
preview: ""
draft: false
tags: []
categories:
    - IT
---
## basic setting 
use mac homebrew to install hugo
``` bash
brew install hugo
hugo new site my-game-dev-blog
cd xx & git init
hugo new posts/my-first-godot-tutorial.md # test for create a post

# add mod
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod

in "hugo.toml" set ` theme = 'PaperMod' # Replace with your topic name.`

hugo serve 
hugo serve -D (will see draft = true posts)

```


set github Actions in github follow the instruction of official website guide：
https://gohugo.io/host-and-deploy/host-on-github-pages/ 

use `Front Matter` extention in VScode to easily manage your post

use `obsidain` to write the posts, set pic url to static/ 
close wiki link and path start from the vault

see my setting:https://github.com/ZHLOVEYY/ZHLOVEYY.github.io
main file:
- render problem: see /layouts/_default/_markup/reder-image.html
- config: hugo.toml can set your own configuration
- github Action: in /.github/workflow


concept reminder：
- in /public the file will be rebuilt so you can't store anything
- the render in  render-image.html is to correct the Path concatenation in github action which will use the ‘base_URL’ in hugo.toml
- iamge converte plugin in obsidian have an impact on the path setting of original obsidain so turn it down



## test part
- store pic and display

![123](static/images/Pasted%20image%2020260201133559.png)
1. code insert test
``` gdscript
extends CharacterBody2D

@export var speed = 300

func _physics_process(delta):
    var direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    
    velocity = direction * speed
    move_and_slide()
    
    # 朝向鼠标（可选）
    look_at(get_global_mouse_position())
```

