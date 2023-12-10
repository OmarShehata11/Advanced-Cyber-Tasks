# Password Cracking

First I used ***john the ripper*** to crack the passwords, I firstly tried to know if there's a different types of hashes using ***hashid***, so I tried to split the hashes from the shadow file to another file: ```cut -f 2 -d ":" shadow.unknown > hashes```

![1](C:\Users\Omar Shehata\Desktop\advanced task\1.png)

and use ***hashid*** on it:

![2](C:\Users\Omar Shehata\Desktop\advanced task\2.png)

So it has a variety of hashes, and john can only crack password for single hash algorithm at once, so I'm going to run it many times, let's try to run it on the file so it take the first hash it faces as the default and do crack for that hash algo:

![3](C:\Users\Omar Shehata\Desktop\advanced task\3.png)

> I used --rules to make some variance in the passwords it gets from the wordlist, like add some numbers to it, change some order ...etc.

then now change the hash algorithm to be equal to the next hash algo used by the second password ( which is sha256):

![4](C:\Users\Omar Shehata\Desktop\advanced task\4.png)

And so on until trying all the other algorithms. But I faced a problem where I can't find the password for the last 3. I tried to brute-force it even without a wordlist for 4 hours and it didn't get me any results, It's just a matter of time to get them.

And now if I tried to show all the cracked passwords:

![5](C:\Users\Omar Shehata\Desktop\advanced task\5.png)

