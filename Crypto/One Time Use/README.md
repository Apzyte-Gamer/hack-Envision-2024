One Time Use
=

Sometimes, long names are the only way to get in.

Connection:
nc cryto.onetime.ctf.teamquark.com 65310

### Author: kavigihan (community)

### Files: [crypto-onetimeuse.zip](./crypto-onetimeuse.zip)

Analyzing the application
=

Opening up the netcat server, we enter our name, lets say `name`. Then `name` is encrypted and given as a base64 string. Lets call this `enc_name`. Then, we get another base64 string, and lets call this `enc_flag`.

We can also notice that the `enc_flag` is always 44 characters, by testing out multiple inputs.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/9ba2aa88-97af-43ba-9e1e-d1de470c666c)

Seeing the code
=

By looking at the code (especially the encrypt() function), we can see that `enc_flag` and `enc_name` are definetly encoded by base64. By then analyzing, I realized we could use strxor to get the original value of `enc_flag`. This basically means that `name` was string xored by the `key`.

```py
def encrypt(message, key, iv):
    cipher = Cipher(algorithms.AES(key), modes.CTR(iv), backend=default_backend())
    encryptor = cipher.encryptor()
    ciphertext = encryptor.update(message.encode()) + encryptor.finalize()
    encrypted_message = ciphertext

    return b64encode(encrypted_message).decode()
```

Note - To strxor, we have to have 2 equal length of strings. So thats why I used "A"*31 which is 31 "A"'s or `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA`

Solution
=

After a long time, I was finally able to make the script and here's how it looks:

```py
import base64
from Crypto.Util import strxor

my_plain_text = b"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
my_enc_flag = base64.b64decode("97K3Po4AZJp8r6DgiYE4CJ3LnyXxQcmhdJcAu3enhg==")
enc_flag = base64.b64decode("x4aXDaQCcZ1G3YDSse0hea7VuwXDWdeQBb8PjgObzQ==")
key = strxor.strxor(my_enc_flag, my_plain_text)

print(strxor.strxor(enc_flag, key))

```

After running the script, we get the flag!

`quarkCTF{3asy-X0r_easY_p0iNt5}`
