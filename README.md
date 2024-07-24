[STYLY for Vision Pro](https://spatial-layer.styly.cc/) supports [OSC](https://opensoundcontrol.stanford.edu/). Users can create STYLY contents receives OSC messages. This is a simple example controlling contents by OSC.

![video](./Screenshots/video.gif)

You can down load the latest version of this project via [this link](https://api.github.com/repos/ku6ryo/OSC-Sample_STYLY-for-VisionPro/zipball/).

# Controller
This demo Unity project assumes that you're using [TouchOSC iOS app](https://apps.apple.com/jp/app/touchosc-mk1/id288120394). However, you can use other OSC controllers (app, devices) in STYLY and you can learn how to realize OSC communication with this project.

## TouchOSC app settings
![app](./Screenshots/app.jpg)

 Before you start working this project, please setup TouchOSC app. Go to setting and select [Beatmachin] as the layout. Then, please set Host with your Vision Pro's local IP address (In testing phase on Unity Editor, please set your PC's local IP address.). You can keep the port number *Port (outgoing)* as the default *8000*.
 
 Following links navigates you to how to get IP address of the following devices.
 - [Vision Pro](https://www.youtube.com/watch?v=OXGVivV84zM)
 - [Mac](https://www.security.org/vpn/find-mac-ip-address/)
 
# Unity project
The content in this project is controlling Y position of a sphere by OSC.

This project uses "[OscJack](https://github.com/keijiro/OscJack)" and "[OscJackVS](https://github.com/keijiro/OscJackVS)". If you implement OSC communication faeture to your own project, please import the Unity packages first.

Please open "Receiver" Unity scene in Unity Editor. The scene is in [Assets] --> [Scenes] --> [Receiver].

![UnityEditor](./Screenshots/unity_editor.png)

In the same folder as the scene, there is a OscConnectionSetting file and a VisualScripting graph.

For the port setting in OscConnectionSetting, please use the port number you set in TouchOSC app.

![OscConnectionSettings](./Screenshots/connection_settings.png)

Please play the scene in Unity Editor and make sure that it works with TouchOSC app (Please do not forget to get your PC's IP address in TouchOSC settings.).

You can learn how to make scripting graph by checking the VisulalScripting graph.

# Other informations
- Unity version: 2022.3.27