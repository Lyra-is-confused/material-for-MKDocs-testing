# Unity Guide

### Overview
The Unity Game engine is one of the most popular game engines for hobbyist and indie developers. It's a free liscenced software for hobbyists, and is often an aspiring game developer's first exposure to object-oriented Programming. it uses the C# language along with many Unity-exclusive add-ons for it. Unity is relatively user-friendly, and has been used by many developers to create all sorts of games: 3D titles like *Rust*, 2D titles like *Hollow Knight*, and even VR titles such as *Rumble* or the *I Expect You to Die* series.


### Is this guide for you?
This Guide is intended for people new to the Unity Game Engine, focused on Term 1 CST students looking to gain a base level of familiarity with game engines and early knowledge of object-oriented programming fundamentals. By the end of this guide, you should have a game scene ready for use and expansion, including a scriptable player and camera object.

### Milestones
In this guide, you will:

- [Create a new Unity Project](Project-creation.md).
- [Prepare the enivronment/scene and player object](Scene-creation.md).
- [Add basic movement script to the player object](player-script.md).
- [Add a basic movement script to the player object](player-script.md).
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

2. Actions you need to perform are bolded:

    **Select Transform** to change the scale

1. Buttons and menu options are italicized:

    click *Add Project* to add a project 

1. File Paths are marked in blockquotes:

    > C:\users\\[name]\





### Admonitions Used
Throughout this documentation, we will use message blocks to grab your attention. Each possible message block, from most important to least important:

!!! warning 
    used to warn the reader for possible errors.
!!! Success 
    Used to indicate that you did something right!
!!! tip
    Used to give useful information that might aid the reader
!!! question
    Used to answer any question the reader may have



