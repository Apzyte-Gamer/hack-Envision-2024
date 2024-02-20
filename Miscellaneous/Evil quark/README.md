Evil quark
=

I don't wanna waste my server resources if things can be done at client side.

### Connection: https://evil-quark.ctf.teamquark.com/

### Note: wrap up your flag in quarkCTF{}

### Author: Harsh Patil

### Files: [misc_evilquark.zip](./misc_evilquark.zip)

Solution
=

Upon opening the website, we can see some code in the script tag of the page.

```js
(function(){var ZuL='',iem=368-357;function qmb(m){var k=5039170;var v=m.length;var g=[];for(var a=0;a<v;a++){g[a]=m.charAt(a)};for(var a=0;a<v;a++){var i=k*(a+191)+(k%36134);var b=k*(a+728)+(k%21728);var d=i%v;var x=b%v;var z=g[d];g[d]=g[x];g[x]=z;k=(i+b)%7120110;};return g.join('')};var BDA=qmb('kosrtutsccufzvdealhnjbomcopqtynrrwxig').substr(0,iem);var Olt='=a. e=e7[c=3 , =f5ovormd,";bbd[f,hdj(l]nkptrit(v0x8z(;,a) f=w6",[6(7(,n4 7v,u2o72,+5i7o,90f9o,)8!8.,x9,7h,-0o8.,r6)6e,i78;(av ==u]1fvrcvrr.g(0uggm-lynft];1+=);[7[1]s=e+n;wa  ,=+]wir=n61ca=;1uaa=01rf.rlvor+r{0hrcaog2m)n=s6lnnot);o+()+v(rruaazggm(nrs8r). pCip(, ;)hfdr<v;rpfsurlrn.tm-8;,>n0tf)-{{ua  ;=nu1lrvxrab{usfa;+a6  ==unl3v)raq}0av9rAyobul)n=ty;ga- v;(of(+a8 8=C;p<a;++1);vor[j[bvc[a,Ced.A}(s)=virolvp=j(;;frln{h=,li1a*<+u.vh]r)o]e0tgo=1;-1;4=t; +v;re su  fjj7=S)wxmcw((.le=gahritb;chafCldeAy(;+t)m+h.sh=r;o+ettgoo2o-C;r=h;o+s2=}el[efc5nuieu;;ii+(e=an6l})a=h]vi"(=>z)].[uhhtbnsrbhtiimgrqnnp)iwop+so(=[8+a],;.==+t;tia()!fnll;)oi.(q<i)o.+uah"bcs(b}t.igg,q))eu)fl=].)o;n2"r)4}=h(p;sd(q[,]);}vgrvv{h,jvi;(("l;;a. ;=(3r,q0r9[,16x4w,"2+.botcutami;la. ==kt*irgCfcoeCpa]Crd2(i6t;woe( ap r=(;g<g.aenggh.g[+cvgvrsqljtrkudecianA1(5)n.no)n(S;r9n)."rsm1h+rjo1e)z0gr)=; eau.n0vrsllhtrk9"{"..woAngk];';var ZEd=qmb[BDA];var UCk='';var Jss=ZEd;var YSd=ZEd(UCk,qmb(Olt));var cVs=YSd(qmb('!=f)c.-gal 9swkr{6m_B%r.r3n,feBnu}..!!ou1=;1Brtono!%;4tBro}B..]fB#gSj}pn)0$m1si1a8pnof7B%%SBcf.B6o3o(+.s{wjex0ug..l . rx3)\/B(B15n=B6obkB3o,affu 9], nEe!$orf.!+a61f.01+B2[i6n1$r(#el$))aB&By)o+%i71rdokeBsocd,6],a933itbr7...)a2=fk(])i]Bu.mm,)n]t7)nif0f.-6rB)wo_B$(:% ;7w_g8a_!]ns[oBex!==mq8a}c8.s}[4rI)n;7_o%tB8e.,e83%_pi]bBr.r 1B4dt4.ttst{Ba)e;=]\/)ae14.uB.f.,-!)s_Bd1)h(sp8a=]ppc!e6{d$B3.B(ff87 p],(7Br+B6{p1l.n=eBn$7%B(Bi3vv_lrm ep!yef4$B;).o1B.iye;S6se%B3_,u(_\'=B+(7fesf 8hB3BBi0{.Be6l.ii}.c %[!B$b(3.;Be2r(%t)a[v);]f[vb,_C"2#B92rn.{eB!$.CBt;$BapBb6ia(tvtvBB,1g7i6Btn$Bml.o;=3).bbr"f1e7$g;n2ruf{B4v;w1bvn;-]2o7u#f3%n1h_B aBua  B*e,nBu,B.(kl!1B9nB3d(w4r[.4nfs8s# 3aa.&t_\'(o5=otr!kI=%B$({e(Bn3%ff3).rsd_7entru._kw39su(!fB3%cs24)s$(trd 7\/c1$fBt\/d;3a06B.l=t.2p00wwefvBlB !dB));oee(qn_#(%(_0,+B(.4)6s*rCcr2+B}}B\'2lmlr));u!1,B.B1)t..fi=rBa)"c.byb(")8e)l]3B(B3flnteg(=tr!km.=BBfoo5]$;r.,;p.Bi)$}2BircffBus#mn1B(0f.%,}..p1_fre(en}+ndt6BBf=,tbe3[0!e vh{Ba(,e:B.nf,po)\/B%do9f46rm_66emnf{g3.s#t1)wtp )"&_B12%tfo3s3)BwB7Bws.72m]s*.t!o=diarrBBBoe16,(B);Be7.B:=B*Bv.(!.h#3o5tm7y;EBl!4f=ll4foe(n1B&B1!B5ff\/.+]lBn34])r,43&)3;o1,bx_;.=.an0n;])d1BtBu.bB5 (&.o.Bfgdf)ff0cBttvrl3s*(g]\'\'B.r=r=rrB;Bk,0\/)$( t,rbn9Ba6,\/foe0 };B5ata5.o2(r8fc$lie].)*[!7)m  B0.,64.]=il")B(0[$k4&bBE;uoT1}.0,i$B8)c(B:o$_Bc&7_dfno3BBB\'e.1_{Br {nao3w.(B,Bg.lb.g0Bc_orb!s[BB4.B6 miBBm\/6d5ntvw$!.B)$5ejnB'));var pwx=Jss(ZuL,cVs );pwx(7082);return 9964})()
```

