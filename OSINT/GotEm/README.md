GotEm
=

Can you deliver justice to Gotham, a hacker villian named V3ng3_nc3 is terrorizing the internet find him and bring him to justice along with the flag, he seems to be active on a forums and Social media.

### Author: 0xHarshsec

Solution
=

By the description, we can infer that V3ng3_nc3 is active on Reddit (since description said he is active on forums and Reddit is the biggest source).

By searching V3ng3_nc3 on Reddit, we found a [user](https://www.reddit.com/user/V3ng3_nc3).

One of the posts said `Thank god nobody saw my secret | The Gotham city relies on me`. This made me suspicious. So, I went to https://web.archive.org/. I pasted his user URL and scanned it.

The website actually had 4 archives, 2 on 17th and 2 on 18th Feb. I opened these archives and got these links:

17th Feb ones:

https://web.archive.org/web/20240217185554/https://www.reddit.com/user/V3ng3_nc3/

https://web.archive.org/web/20240217192652/https://www.reddit.com/user/V3ng3_nc3/

18th Feb ones:

https://web.archive.org/web/20240218101932/https://www.reddit.com/user/V3ng3_nc3/

https://web.archive.org/web/20240218101933/https://www.reddit.com/user/V3ng3_nc3/

I opened all of these, and found [this one interesting](https://web.archive.org/web/20240217192652/https://www.reddit.com/user/V3ng3_nc3/).

This had a post that was deleted, and therefore upon clicking on the image, we got a cipher. txdunFWI{!_dp_Y3QJ3@QF3}.

Going to CyberChef and bruteforcing it as a ROT 13 cipher with known key as `quarkCTF`, we got the flag!

`quarkCTF{!_am_V3NG3@NC3}`
