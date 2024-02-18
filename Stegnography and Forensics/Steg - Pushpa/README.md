Steg - Pushpa
=

I need your help remembering a special phrase my friend used to say. I've forgotten it, but it meant a lot to us.Can you help me find it again?

### Author: Rohit Yeole

### Files: [steg_pushpa.zip](https://github.com/Apzyte-Gamer/hack-Envision-2024/files/14324168/steg_pushpa.zip)

Solution
=

I unzipped the file and got an audio file and an image.zip which was password protected. In hopes for finding the password of the zip in the audio file, I opened it up in Audacity and checked the spectogram.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/35846c35-2938-4b04-a8d9-20ab06b4a22c)

The spectogram sure had text as `Red Sandalwood` and upon trying it as the password for the zip file, it worked!

In the zip file was this image:

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/fb9641f8-1942-4cf7-a6d0-420001274966)

Using Aperi'Solve, I looked at the metadata of the file and found `xbhyrJAM{T41u-qOb7n4-U4o1-8HS4}` in the comment.

Using CyberChef, I bruteforced it as a ROT 13 cipher which known phrase as `quarkCTF` and got the flag!

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/0fda949b-7fd5-4fe1-8bb0-bdc99a8f98df)

`quarkCTF{M41n-jHu7g4-N4h1-8AL4}`
