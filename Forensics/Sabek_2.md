
**Challenge**: Sabek 2

**Pts**: 100

**Solves** 13

**1st 🥇 Solved**

**Description**:

Question3: What was the initial exploitation vector?

Ignore the password bruteforce, what type of vuln was executed and the full path

flag format: acdfCTF{LFI-/path/of/vuln}

[Sabek1.pcap](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/blob/main/chal_files/Sabek1.pcap)

# Solution 

From Sabek 1, we know that the target is _192.168.0.37_ and the hacker is _192.168.0.31_. So I filtred all http request like: `http && ip.src ==192.168.0.31`

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/144a04f8-1e77-4339-bc85-eb8acb354bc2)

So look at the packets, I noticed that, he/she try to list a directory content with `dir` cmd

![image](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/78282359/db283856-2364-40ec-adf6-979fb08b1808)

The path for this vuln is **/wordpress/wp-content/plugins/advanced-custom-fields-pro/acf.php?cmd=dir**

And the type of the vuln in [RCE](https://en.wikipedia.org/wiki/RCE_-_Remote_Code_Execution), so our flag is there...

**FLAG**: acdfCTF{RCE-/wordpress/wp-content/plugins/advanced-custom-fields-pro/acf.php?cmd=dir} 

