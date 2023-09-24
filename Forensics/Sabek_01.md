**Challenge**: Sabek 01

**Pts**: 100

**Solves**: 29

**2nd 🥈 Solved ...😎**

**Description**

Detective, I understand that you've be given the files we got, Sabek really got hit hard, Can you get me the time my team extracted this pcap file ?

Flag Format acdfCTF{Capture Start time&Capture End time} The time is UTC +1 Eg: acdfCTF{2008-12-12 22:25:54&2008-12-12 23:15:51} Because of diffeence in time zone it may be a bit confusing so try having it to be at WAT time (UTC +1)

# Solution 

Just know a basic usage for [wireshark](https://www.wireshark.org/) to get the flag.

Under **Statistic/Capture file propeties** you will find **time** 

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/5f070827-3143-4222-ba13-a621a61736d0)

The time should be **WAT time (UTC +1)**
I am using **WAT time (UTC +2)**

**FLAG**: acdfCTF{2018-04-04 12:15:51&2018-04-04 12:27:17}


