
**Challenge**: Sabek 1

**Pts**: 75

**Solves**: 26

**2nd 🥈 Solved ...😎**

**Description**

Using Sabek1.pcap

Question2: What was the attacker's IP address and host Operating System?

Flag format: acdfCTF{IP&Android_Operating_System}

[Sabek1.pcap](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/blob/main/chal_files/Sabek1.pcap)

# Solution 

To quickly solve this challenge, you need to know the basics of the [attack execution process](https://www.information-age.com/7-steps-hackers-take-execute-successful-cyber-attack-745/).
The first steps are **Reconnaissance** and **Scanning**. To know more about, ask your friend [google](google.com) or [ChatGPT](https://chat.openai.com/)
This mean we shoul look at from wich IP coming many request to wich one ...
The first is the attacker and the second is the target.

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/5eef48e6-8e1a-40b9-9b90-2ea095c1edac)

Look at a packet I noticed that `192.168.0.37` is a web server. So our hacker may be `192.168.0.21`

Looking for some conversation from the web server I found this.

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/15b18c54-d5af-49a7-bc4c-3aaf0afdab79)

This mean that its OS is **Windows Operation System** 

Let's try our flag... acdfCTF{192.168.0.21&Windows_Operating_System} 

wath ??? Wrong 🙁

Try the second IP: acdfCTF{192.168.0.31&Windows_Operating_System} 

Correct ✅

**FLAG**: acdfCTF{192.168.0.31&Windows_Operating_System}
