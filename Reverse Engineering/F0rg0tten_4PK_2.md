**Challenge**: F0rg0tten 4PK 2

**pts**: 150

**solves**: 4

**2nd 🥈 Solved ...😎**

**Description**

There is an hidden flag in the previous 4PK. What could it be 🤔.

Flag Format: acdfCTF{}

# Solution

Using `apktool d F0rg0tten.apk` or `binwalk  -ie --dd='.*' F0rg0tten.apk` to get the apk content file.

I try to find the flag with `grep -ri acdfCTF` but anything... Then, I try to search if there are some text file `.txt`

`└─$ find -type f -name *.txt`

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/e2e242bc-feda-432b-b25e-7ec16b2f397b)

`cat ./res/drawable/z.txt`   ==> I mean right right......: }7331_n3tt0gr0f_3b_0t_r3v3N{FTCfdca                                                                                

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/9bc5314e-c31b-49b4-acd2-9a7f926c8b4f)

Open python shell: `flg=}7331_n3tt0gr0f_3b_0t_r3v3N{FTCfdca; flg[::-1]`

**FLAG**: acdfCTF{N3v3r_t0_b3_f0rg0tt3n_1337}
