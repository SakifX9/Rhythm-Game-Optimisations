The goal?
This will allow you to play rhyhtm games at the lowest latency possible without sacrafcing other audio such as Discord calls, Stream alert audios etc.
Usually when enabling WASAPI Exclusive or ASIO in any program it will take exclusive control of your device. This will let you have multiple audio streams while still being able to enable ASIO or WASAPI Exclusive on your rhythm games so you are able to stream them.

# Setting up Voicemeeter

The following guide assumes that you are installing Voicemeeter for the first time, if you have an existing installation you can scroll further down.

Install Voicemeeter Banana from https://vb-audio.com/Voicemeeter/banana.htm

Run Voicemeeter Banana

![image](https://user-images.githubusercontent.com/16516667/208906942-f8f933b9-743f-43bf-9854-c2a1fdaa5133.png)


Open up your Windows Audio Panel

Set Voicemeeter Input to the default audio device

![image](https://user-images.githubusercontent.com/16516667/215750358-0da6bf7f-c07f-442c-9b4c-2ff7e2d95499.png)

On the Voicemeeter windwo press A1 on the top right corner and select KS: [Your Audio Device], my device is the Rode AI-1 (You can use ASIO if your device supports it but if your ASIO device has a microphone plugged in I suggest to use KS unless you are willing to setup your microphone with Voicemeeter as it will take full control of your Sound Card/Audio Interface), Realtek ASIO does not seem to work with this btw.

Note: I you are using your headphones directly to the motherboard a KS option may not show up, if it doesn't I suggest you buy a cheap USB Sound Card from eBay or Amazon as they have the ability to use KS Audio.
![image](https://user-images.githubusercontent.com/16516667/215750745-76004d90-a4d5-4565-85c4-b76af61be10f.png)

Select A1 on both Voicemeeter VAIO and AUX and select B1 for Voicemeeter VAIO

![image](https://user-images.githubusercontent.com/16516667/215753716-d527c96c-c3a6-4f08-b076-14847ae28cc9.png)

Go back to your Windows Audio Panel and disable your audio device on there as Voicemeeter will now be taking full control of your device and leaving it enabled can possibly cause conflicts.

![image](https://user-images.githubusercontent.com/16516667/215751486-c046c22c-8557-4e6b-8bab-0ab4a337898d.png)

Go to System Settings/ Options on Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215751873-88724d57-c9cb-44a6-a9fd-55446992cc0b.png)

Change the highlighted values to 256, if you have a stronger CPU you can go much lower but I suggest 256 buffer size so your audio so you have a more stable audio stream to Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215752509-349268a9-26de-4568-8dd8-d3b514749b81.png)

# Setting up Voicemeeter with a rhythm game

If the game has ASIO, ALWAYS pick the ASIO option, if not pick the WASAPI Exclusive option option

## Setting up a rhythm game with ASIO 

![image](https://user-images.githubusercontent.com/16516667/215756501-6fa935de-db86-4cfc-89d7-ce4bc24ac550.png)


## Setting up a rhythh with WASAPI Exclusive 
Make sure you are ticking the WASAPI Exclusive option, it should use your default audio device in Windows which we set earlier on in the guide, but if it doesnt, select "Voicemeeter Output".

![image](https://user-images.githubusercontent.com/16516667/215757434-e7b5ee78-e015-4026-97fe-f60bc6c225ef.png)


# Setting up Voicemeeter with OBS 

In your Sources tab press the plus icon and Audio Input Capture
You may be asking why are we adding a microphone, well we set Voicemeeter VAIO to playback to B1 which is "Voicemeeter Output" and since OBS can't capture exclusive audio like WASAPI Exclusive or ASIO we are using Voicemeeter to route it to a virtual microphone so that OBS can actually capture the audio.

![image](https://user-images.githubusercontent.com/16516667/215758817-419a9e19-c7cf-4a26-9ad3-3a1f8c3bf038.png)

Call it Rhythm Game Audio, press ok and select Voicemeeter Output

![image](https://user-images.githubusercontent.com/16516667/215759187-bc807c44-6842-4775-9f00-2471e95acd0b.png)

Make sure you have this source in every scene which you use to stream rhythm games. 







