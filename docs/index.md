# Unity Guide

### Introduction
This Guide is intended for people new to the Unity Game Engine, focused on Term 1 CST students looking to gain a base level of familiarity with game engines and early knowledge of object-oriented programming fundamentals. By the end of this guide, you should have a game scene ready for use and expansion, including a scriptable player and camera object.

> Unity is a popular game engine, used by many developers to create games such as *Rust* and *Hollow Knight*.

### Milestones
In this guide, you will:

- [Create a new Unity Project](Project-creation.md).
- [Prepare the enivronment/scene and player object](Scene-creation.md).
- [Add basic movement script to the player object](player-script.md).
- [Add basic camera script to go along with the player object](Mouse_Look.md).


### Prerequisites
To follow along, this guide requires that you have:

- A Windows 11 (22h2 or newer) capable computer that meets the minimum specs for Unity ([System requirements](https://docs.unity3d.com/6000.4/Documentation/Manual/system-requirements.html))
- Unity hub and Unity Editor version 6.4 installed on your computer (**This guide will not cover installation**)
- An IDE compatible with Unity (This guide will use Visual Studio Code)


### Typographical Conventions

1. Code is shown like this:

    ```csharp
    float speed;
    if (Input.GetKey(KeyCode.LeftShift)) {
        speed = sprintSpeed; 
    }
    else {
        speed = walkSpeed; 
    }
    ```
    
2. Specific code from the codeblocks are shown as such:

    `Input.GetKey()` checks for a specific key press

3. Actions you need to perform, and menu items are bolded:

    **Select Transform** to change the scale

4. Button items are surronded by quotations:

    "Add Project" to add a project 




### Admonitions Used
Throughout this documentation, we will use message blocks to grab your attention. Each possible message block, from most important to least important:

!!! warning 
    used to warn the reader for possible errors.
!!! Success 
    Used to indicate that you did something right!
??? tip
    Used to give useful information that might aid the reader
??? question
    Used to answer any question the reader may have



