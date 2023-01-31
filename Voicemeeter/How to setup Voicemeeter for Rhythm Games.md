The goal?
This will allow you to play rhyhtm games at the lowest latency possible without sacrafcing other audio such as Discord calls, Stream alert audios etc.
Usually when enabling WASAPI Exclusive or ASIO in any program it will take exclusive control of your device. This will let you have multiple audio streams while still being able to enable ASIO or WASAPI Exclusive on your rhythm games so you are able to stream them.

The following guide assumes that you are installing Voicemeeter for the first time, if you have an existing installation you can scroll further down.

Install Voicemeeter Banana from https://vb-audio.com/Voicemeeter/banana.htm

Run Voicemeeter Banana

![image](https://user-images.githubusercontent.com/16516667/208906942-f8f933b9-743f-43bf-9854-c2a1fdaa5133.png)


Open up your Windows Audio Panel

Set Voicemeeter Input to the default audio device

![image](https://user-images.githubusercontent.com/16516667/215750358-0da6bf7f-c07f-442c-9b4c-2ff7e2d95499.png)

On the Voicemeeter windwo press A1 on the top right corner and select KS: [Your Audio Device], my device is the Rode AI-1 (You can use ASIO if your device supports it but if your ASIO device has a microphone plugged in I suggest to use KS unless you are willing to setup your microphone with Voicemeeter as it will take full control of your Sound Card/Audio Interface), Realtek ASIO does not seem to work with this btw.
![image](https://user-images.githubusercontent.com/16516667/215750745-76004d90-a4d5-4565-85c4-b76af61be10f.png)

Select A1 on both Voicemeeter VAIO and AUX and select B1 for Voicemeeter VAIO

![image](https://user-images.githubusercontent.com/16516667/215753716-d527c96c-c3a6-4f08-b076-14847ae28cc9.png)

Go back to your Windows Audio Panel and disable your audio device on there as Voicemeeter will now be taking full control of your device and leaving it enabled can possibly cause conflicts.

![image](https://user-images.githubusercontent.com/16516667/215751486-c046c22c-8557-4e6b-8bab-0ab4a337898d.png)

Go to System Settings/ Options on Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215751873-88724d57-c9cb-44a6-a9fd-55446992cc0b.png)

Change the highlighted values to 256, if you have a stronger CPU you can go much lower but I suggest 256 buffer size so your audio so you have a more stable audio stream to Voicemeeter

![image](https://user-images.githubusercontent.com/16516667/215752509-349268a9-26de-4568-8dd8-d3b514749b81.png)






