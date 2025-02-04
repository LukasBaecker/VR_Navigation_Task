# Comparing 2D and 3D Sketch Maps in Virtual Reality
This repository contains the Unity-project and all important analysis steps from my Masterthesis "Comparing 2D and 3D Sketch Maps in Virtual Reality" written at the [Institute for Geoinformatics](https://www.uni-muenster.de/Geoinformatics/).

## Abstract 
The aim of this thesis is to compare 2D and 3D Sketch Maps
...more to follow

## Software and Versions
  * Blender 3.4.1
  * Unity 2021.3.10f1
    * with XR Interaction Toolkit 2.0.4 
  * Meta Quest with System ...
  * R Studio 2023.03.1+446
  * R 4.3.0
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
  
### How to install the navigation app of the study on your Meta Quest 2
When the project is set up the following steps need to be done to use the app on our Quest 2:

  * Download the Meta Quest Mobile App and login with the admin account on your Quest 2.
  * They Quest 2 and the phone should be in the same Wifi and the connection to the app should be straight forward.
  * In the app click on the Meta Quest 2 and open the headset-settings. Here you can enable the developer mode of the glasses.
  * Now you can connect the Quest 2 to your computer via USB.
  * Looking into your Quest 2 you will get a message you need to accept when connecting to the PC.
  * In Unity with the project opened go to File -> Build Settings (Ctrl+Shift+B)
  * Under "Run Device" click "Refresh" and select the Meta Quest 2 in the dropdown menu.
  * Optional: change settings as you wish (without warranty) like for example under "Player Settings..." you can change the "Product Name" that will be shown as the app's name on the Meta Quest 2.
  * Click "Build and Run", safe the apk on your computer with a recognizable name even if the game will be build and run on the glasses directly.
  * Your app will automatically run on your device but it can also be found anytime in your installed apps. set the filter for "unknown sources" and you will see your app with the project name you set. 
  
### Note this
In the project you will find all assets, skripts and settings I set up for my user study. Following are the most important aspects explained:
  * The assest used, are partly build on my own with Blender and partly downloaded as free assets with CC-licence (check out for example the assets from the [School Rooms Collection](./project/Assets/SchoolRooms)). The main model can be found in the [/Assets/Masterthesis subfolder](./project/Assets/Masterthesis) which was created with Blender. I finalized it in Unity why the fbx file differs from the final model. When putting it into a scene, It can be unpacked and modified this way.
  * The [/Assets/Scenes subfolder](./project/Assets/Scenes) contains the training scene and the study scene that both could be modified or also more scence (as a menu scene) could be added. The scene order can be changed in the Build setting window. The navigation between different scenes was realised with a script that lets a player changes the scene when colliding with a trigger.
  * The scripts can be found at [/Assets/Scripts](./project/Assets/Scripts). The above mentioned [ChangeScene Script](./project/Assets/Scripts/ChangeScene.cs) could be adapted to any object with a trigger and lead a player into a scene with a setable index. The other scripts are part of the navigation task and adding logic to the two buttons for show/hide the navigation-stripes, show the next stripe on the route and how the button at the end of the route behaves. When repositioning the buttons their coordinates have to be changed in the scripts. Also when changing the route the segments have to be changed accordingly.
  * The settings are optimized for the Android OS of the Meta Quest 2
  * The project may contain packages that I did not deleted, are not used in the final results but were dowloaded at a point.

## Analysing Study Results
The [analysis subfolder](./analysis) contains all tools that I needed to analyse the study result as part of my masterthesis. It also contains a R-markdown file to follow the analysis step-by-step.

### How to setup the analysis
To re-construct the analysis, download the described R and R-Studio versions to avoid errors and open the analysis folder in a new project. Now start the R-markdown file and run the code. There might be errors installing packages. Make sure that all the used packages are running and you should not have any errors. Enjoy.

## 3D Assets Attribution
Low Poly Shark by IsabelleDotJpeg ([at sketchfab](https://sketchfab.com/3d-models/low-poly-blahaj-5ac23e0cd44d49dcaaa14967f7d7a778))
Low Poly Car by Creative Mango ([at sketchfab](https://sketchfab.com/3d-models/low-poly-car-93971323324243468f24d7da9d18f617))
Stuffed rhino toy low poly by assetfactory ([at sketchfab](https://sketchfab.com/3d-models/stuffed-rhino-toy-low-poly-f5251aad48af4eae8bcccad6217fc5a6))
Cat - PS1 Low Poly (Rigged) by Wersaus33 ([at sketchfab](https://sketchfab.com/3d-models/cat-ps1-low-poly-rigged-78d863ba43b34a6c9fdd6c61dbf5776f))
Stuffed sheep toy low poly by assetfactory ([at sketchfab](https://sketchfab.com/3d-models/stuffed-sheep-toy-low-poly-13c1fb8edb994f69a84a94c3d31e63a7))
