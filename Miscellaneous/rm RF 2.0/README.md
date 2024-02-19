rm RF 2.0
=

more like a shell

### Netcat: nc rmrf.ctf.teamquark.com 65322

### For better experience: rlwrap nc rmrf.ctf.teamquark.com 65322

### Author: Gourav Suram

Solution
=

I looked at the source code at first and focused on the allowed commands. I read documentations about them. The most interesting I found was `ps`. When you run `ps aux`, it prints out all the processes. And each process is created in `/proc/<PID>/`. The code is creating a file, so we can use `fd` which has links to what files are used in code.

`allow = ['cat', 'ls', 'whoami', 'cd', 'ps', 'uname', 'date', 'wc']`

So to list all files, I used `ls -la /proc/32/fd/` and got this:

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/458bca2e-f7b2-438e-9dda-2fe16749f1a2)

I then logged the 5th file and got the flag!

`quarkCTF{D3lEt3D_fiL35_4r3_in-FD}`
