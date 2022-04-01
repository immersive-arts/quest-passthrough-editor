# Quest Passthrough Editor

![alt text](README_Pictures/PassthroughEditor.png)

## Introduction
The [Quest/2 passthrough](https://developer.oculus.com/documentation/unity/unity-passthrough/) functions allow developers to create mixed reality experiences and games by integrating the camera image of the VR headset. There are multiple options to customize the black and white camera feed. However, the changes only apply in a new build, which means you have to switch back and forth between the editor and the build. This simple UI editor allows you to change and create multiple passthrough settings directly in your build and save it as a JSON configuration. Later this configuration can be added to the Unity Project and will be applied on startup.

## Process
Build an APK of this project or implement it into your existing project. Install and run the application and create multiple passthrough presets. Use [Android File Transfer](https://www.android.com/filetransfer/) to copy the saved JSON config from your headset to your computer. The JSON config on the quest/2 is stored under the following path: `Android/data/com.companyname.appname/files/PassthroughData.json`

Replace the newly created JSON with the JSON of your unity editor on the [presistent data path](https://docs.unity3d.com/ScriptReference/Application-persistentDataPath.html). When changing into the play mode of the Unity editor, the new configuration is loaded from your JSON config and you can write it to the `OVRPassthroughLayer.cs` component by selecting the specific preset in the game UI. While in play mode, use `copy component` to copy the data. After that stop the play mode and paste the copied data onto the component to store it permanently.

![alt text](README_Pictures/UnityEditor.png)


## Repository
This Unity project has been developed and tested with Unity 2020.3.13f1.
Import the [Oculus Integration](https://assetstore.unity.com/packages/tools/integration/oculus-integration-82022) from the asset store in to this project.

# Licenses

All code is licensed under ![CC-BY](https://i.creativecommons.org/l/by/4.0/88x31.png).

# Credits

Created by the [IASpace](http://immersive-arts.ch), Zürich University of the Arts, Switzerland.
* Chris Elvis Leisi - Associate Researcher at the Immersive Arts Space
