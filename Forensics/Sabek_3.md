
**Challenge**: Sabek 3

**pts**: 100

**Solves**: 100

**1st 🥇 Solved**

**Description**

Question: What file did the attacker upload to the compromised server for a shell and what port was used to get ?

FLAG FORMAT: acdfCTF{zoo.elf,4444}

[Sabek1.pcap]()

# Solution

From Sabek 1, we know that the target is 192.168.0.37 and the hacker is 192.168.0.31. So I filtred all http request like: http && ip.src ==192.168.0.31

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/5fdd2b8e-4d99-43c4-8d31-8c8cd28eee9c)

Look at the following packet, there are something... `shell.exe`

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/3063c8fe-188b-4f36-9923-4fe189adb317)

Export all http object from the pcap file. I get this exe file. Upload on [virustotal](https://www.virustotal.com/gui/file/be4211fe5c1a19ff393a2bcfa21dad8d0a687663263a63789552bda446d9421b/detection), I get:

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/3fdbb488-2915-4d1e-914d-f8918bc56ac6)

So **shell.exe** is the right file. 

Look at the filtred packet, I get something encoded in [url encode](https://en.wikipedia.org/wiki/Percent-encoding#Types_of_URI_characters). Using [cyberchef](https://gchq.github.io/CyberChef/), we can decode it.

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/c92e7567-68d5-4817-82c3-c0588670930e)


Now we know that the port is **1234**

So the flag is acdfCTF{shell.exe,1234}

**FLAG**: _acdfCTF{shell.exe,1234}_



