RSA++
=

I am using large bit modulus, but I wanted to see if a single prime number also works. Can you test if my RSA is secure enough?

### Author: Gourav Suram

### Files: [chall.py](./chall.py) and [cipher.txt](./cipher.txt)

Solution
=

I inspected the chall.py and found it to be a RSA challenge with 2 ciphers. These challenges usually take these steps to be solved:

1) Calculate the difference between both the ciphers
2) Calculate the GCD of the difference and `n`
3) We then have to compute `p` and `q` using floor division
4) We then have to compute the private exponent `d`
5) We can then simply decrypt the 1st cipher to get the flag

Using these steps, I made this script

```py
from Crypto.Util.number import long_to_bytes
from math import gcd

n = 81120097948660064963760363050224942579193189658348303705417893337169638307930351045249862762611157186996852696621784130049967859671648623160495105395190069314659009235762286765210860898811784296123193952250059910523047202326030491416120053059504011321595408304983860432724425092826960453007550936094304250963
c1 = 45542186634979818062894508292378753199478347063475697933499959697412788876807522856025815165018689983246356097240196880132597170468962860463199963360111660016494444108422393986533159592722480873081672381024281364897042977740113819516183806738336958274218078682579800284758665877467676683984973821673759803463
c2 = 6259323892279367679323225674356195466045260619714530100569015926670850676458507016827519096626664770457854380432846957698467052357514606396208880352441451
e = 65537

# Step 1: Calculate the difference between the two ciphers
diff = c1 - c2

# Step 2: Calculate GCD of `n` and the difference
gcd_value = gcd(n, diff)

# Step 3: Compute `p` and `q` using floor division
p = gcd_value
q = n // p

# Step 4: Compute the private exponent `d`
phi = (p - 1) * (q - 1)
d = pow(e, -1, phi)

# Step 5: Decrypt the first cipher to obtain the flag
m = pow(c1, d, n)
flag = long_to_bytes(m)

print("Flag:", flag.decode())
```

By running this script, we get our flag!

`quarkCTF{is_r5a-secur3d??}`
