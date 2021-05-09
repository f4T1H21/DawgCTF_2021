# Cookin The Ramen
## Challenge
Type: Crypto
```
Apparently we made cookin the books too hard, here's some ramen to boil as a warmup:
.--- ...- ...- . ....- ...- ... ..--- .. .-. .-- --. -.-. .-- -.- -.-- -. -... ..--- ..-. -.-. ...- ...-- ..- --. .--- ... ..- .. --.. -.-. .... -- ...- -.- . ..- -- - . -. ...- -. ..-. --- -.-- --.. - .-.. .--- --.. --. --. ...-- ... -.-. -.- ..... .--- ..- --- -. -.- -..- -.- --.. -.- ...- ..- .-- - -.. .--- -... .... ..-. --. --.. -.- -..- .. --.. .-- ...- ... -- ...-- --.- --. ..-. ... .-- --- .--. .--- .....
```

## Solve
We can clearly see that this is morse encoded. When we try to decode it using morse, we get the following output:
```
JVVE4VS2IRWGCWKYNB2FCV3UGJSUIZCHMVKEUMTENVNFOYZTLJZGG3SCK5JUONKXKZKVUWTDJBHFGZKXIZWVSM3QGFSWOPJ5
```

Now it seems like base32/64 or something like that. There is a tool called [CyberChef](https://gchq.github.io/CyberChef/) which can decode these kind of strings recursively by their encoding algorithm.

Put our Morse decoded string in the "input" box, then press the magic stick button at the top of the output box. Let's see what happens!
[!flag](src/cookintheramen_flag.png)

We've successfully captured the flag!! ``DawgCTF{0k@y_r3al_b@by's_f1r5t}``

***Written by f4T1H***
