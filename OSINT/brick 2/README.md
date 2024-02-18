brick 2
=

Submit the final flag (after you log in successfully)

### Author: Gourav Suram

Solution
=

This one is a continuation of brick 1.... In the description, it said "after you log in successfully". This meant there was a login portal somewhere. I looked at his github profile and there was this [company-portal](https://github.com/tombrickctf/company-portal) repo.

I looked in its code and found `login.hackenvision.ctf.teamquark.com` in cname.txt. I opened it and it was indeed a login portal.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/829942fd-a066-4492-93bd-cc4afa6eb178)

I then looked in src/app.py to see how the portal works. Since TOPT's are not permanent, we have to generate one.

To do that, I went to a [TOPT generator](https://totp.danhersam.com/) and put in the secret key from brick 1. I got the TOPT, logged in the portal and got the flag!

`quarkCTF{05int-c4n_b3_d4nger0Us-#be_safe}`
And yes, please follow this flag.
