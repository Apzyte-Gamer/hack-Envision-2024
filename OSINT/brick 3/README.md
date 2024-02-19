brick 3
=

After the notice that mentioned we were gonna fire him, Tom is using private repo more often.

### Note: Flag is in plaintext (with different format this time) Author: Gourav Suram

### Hint: can you list private repo using tokens? YES github allows you to do it. (cli way)

Solution
=

The question asks us to find a private repository owned by tombrickctf and find the flag in there. I immediately looked up how to see private repositories, but the plot twist comes that we need to have the account's token to see it. 

I opened tombrickctf's github page from previous challenges and tried to find something interesting. We can see that he has 14 (10 in development and 4 in main) commits and 2 braches (main and development). 

Looking at the commits of the main branch, there's nothing special, Looking at the commits of the development branch, we can see tokens!

1) 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
2) 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
3) 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
4) https://pastebin.com/YtLe2U9Z  -->  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

As in the commits, we can see that all 3 are outdated except the 4th one, the pastebin one.

Now that we have got our token, we can move onto accessing the private repo!

Looking at qustions in forums to github documentations, I got a list of few commands but none worked. Example - `curl -H "Authorization: Bearer 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" https://api.github.com/user/repos?type=all`.

After a hint got released, about using the github cli, I started reading documentation about git cli.

The documentation said that you could see the repos, by using the cmd `gh auth login`. I tried this command but failed since the token didnt have the `repo` scope. I also tried `gh repo list` but it had to be verified by `gh auth login`....

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/2ac3e740-d054-405e-bd45-2e4e6f547adb)

I then wasted 1-2 hours on trying random commands until I eventually came back to the place where I started from and read the text carefully. I went to https://cli.github.com/manual/gh_auth_login and read everything carefully and I found one interesting thing.

![image](https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/3eadbc13-fb0e-43ab-a0fb-4630c045e991)

I then went to my environment variables and added a variable `GH_TOKEN: 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`. I then reloaded cmd and ran `gh repo list` and got the flag!

`quarkCTF_tokens-are-moreIMP-then-privREPO`
