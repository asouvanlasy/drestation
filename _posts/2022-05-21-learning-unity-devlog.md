---
layout: post
title: "Learning Unity 2D - Devlog"
---

The first year of university is over, so I'm met with an abundance of time and no direction. After struggling to bring myself to start a coding project or to learn a language, then playing the excellent 2D game *Katana ZERO*, I decided to learn Unity 2D game development.

I had used Unity for a short time modifying 3D avatars for *VRChat*, adjusting properties like scale, editing textures, adding sounds, and failing to get eye-tracking working. All of that didn't require any C# coding, but now I can use my knowledge from my C# class this year.

## Getting Started

I knew going into this that if I mindlessly followed a 4 hour long tutorial on YouTube, I wouldn't learn anything. My plan became to go step-by-step through the process, adding one feature at a time.

Thankfully, I found an great tutorial series by [Pandemonium](https://www.youtube.com/playlist?list=PLgOEwFbvGm5o8hayFB6skAfa8Z-mw4dPV) on YouTube which fit my plan. Each video is a topic in of itself and is very digestable. This style of learning is proving to be effective since I can follow an episode and add something new each day, creating a positive feedback loop.

## Roadmap

### May 16-21, 2022

![Snapshot of the game currently](https://i.imgur.com/TEDrj5G.png)

- Created the Unity project
- Created a black line as the ground and a white square as the player
- Basic movement left-right (first C# script)
- Imported a free Unity asset for player model and animations
- Player movement is animated
- Added jumping
- Added wall jumping
- Added shooting fireballs
- ~~TODO: fix fireballs behaviour~~

#### Thoughts on C# Scripting

Coding C# for Unity is surprisingly intuitive. You have the option of using VS2019 or VSC (my preference) which comes handy with IntelliSense/auto-completion. Unity's components are literally OOP "objects".

I'm by no means already a Unity syntax expert, but what I've seen so far is very approachable for a programmer with a year's worth of experience.

### May 25, 2022

![New sprite graphics](https://i.imgur.com/ftEodPn.png)

-  Added terrain and background textures

I feel like there should be a more efficient way of creating levels than copy-pasting each tile.

### May 30, 2022

![Camera follows player](https://i.imgur.com/anZPFED.gif)

- Added a following camera. It even looks ahead of the direction of movement!

### June 6, 2022

![Player dying](https://i.imgur.com/svYPfE5.png)

- Added health. Player has 3 hearts which update when damaged
- Spinning saw trap to hurt the player
- Health pickups
- Animations for getting hurt and dying
- Added sorting layers for sprites (background -> foreground -> player -> ground)

One thing that I thought was pretty cool was this getter and setter in the scripts for the player's health and healthbar.

#### HealthBar.cs
```
// Update UI to match player's current health
private void Update()
{
    currentHealthBar.fillAmount = playerHealth.currentHealth / 10; 
}
```

HealthBar needs to be able to know what the player's health is, but that variable is from Health.cs. To get around this:

#### Health.cs
```
public float currentHealth { get; private set; } // Var can be grabbed from outside, but can only be set inside this script
```

So, any file can `{get}` the player's health, but they can't `{set}` it. This matters because I don't want that variable to get modified from anywhere except here (which could lead to bugs).