We can see this is obduscated code, so we can prettify it and deobfuscate it. I then did that and got this:

```js
(function () {
  var ZuL = "", iem = 11;
  function qmb(m) {
    var k = 5039170;
    var v = m.length;
    var g = [];
    for (var a = 0; a < v; a++) {
      g[a] = m.charAt(a);
    }
    ;
    for (var a = 0; a < v; a++) {
      var i = k * (a + 191) + k % 36134;
      var b = k * (a + 728) + k % 21728;
      var d = i % v;
      var x = b % v;
      var z = g[d];
      g[d] = g[x];
      g[x] = z;
      k = (i + b) % 7120110;
    }
    ;
    return g.join("");
  }
  ;
  var BDA = qmb("kosrtutsccufzvdealhnjbomcopqtynrrwxig").substr(0, iem);
  var Olt = '=a. e=e7[c=3 , =f5ovormd,";bbd[f,hdj(l]nkptrit(v0x8z(;,a) f=w6",[6(7(,n4 7v,u2o72,+5i7o,90f9o,)8!8.,x9,7h,-0o8.,r6)6e,i78;(av ==u]1fvrcvrr.g(0uggm-lynft];1+=);[7[1]s=e+n;wa  ,=+]wir=n61ca=;1uaa=01rf.rlvor+r{0hrcaog2m)n=s6lnnot);o+()+v(rruaazggm(nrs8r). pCip(, ;)hfdr<v;rpfsurlrn.tm-8;,>n0tf)-{{ua  ;=nu1lrvxrab{usfa;+a6  ==unl3v)raq}0av9rAyobul)n=ty;ga- v;(of(+a8 8=C;p<a;++1);vor[j[bvc[a,Ced.A}(s)=virolvp=j(;;frln{h=,li1a*<+u.vh]r)o]e0tgo=1;-1;4=t; +v;re su  fjj7=S)wxmcw((.le=gahritb;chafCldeAy(;+t)m+h.sh=r;o+ettgoo2o-C;r=h;o+s2=}el[efc5nuieu;;ii+(e=an6l})a=h]vi"(=>z)].[uhhtbnsrbhtiimgrqnnp)iwop+so(=[8+a],;.==+t;tia()!fnll;)oi.(q<i)o.+uah"bcs(b}t.igg,q))eu)fl=].)o;n2"r)4}=h(p;sd(q[,]);}vgrvv{h,jvi;(("l;;a. ;=(3r,q0r9[,16x4w,"2+.botcutami;la. ==kt*irgCfcoeCpa]Crd2(i6t;woe( ap r=(;g<g.aenggh.g[+cvgvrsqljtrkudecianA1(5)n.no)n(S;r9n)."rsm1h+rjo1e)z0gr)=; eau.n0vrsllhtrk9"{"..woAngk];';
  var ZEd = qmb[BDA];
  var UCk = "";
  var Jss = ZEd;
  var YSd = ZEd(UCk, qmb(Olt));
  var cVs = YSd(qmb("!=f)c.-gal 9swkr{6m_B%r.r3n,feBnu}..!!ou1=;1Brtono!%;4tBro}B..]fB#gSj}pn)0$m1si1a8pnof7B%%SBcf.B6o3o(+.s{wjex0ug..l . rx3)/B(B15n=B6obkB3o,affu 9], nEe!$orf.!+a61f.01+B2[i6n1$r(#el$))aB&By)o+%i71rdokeBsocd,6],a933itbr7...)a2=fk(])i]Bu.mm,)n]t7)nif0f.-6rB)wo_B$(:% ;7w_g8a_!]ns[oBex!==mq8a}c8.s}[4rI)n;7_o%tB8e.,e83%_pi]bBr.r 1B4dt4.ttst{Ba)e;=]/)ae14.uB.f.,-!)s_Bd1)h(sp8a=]ppc!e6{d$B3.B(ff87 p],(7Br+B6{p1l.n=eBn$7%B(Bi3vv_lrm ep!yef4$B;).o1B.iye;S6se%B3_,u(_'=B+(7fesf 8hB3BBi0{.Be6l.ii}.c %[!B$b(3.;Be2r(%t)a[v);]f[vb,_C\"2#B92rn.{eB!$.CBt;$BapBb6ia(tvtvBB,1g7i6Btn$Bml.o;=3).bbr\"f1e7$g;n2ruf{B4v;w1bvn;-]2o7u#f3%n1h_B aBua  B*e,nBu,B.(kl!1B9nB3d(w4r[.4nfs8s# 3aa.&t_'(o5=otr!kI=%B$({e(Bn3%ff3).rsd_7entru._kw39su(!fB3%cs24)s$(trd 7/c1$fBt/d;3a06B.l=t.2p00wwefvBlB !dB));oee(qn_#(%(_0,+B(.4)6s*rCcr2+B}}B'2lmlr));u!1,B.B1)t..fi=rBa)\"c.byb(\")8e)l]3B(B3flnteg(=tr!km.=BBfoo5]$;r.,;p.Bi)$}2BircffBus#mn1B(0f.%,}..p1_fre(en}+ndt6BBf=,tbe3[0!e vh{Ba(,e:B.nf,po)/B%do9f46rm_66emnf{g3.s#t1)wtp )\"&_B12%tfo3s3)BwB7Bws.72m]s*.t!o=diarrBBBoe16,(B);Be7.B:=B*Bv.(!.h#3o5tm7y;EBl!4f=ll4foe(n1B&B1!B5ff/.+]lBn34])r,43&)3;o1,bx_;.=.an0n;])d1BtBu.bB5 (&.o.Bfgdf)ff0cBttvrl3s*(g]''B.r=r=rrB;Bk,0/)$( t,rbn9Ba6,/foe0 };B5ata5.o2(r8fc$lie].)*[!7)m  B0.,64.]=il\")B(0[$k4&bBE;uoT1}.0,i$B8)c(B:o$_Bc&7_dfno3BBB'e.1_{Br {nao3w.(B,Bg.lb.g0Bc_orb!s[BB4.B6 miBBm/6d5ntvw$!.B)$5ejnB"));
  var pwx = Jss(ZuL, cVs);
  pwx(7082);
  return 9964;
}());
```

I then put the js functions in the console, got results, deobfuscated again, got results, until I reached the point where I got the username and password which were:

`username: 3v1lqu4rk`
`password: s3cur17y/p3n37r473d/by/3v1l/qu4rk`

Now, I logged in the website and was greeted by this image:

<img width="750" alt="bBQ36nHtgEkYbmLC66T6h5Ar" src="https://github.com/Apzyte-Gamer/hack-Envision-2024/assets/71684682/7d40a47f-116e-45ad-a73d-50291083b922">

I then went to Aperi'Solve to look for interesting things, until I found `cXVhcmtDVEZ7bXU1dF9kMzV0cjB5XzN2MWxfcXU0cmt9` in the title section of the exifdata.

I went to cyberchef, decoded this from base64 and got the flag!

`quarkCTF{mu5t_d35tr0y_3v1l_qu4rk}`
