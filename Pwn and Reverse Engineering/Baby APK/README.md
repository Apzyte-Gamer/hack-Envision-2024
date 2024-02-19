Baby APK
=

Our club members wrote an secure Login APK, please brek their myth of "everything can be secured"

### Note: Wrap up your findings in quarkCTF{}

### Challenge Author: Aditya Bhendavadekar

### Files: [ctf.apk](./ctf.apk)

Solution
=

The file given is an apk file. Upon opening in bluestacks (emulator for android), it was a simple login page. I tried to login with random credentials and it didnt give anything.

So, to understand the file or to basically decompile it, I opened it with jadx-gui. Upon opening, we can see the source code. Seeing the files, I found `Source code/com/aditya.ctf_quark/Login` interesting since it was handling the login page.

I inspected the Login class, and found the username and password (in encrypted form). 

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/1fc0cd85-7ad2-4718-8ba8-06d73b48fad2)
![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/8c68aa0b-9073-489e-a762-259b621ca031)

I then went onto CyberChef with the string `AAE^pZXiwJof4<ZV}V~hQVXf` and tried to decrypt it.

The `encryptPass` function used to encrypt the password had `reverse.charAt(i) + 4` which made me sure to do `SUB` and `reverse` at first.

And finally by these methods, I was able to get `m4Lw4rE_4nAly5ed` and putting this as the flag works!

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/300fb92c-0125-43dc-8979-d35423ff2b0a)

`quarkCTF{m4Lw4rE_4nAly5ed}`
