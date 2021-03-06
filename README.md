<h2 style="line-height:2;"><a>NexPlayer™ for Unity</a><a href="https://www.nexplayersdk.com/contact?utm_source=github&utm_medium=organic&utm_campaign=unity&utm_content=20200901--unitycontactbutton" target="_blank"><img  src="https://github.com/NexPlayer/NexPlayer_Unity_Plugin/blob/master/resources/Button%20Demo.png" width="23%" height="10%" alt="Unity video player" align="right"></img></a></h2>

</br>

![NexPlayer Unity Video Streaming Player Plugin](resources/Big%20Buck%20Bunny%20Demo.gif)

NexPlayer™ for Unity is a multiscreen video streaming player for Unity apps that supports both standard and 360 video playback across all Android, iOS and PC devices. NexPlayer™ for Unity is the only playback solution for Unity that supports HLS &amp; DASH live streaming with Widevine DRM across all Android & iOS devices.

This repository contains the NexPlayer™ Unity video streaming player plugin features list as well as an integration guide. If you want to get a copy of our fully working demo, contact us at our [website](https://www.nexplayersdk.com/contact?utm_source=github&utm_medium=organic&utm_campaign=unity&utm_content=20190918--unity).

## Table of Contents

* **[Features](#features)**  

* **[Supported Platforms](#supported-platforms)**

* **[Demo Installation Guide](#demo-installation-guide)**
 
 <br>
 
<p align="center" style="border-style:solid"><a rel="noopener noreferrer"><img src="https://github.com/NexPlayer/NexPlayer_Unity_Plugin/blob/master/resources/Interactivity2.gif" style="max-width:100%;" height="250"></a> <a rel="noopener noreferrer"><img src="https://github.com/NexPlayer/NexPlayer_Unity_Plugin/blob/master/resources/Cube_Demo.gif" alt="NexPlayer for Unity Video Player Sample Interface" style="max-width:70%;" height="250"></a></p>

<p style="margin-left:auto;margin-right:auto" width="300px" align="left">Our Unity video plugin allows for additional interactivity within your Unity projects. With our plugin, you can use in-game actions and objects to modify video content.</p>

## Features

The NexPlayer™ for Unity video streaming player plugin contains the latest features. As our Unity video plugin is developed entirely in-house, we can implement any desired functionalities. 

We support the following features:

- Overview
    - Unity Versions 2017 or Higher
    - HLS & DASH Streaming with ABR (Adaptive Bitrate)
    - Widevine DRM on Local Playback and Streaming   
    - Low Latency Live Streaming
    - Up to 4K Ultra High Definition (UHD) Resolution
    - Rendering Videos in 2D & 3D Objects
- Basic Features:
    - Play / Pause
    - Seek
    - Audio Volume Adjustment
    - Loop Playback
    - Configurable Aspect Ratio
    - Portrait / Landscape Orientation
- Advanced Features:
    - Adjustable Buffering Time
    - Offline Streaming Playback for HLS & DASH    
    - SRT, SMI, & WebVTT Subtitles & CEA-608/708 Closed Captions 
    - Multiple Audio & Subtitle Track Selection
    - Content Information and Statistics (Audio & Video Bitrate, Codec, Average FPS, and More)
    - Transparency and Chroma Support
- 360 Video Playback and Virtual Reality (VR)
    - Touch input which includes movement, and camera rotation
    - Gyroscope input to move the camera
    - Mouse input to move the camera
    - Automatic Ground Leveler to stabilize the video
    - Custom shaders to map 2D, 3D Over/Under and 3D Left/Right 360 videos
    - Compatible with VR libraries for Unity (Google Cardboard, Vive & Oculus)

## Supported Platforms

| Platform | Supported Graphics APIs | HLS | DASH | Local | Inside App (Streaming Assets) |
| :-----:| :-----:| :-----:| :-----:| :-----:| :-----:|
| Android  | OpenGLES2, OpenGLES3 | O | O | O | O |
| iOS | Metal | O | O | O | O |
| Windows | DirectX11 | O | O | O | O |

## Demo Installation Guide

#### 1) Play standard video

Create a new [Unity](https://unity3d.com/) project and import the NexPlayer™ Unity video streaming player plugin.

![NexPlayer Plugin](resources/import_package.png)

In order to load the player [Scene](https://docs.unity3d.com/Manual/UsingTheSceneView.html) follow the path: 'Assets/NexPlayer/Scenes' and open 'NexPlayer_RawImage_Sample.unity' by double clicking.
Test the playback by selecting the play button in the editor.

![NexPlayer Plugin](resources/playback_demo1.png)

#### 2) Play a 360 scene

Load the 360 Video [Scene](https://docs.unity3d.com/Manual/UsingTheSceneView.html) available in 'Assets/NexPlayer/NexPlayer360/Scenes/NexPlayer360.unity'.
Test the playback by selecting the play button in the editor.

![NexPlayer Video Streaming Player Plugin](resources/360_scene.gif)

#### 3) Load NexPlayer™ demo

Add the following scenes to the Unity build:

- Assets/NexPlayer/Scenes/MainMenu.unity
- Assets/NexPlayer/Scenes/NexPlayer_ChangeRenderMode_Sample.unity
- Assets/NexPlayer/Scenes/NexPlayer_MaterialOverride_Sample.unity
- Assets/NexPlayer/Scenes/NexPlayer_PlaybackMultipleRenderer_Sample.unity   
- Assets/NexPlayer/Scenes/NexPlayer_PlaybackSetting_Sample.unity
- Assets/NexPlayer/Scenes/NexPlayer_RawImage_Sample.unity   
- Assets/NexPlayer/Scenes/NexPlayer_RenderTexture_Sample.unity   
- Assets/NexPlayer/Scenes/NexPlayer_Transparency_Sample.unity   
- Assets/NexPlayer/Scenes/NexPlayer_VideoSpreadRenderTexture_Sample.unity 
- Assets/NexPlayer/NexPlayer360/Scenes/NexPlayer360.unity

Switch to the desired platform.

![Load Demo](resources/unity_scene_setup.png)


#### 4) Configuration steps

Manually select the compatible graphics APIs in the "Player Settings" section of Unity for each platform.

#### Android platform:

- To allow the application to have internet access for streaming videos, select the "Require" value for the "Internet Access" option in the Unity player settings.
- Set "Write Permision" to External (SDcard)
- Make sure to set a specific app ID under "Package Name" as required by Unity before compiling your application.

#### iOS platform:

- To view HTTP videos, enable "Allow downloads over HTTP" option.
- After compilation, in XCode make sure to set a "Signing Team."
- Under embedded binaries, click the "Plus" button and add:
   - widevine_cdm_sdk_release.framework
   - WidevineIntegration.framework

A quick and easy way to enable these settings is by using the helper component
(NexEditorHelper.cs). If the helper component NexEditorHelper.cs is attached to any GameObject, it will include a graphics UI to
auto detect any conflict regarding the graphics API, and it will promptly solve it.

-------------------


## Contact
[supportmadrid@nexplayer.com](mailto:supportmadrid@nexplayer.com)
<br>+34 914 184 356
