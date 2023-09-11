This guide is for the people that have low latency audio devices such as DACs,Audio Interfaces and Sound Cards that have existing ASIO drivers and want to be able to play games with ASIO/WASAPI Exclusive mode while being able to hear other applications. 

If you are using this guide soley to just capture ASIO/WASAPI Exclusive audio, I suggest using a headphone jack splitter instead, way less hassle and strain on your CPU. 

Tested games(working): Sound Voltex コナステ([44.1khz configuration required](#configuring-voicemeeter-to-work-properly-for-games-that-require-441khz-audio-sound-voltex-beatoraja-etc)), Beatoraja([44.1khz configuration required](#configuring-voicemeeter-to-work-properly-for-games-that-require-441khz-audio-sound-voltex-beatoraja-etc)),  DJMax Respect V, Beatmania IIDX Infinitas ([ASIO registry hack](https://github.com/darekasan/inf_launch_ext/blob/master/asio.md] and [44.1khz configuration required](#configuring-voicemeeter-to-work-properly-for-games-that-require-441khz-audio-sound-voltex-beatoraja-etc))
If you can test games with ASIO support please let me know so I can update this list

Confirmed not working: Beatmania IIDX Infinitas(ASIO with regstry hack and WASAPI Exclusive modes don't work but if you can get it to work please tell me!)


Table of Contents
_________________

The following guide assumes that you are installing Voicemeeter for the first time.

* [Setting up Voicemeeter](#setting-up-voicemeeter) - Start here.
  * [Setting up your Audio device in the Windows Audio Panel](#setting-up-your-audio-device-in-the-windows-audio-panel)
  * [Configuring Voicemeeter with your Audio device](#configuring-voicemeeter-with-your-audio-device)
  * [Configuring Voicemeeter to work properly for games that require 44.1khz audio (Sound Voltex, Beatoraja etc)](#configuring-voicemeeter-to-work-properly-for-games-that-require-441khz-audio-sound-voltex-beatoraja-etc)
* [Configuring Voicemeeter with a rhythm game](#configuring-voicemeeter-with-a-rhythm-game)
  * [Configuring a rhythm game with ASIO](#configuring-a-rhythm-game-with-asio)
  * [Configuring a rhythm with WASAPI Exclusive](#configuring-a-rhythm-with-wasapi-exclusive)
* [Configuring Voicemeeter with OBS](#configuring-voicemeeter-with-obs) 
  * [Configuring OBS to work with 44.1khz audio](#configuring-obs-to-work-with-441khz-audio)


# Setting up Voicemeeter

Install Voicemeeter Banana from https://vb-audio.com/Voicemeeter/banana.htm

Run Voicemeeter Banana

![image](https://user-images.githubusercontent.com/16516667/208906942-f8f933b9-743f-43bf-9854-c2a1fdaa5133.png)

## Setting up your Audio device in the Windows Audio Panel

Open up your Windows Audio Panel

Set Voicemeeter Input to the default audio device and Voicemeeter AUX Input to default communication device


![image](https://user-images.githubusercontent.com/16516667/215765846-cc75ec05-3b64-425a-9db1-d848363951d6.png)
![image](https://user-images.githubusercontent.com/16516667/215778527-a48b9860-b993-4bef-afac-4cfeca574eab.png)

Use the Windows Volume Mixer to move your Communication(Discord, Teamspeak etc), Music(Spotify, SoundCloud), OBS Alerts and Browser audio to VoiceMeeter AUX Input so that you will still be able to hear them if you play a WASAPI Exclusive game. 

![image](https://user-images.githubusercontent.com/16516667/215784867-20dab29b-d26c-4568-8d14-3f3475e71949.png)


Disable your audio device on the Windows Audio Panel as Voicemeeter will now be taking full control of your device and leaving it enabled can possibly cause conflicts.

![image](https://user-images.githubusercontent.com/16516667/215751486-c046c22c-8557-4e6b-8bab-0ab4a337898d.png)

## Configuring Voicemeeter with your Audio device

On the Voicemeeter window press A1 on the top right corner and select KS: [Your Audio Device], my device is the Rode AI-1.

![image](https://user-images.githubusercontent.com/16516667/215750745-76004d90-a4d5-4565-85c4-b76af61be10f.png)

>**You can use your device ASIO output if it has support for it, but if you have a microphone plugged into the audio interface/sound card you are using you will also have to set that up through Voicemeeter, which requires a bit more effort than just setting your Hardware Input to B2 and will not be covered in this guide as it is not relevant to the goal of this guide.**
**KS and ASIO are both low latency interfaces so just pick KS as it only takes exclusive control of your audio device and leaves your microphone alone.**

>**Note**: If you are using your headphones directly to the motherboard a KS option may not show up. If it doesn't show up, I suggest you buy a cheap USB Sound Card from eBay or Amazon as they have the ability to use KS Audio.


Select A1 on both Voicemeeter VAIO and AUX and select B1 for Voicemeeter VAIO

![image](https://user-images.githubusercontent.com/16516667/215753716-d527c96c-c3a6-4f08-b076-14847ae28cc9.png)


Go to System Settings/ Options on Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215751873-88724d57-c9cb-44a6-a9fd-55446992cc0b.png)

Change the highlighted values to 256, if you have a stronger CPU you can go much lower but I suggest 256 buffer size so your audio so you have a more stable audio stream to Voicemeeter and change Virtual ASIO Type to Int32LSB.

![image](https://user-images.githubusercontent.com/16516667/216692924-cbeef2b4-6114-47e7-b746-3abef25c0c00.png)


## Configuring Voicemeeter to work properly for games that require 44.1khz audio (Sound Voltex, Beatoraja etc)

Change the Sample rate and Preferred main sample rate to 44100hz in Voicemeeter System settings. If you chose to use your device ASIO option instead of KS, change the sample rate in your ASIO driver settings if applicable. 

![image](https://user-images.githubusercontent.com/16516667/218286482-22e51de8-1569-4c0b-a867-fd28d72210b5.png)

Download the [VB Audio Devices checker](https://download.vb-audio.com/Download_CABLE/VBDeviceCheck.zip), open it and press devices. Then press the "Set All devices format in 44.1khz" option

![image](https://user-images.githubusercontent.com/16516667/215767317-4f1f446f-c931-43db-85da-ae3f4a113f09.png)


# Configuring Voicemeeter with a rhythm game

If the game has ASIO, ALWAYS pick the ASIO option, if not pick the WASAPI Exclusive option

## Configuring a rhythm game with ASIO 

![image](https://user-images.githubusercontent.com/16516667/215756501-6fa935de-db86-4cfc-89d7-ce4bc24ac550.png)


## Configuring a rhythm with WASAPI Exclusive 
Make sure you are ticking the WASAPI Exclusive option, it should use your default audio device in Windows which we set earlier on in the guide, but if it doesnt, select "Voicemeeter Input".

>Don't forget to set the applications you want to be able to hear, such as Discord, OBS(for stream alerts) etc to "Voicemeeter AUX Input"

![image](https://user-images.githubusercontent.com/16516667/215757434-e7b5ee78-e015-4026-97fe-f60bc6c225ef.png)


# Configuring Voicemeeter with OBS 

In your Sources tab press the plus icon and Audio Input Capture
You may be asking why are we adding a microphone, well we set Voicemeeter VAIO to playback to B1 which is "Voicemeeter Output" and since OBS can't capture exclusive audio like WASAPI Exclusive or ASIO we are using Voicemeeter to route it to a virtual microphone so that OBS can actually capture the audio.

![image](https://user-images.githubusercontent.com/16516667/215758817-419a9e19-c7cf-4a26-9ad3-3a1f8c3bf038.png)

Call it Rhythm Game Audio, press ok and select Voicemeeter Output

![image](https://user-images.githubusercontent.com/16516667/215759187-bc807c44-6842-4775-9f00-2471e95acd0b.png)

Make sure you have this source in every scene which you use to stream rhythm games. 

## Configuring OBS to work with 44.1khz audio

If you followed the earlier step for configuring Voicemeeter to work with 44.1khz audio 

MAKE SURE you change the sample rate in OBS to 44.1khz as well or else it can make your audio sound bad.
![image](https://user-images.githubusercontent.com/16516667/216699622-99f787ba-3117-4bb4-9128-47bc6ac808bb.png)






