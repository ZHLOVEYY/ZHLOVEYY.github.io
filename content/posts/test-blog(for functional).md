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

I love obsidian, I love open-source 
## test
- store pic and display

![123](static/images/Pasted%20image%2020260201133559.png)
![](static/images/Pasted%20image%2020260201134155.png)

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

