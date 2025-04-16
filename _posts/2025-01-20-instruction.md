---
layout: post
title: Vscode Instruction
date: 2024-01-20 08:57:00-0400
description: an example of a blog post with jupyter notebook
tags: formatting jupyter
categories: sample-posts
giscus_comments: true
related_posts: false
---

-p 选项表示 "parents"，用于创建父目录。如果指定的路径中包含不存在的父目录，-p 选项会自动创建这些父目录。这样可以避免手动逐级创建目录的麻烦。

* github.io 网页的本地编辑 （使用docker）： docker compose up  
* sphinx的本地编辑： 

VScode python调试的launch.json的写法。特别注意 路径 以及调试的arg的书写方式。

{
    // 使用 IntelliSense 了解相关属性。 
    // 悬停以查看现有属性的描述。
    // 欲了解更多信息，请访问: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python 调试程序: 当前文件",
            "env": {
                "PYTHONPATH": "${workspaceFolder}/HarmonicMapHeatFlow/core:${workspaceFolder}/HarmonicMapHeatFlow"
            },
            "type": "debugpy",
            "args": [
                "/home/jiashhu/HarmonicMapping/HarmonicMapHeatFlow/exp_param_set/linear_imp/gauss/stationary/Q2H1/Q2_H1.json"
            ],
            "request": "launch",
            "program": "${file}",
            "console": "integratedTerminal"
        }
    ]
}

Vscode中的jupyter notebook中的运行并跳转到下一行的命令的快捷键和python的快捷键冲突了。修改方式：

Cmd+K + Cmd+S 打开快捷键编辑
搜索shift + enter
如果两者有冲突，可以设置python下的when条件：增加 !notebookEditorFocused 
来表明python的命令不适用于 notebook Editor的使用时。 

