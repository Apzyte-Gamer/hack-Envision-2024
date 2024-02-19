Average pyJail
=

Just a simple python jail for you guys!!

### Connection: nc misc.avgjail.ctf.teamquark.com 65321

### Author: Gourav Suram

### Files: [misc-avgjail.zip](./misc-avgjail.zip)

Solution
=

Looking at the code, I only find this code interesting, since it is the only code actually running the app.

```py
inp = input("Enter payload for eval : ")
signal.alarm(0)
if len(inp) < len('print(secret)') - 1 and 'secret' not in inp:
    print(eval(inp))
else:
    print('Nice try (ig)')
```

I modify this code to this so I can test my payloads locally:

```py
inp = input("Enter payload for eval : ")
if len(inp) < len('print(secret)') - 1 and 'secret' not in inp:
    print(eval(inp))
else:
    print('Nice try (ig)')
```

I tried many payloads until `globals()` worked.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/36771ef3-93aa-4503-9f7d-d2a77d442c48)

I then went to the netcat server and gave `globals()` as the input and sure enough we see some text with our flag format and we get the flag!

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/c55ae3aa-5ca6-4239-9baf-05f905ac8200)

`quarkCTF{pyjail_fl4gs_are_FR33_p0int5_riGHT??}`
