**Challenge**: Sabek Intro

**Pts**: 50

**Solved**: 52

**Description**

Sabek College has a Critical Server that is used for The Institution Website Hosting, at the same time the Systems Administrator uses it to keep his documents. The CEO of the college has gotten a notification that someone was trying to access his email, and he knows very well that the only person who had his credentials was the Systems Admin who created him the account and sent him credentials in a text file called Passwords.rtf. The issue has become so serious that the Systems Admin could lose his position in the in the institution and further get sued for a cyber crime. Since the Systems Admin has denied liability and doesn’t want to be held accountable, the network administrator of the college is asked to submit network captures for investigations to kick off. You are the only one who can save the situation, to prove whether it’s the Systems Admin who did it or someone else got access to the file that the Systems Admin created in the server before sending to the CEO. The Systems Admin believes that you can prove that he is not the one who accessed the CEO’s mail, he believes that there could be an intruder who could have gained access to the same file because he faced some abnormalities with the Server in an hour’s time. Provided You are provided with a pcap file that was captured, named Sabek1.pcap

[Sabek1.pcap]()

# Solution

The flag is acdfCTF{number_of_packets_}

So open the Sabek1.pcap with [wireshark](https://www.wireshark.org/), under `Statistic/Capture file propeties` you will find `Captured`. The number of captured packet is there.

**FLAG:**  _acdfCTF{3322}_
