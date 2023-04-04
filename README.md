# Comparing 2D and 3D Sketch Maps in Virtual Reality
This repository contains the Unity-project and all important analysis steps from my Masterthesis "Comparing 2D and 3D Sketch Maps in Virtual Reality" written at the [Institute for Geoinformatics](https://www.uni-muenster.de/Geoinformatics/).

## Abstract 
The aim of this thesis is to compare 2D and 3D Sketch Maps
...more to follow

## Unity VR-Navigation Project
The [project](./project) subfolder contains the Unity project for a VR navigation task of my study.

This project can be used to be rebuild and used with other environments for VR with head-mounted displays (HMD). The project is ompimized for the [Meta Quest 2](https://www.meta.com/de/quest/products/quest-2/) as a standalone HMD running with Android OS. It includes the model I used in my masterthesis "Comparing 2D and 3D Sketch Maps in Virtual Reality"

The idea of the project is, that one can put in any model and change the route as they wish. At the start position are two buttons: one (the green one) that activates the first part of the route and one (the red one) that deactivates the whole route regardless of the state of the navigation task. Each part of the route has a box collider as a trigger that activates the following segment. the last segment activates a final button that can be pushed and filled with more logic if one wishes.

### How to set up the Unity Project
Unity Version: 2021.3.10f1

To use the Unity project follow these steps:
  * clone or download the repo
  * open the Unity Hub
  * open the [project](./project) folder and follow the instructions by Unity
  
### Note this
In the project you will find all assets, skripts and settings I set up for my user study. Following are the most important aspects explained:
  * The assest used, are partly build on my own with Blender and partly downloaded as free assets with CC-licence (check out for example the assets from the [School Rooms Collection](./project/Assets/SchoolRooms)). The main model can be found in the [/Assets/Masterthesis subfolder](./project/Assets/Masterthesis) which was created with Blender. I finalized it in Unity why the fbx file differs from the final model. When putting it into a scene, It can be unpacked and modified this way.
  * The [/Assets/Scenes subfolder](./project/Assets/Scenes) contains the training scene and the study scene that both could be modified or also more scence (as a menu scene) could be added. The scene order can be changed in the Build setting window. The navigation between different scenes was realised with a script that lets a player changes the scene when colliding with a trigger.
  * The scripts can be found at [/Assets/Scripts](./project/Assets/Scripts). The above mentioned [ChangeScene Script](./project/Assets/Scripts/ChangeScene.cs) could be adapted to any object with a trigger and lead a player into a scene with a setable index. The other scripts are part of the navigation task and adding logic to the two buttons for show/hide the navigation-stripes, show the next stripe on the route and how the button at the end of the route behaves. When repositioning the buttons their coordinates have to be changed in the scripts. Also when changing the route the segments have to be changed accordingly.
  * The settings are optimized for the Android OS of the Meta Quest 2
  * The project may contain packages that I did not deleted, are not used in the final results but were dowloaded at a point.

## Analysing Study Results
The [analysis subfolder](./analysis) contains all tools that I needed to analyse the study result as part of my masterthesis.
...more to follow

### How to setup the analysis
...more to follow
