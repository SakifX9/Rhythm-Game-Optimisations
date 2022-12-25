The following guide assumes that you are installing Voicemeeter for the first time, if you have an existing installation you can scroll further down.

Install Voicemeeter Banana from https://vb-audio.com/Voicemeeter/banana.htm

Run Voicemeeter Banana

![image](https://user-images.githubusercontent.com/16516667/208906942-f8f933b9-743f-43bf-9854-c2a1fdaa5133.png)

If your audio interface or sound card supports ASIO then continue with the ASIO Guide, if you aren't sure search up your device name + ASIO driver on google and check if your device is compatible with ASIO as it makes things a lot easier 
https://github.com/SakifX9/Rhythm-Game-Optimisations/edit/main/Voicemeeter/How%20to%20setup%20Voicemeeter%20for%20Rhythm%20Games.md#asio

IF your device does not have support for ASIO then you can continue with then follow the WASAPI Guide
https://github.com/SakifX9/Rhythm-Game-Optimisations/edit/main/Voicemeeter/How%20to%20setup%20Voicemeeter%20for%20Rhythm%20Games.md#wasapi-exclusive

# ASIO
Press A1 and select the ASIO output for your device 

![image](https://user-images.githubusercontent.com/16516667/208910420-fd020973-fafc-4705-bdd5-f4af044fde44.png)

Go to your Windows Audio settings and head to the Playback tab. Disable the device that you are using for ASIO in the Windows Audio Control Panel

![image](https://user-images.githubusercontent.com/16516667/209463005-207c2119-be97-488b-86ec-b008805f0ae6.png)

If you are using a mic with your audio interface you may see Hardware Input 1 be occupied by "A1 ASIO Input"

![image](https://user-images.githubusercontent.com/16516667/209463023-3988b429-9946-49c5-9e2f-be719b2b7a9c.png)

If that is the case also disable your device in the Recording tab in the Windows Audio Control Panel and set VoiceMeter Output as your default recording device

![image](https://user-images.githubusercontent.com/16516667/209463063-4e1705b5-c909-45d5-b634-fed5e051bd29.png)



Press Menu > System Settings 

Set Buffering ASIO to 128 samples

![image](https://user-images.githubusercontent.com/16516667/208909916-f916a9af-b008-4657-a4b4-5872d15a79de.png)




# WASAPI Exclusive 



