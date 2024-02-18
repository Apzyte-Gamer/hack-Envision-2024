brick 1
=

Tom brick is an Intern for us at hack envision, he's really good at his work, but we noticed he ignore security practices.

Your challenge is to find tom's gmail id
Flag format : `quarkCTF{his-email-id}`

### Author: Gourav Suram

Solution
=

Upon seeing the description, I got a hint that since tom is an intern, he must have an official account for his work stuff. I then looked up on 2 popular website Linkedin and Github, and found [tombrickctf](https://github.com/tombrickctf) in Github.

I looked at his pfp and saw a QR code. I scanned it using google lens and got `otpauth://totp/hackEnvision:tombrickctf@gmail.com?secret=DVMQS3XJYBJE3JRJ&issuer=hackEnvision` as the result. In this, there was his email id and we got the flag!

`quarkCTF{tombrickctf@gmail.com}`
