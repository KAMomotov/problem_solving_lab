# Help the general decode secret enemy messages.

General Patron is faced with a problem , his intelligence has intercepted some secret messages from the enemy but they are all encrypted. Those messages are crucial to getting the jump on the enemy and winning the war. Luckily intelligence also captured an encoding device as well. However even the smartest programmers weren't able to crack it though. So the general is asking you , his most odd but brilliant programmer.

You can call the encoder like this.

```Python
encode("Hello World!") # >>> atC5kcOuKAr!
```

Our cryptoanalysts kept poking at it and found some interesting patterns.

```Python
print(
encode("aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa")) # >>> bdhpF,82QsLirJejtNmzZKgnB3SwTyXG ?.6YIcflxVC5WE94UA1OoD70MkvRuPqHabdhpF,82QsLir
print(
encode("bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb")) # >>> dhpF,82QsLirJejtNmzZKgnB3SwTyXG ?.6YIcflxVC5WE94UA1OoD70MkvRuPqHabdhp
print(encode("!@#$%^&*()_+-")) # >>> !@#$%^&*()_+-
a,b,c = "", "", ""
for w in "abcdefghijklmnopqrstuvwxyz":
    a += encode(  "" + w)[0]
    b += encode( "_" + w)[1]
    c += encode("__" + w)[2]
print(a) # >>> bdfhjlnprtvxzBDFHJLNPRTVXZ
print(b) # >>> dhlptxBFJNRVZ37,aeimquyCGK
print(c) # >>> hpxFNV3,emuCKS08bjrzHPX5 g
```

We think if you keep on this trail you should be able to crack the code! You are expected to fill in the

```Python
decode(s)
```

function. Good luck ! General Patron is counting on you!
