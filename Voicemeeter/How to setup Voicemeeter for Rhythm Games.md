The goal? Basically add ASIO to any (mostly any) Audio device. Have an ASIO device already? Well great this guide will also show you how to be able to setup multiple audio streams so you can have low latency audio and still be able to hear other audio such as Discord or Stream alerts AND it shows you how to capture your ASIO audio into OBS which was my main motivation for writing this guide in the first place.

This guide works best if you are using USB Audio like a USB Sound Card, Audio Interface, USB Headset or a DAC. If your audio device is plugged directly into your motherboard 3.5mm ports it may not be compatible, see [below](#configuring-voicemeeter-with-your-audio-device) to see if the option shows up

Tested games(working): Sound Voltex コナステ, DJMax Respect V, Beatoraja.
If you can test games with ASIO support please let me know so I can update this list

Confirmed not working: Beatmania IIDX Infinitas(in ASIO with regstry hack and WASAPI Exclusive modes)


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


# Setting up Voicemeeter

Install Voicemeeter Banana from https://vb-audio.com/Voicemeeter/banana.htm

Run Voicemeeter Banana

![image](https://user-images.githubusercontent.com/16516667/208906942-f8f933b9-743f-43bf-9854-c2a1fdaa5133.png)

## Setting up your Audio device in the Windows Audio Panel

Open up your Windows Audio Panel

Set Voicemeeter Input to the default audio device and Voicemeeter AUX Input to default communication device
Set things like music audio, discord audio, OBS alerts and your web browser to Voicemeeter AUX Input so that you are able to hear them if you play a WASAPI Exclusive game.

![image](https://user-images.githubusercontent.com/16516667/215765846-cc75ec05-3b64-425a-9db1-d848363951d6.png)
![image](https://user-images.githubusercontent.com/16516667/215778527-a48b9860-b993-4bef-afac-4cfeca574eab.png)


Disable your audio device on there as Voicemeeter will now be taking full control of your device and leaving it enabled can possibly cause conflicts.

![image](https://user-images.githubusercontent.com/16516667/215751486-c046c22c-8557-4e6b-8bab-0ab4a337898d.png)

## Configuring Voicemeeter with your Audio device

On the Voicemeeter windwo press A1 on the top right corner and select KS: [Your Audio Device], my device is the Rode AI-1.
(You can use ASIO if your device supports it but if your ASIO device has a microphone plugged in I suggest to use KS unless you are willing to setup your microphone with Voicemeeter as it will take full control of your Sound Card/Audio Interface), Realtek ASIO does not seem to work with this btw.

Note: If you are using your headphones directly to the motherboard a KS option may not show up, if it doesn't I suggest you buy a cheap USB Sound Card from eBay or Amazon as they have the ability to use KS Audio.
![image](https://user-images.githubusercontent.com/16516667/215750745-76004d90-a4d5-4565-85c4-b76af61be10f.png)

Select A1 on both Voicemeeter VAIO and AUX and select B1 for Voicemeeter VAIO

![image](https://user-images.githubusercontent.com/16516667/215753716-d527c96c-c3a6-4f08-b076-14847ae28cc9.png)


Go to System Settings/ Options on Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215751873-88724d57-c9cb-44a6-a9fd-55446992cc0b.png)

Change the highlighted values to 256, if you have a stronger CPU you can go much lower but I suggest 256 buffer size so your audio so you have a more stable audio stream to Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215752509-349268a9-26de-4568-8dd8-d3b514749b81.png)


## Configuring Voicemeeter to work properly for games that require 44.1khz audio (Sound Voltex, Beatoraja etc)

Change the Sample rate to 44100hz in Voicemeeter System settings 

![image](https://user-images.githubusercontent.com/16516667/215766822-83e2a512-53de-49ec-8bc4-3ecae684878f.png)

Download the [VB Audio Devices checker](https://download.vb-audio.com/Download_CABLE/VBDeviceCheck.zip), open it and press devices. Then press the "Set All devices format in 44.1khz" option

![image](https://user-images.githubusercontent.com/16516667/215767317-4f1f446f-c931-43db-85da-ae3f4a113f09.png)


# Configuring Voicemeeter with a rhythm game

If the game has ASIO, ALWAYS pick the ASIO option, if not pick the WASAPI Exclusive option option

## Configuring a rhythm game with ASIO 

![image](https://user-images.githubusercontent.com/16516667/215756501-6fa935de-db86-4cfc-89d7-ce4bc24ac550.png)


## Configuring a rhythm with WASAPI Exclusive 
Make sure you are ticking the WASAPI Exclusive option, it should use your default audio device in Windows which we set earlier on in the guide, but if it doesnt, select "Voicemeeter Output".

![image](https://user-images.githubusercontent.com/16516667/215757434-e7b5ee78-e015-4026-97fe-f60bc6c225ef.png)


# Configuring Voicemeeter with OBS 

In your Sources tab press the plus icon and Audio Input Capture
You may be asking why are we adding a microphone, well we set Voicemeeter VAIO to playback to B1 which is "Voicemeeter Output" and since OBS can't capture exclusive audio like WASAPI Exclusive or ASIO we are using Voicemeeter to route it to a virtual microphone so that OBS can actually capture the audio.

![image](https://user-images.githubusercontent.com/16516667/215758817-419a9e19-c7cf-4a26-9ad3-3a1f8c3bf038.png)

Call it Rhythm Game Audio, press ok and select Voicemeeter Output

![image](https://user-images.githubusercontent.com/16516667/215759187-bc807c44-6842-4775-9f00-2471e95acd0b.png)

Make sure you have this source in every scene which you use to stream rhythm games. 







