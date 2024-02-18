Dynamo
=

<No description given 0.0>

### Files: [payatu](./payatu)

Solution
=

Since the file didn't have any extension, I loaded it up in 010 hex editor to possibly find the extension.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/6c5242fd-c8e1-4f61-bf07-70746ec7b069)

In there, I saw the first few bytes corrupted. In order to find the correct bytes, I searched up the bytes after it (0D 0A 1A 0A) and got a result.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/4c409533-d6b4-48f1-bbb4-28df3df28ac2)

This was a .png file. I switched up the `%iii` to `%PNG` and exported it as [payatu.png](./payatu.png).

![payatu.png](./payatu.png)

Upon opening the png, we can see text on the top which is our flag!

`quarkCTF{s@y_ch33s3}`
