**Challenge:** CodeX

**Pts:** 100

**Description**

I'm almost there to create the perfect recipe, but a crucial ingredient is missing. Can you discover the secret ingredient? Once you do, I'll gladly share my perfect recipe with you.

Flag Format: acdfCTF{}

File: [**recipe**](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/raw/main/chal_files/recipe)


# Solution

I used an online tool for decompilation. The tool is **dogbolt** (https://dogbolt.org/). On dogbolt, decompiling with binary ninja and Hex-Rays directly displays the inverse of the flag, but ghidra displays it in hex.

![Screenshot from 2023-09-24 18-05-22](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/108412975/52c628ec-0ce2-4d2a-a734-a7a566b428ce)

I used this tool (https://kt.gy/tools.html#conv/) to reverse the reverse of the flag what I got:

![Screenshot from 2023-09-24 18-15-10](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/108412975/d4e76463-961a-41c1-870d-92791bd8cff8)

![Screenshot from 2023-09-24 18-15-25](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/assets/108412975/438af6a3-4884-4591-baff-6bafd28405d7)

The flag is: **acdfCTF{Th3_p3rf3ct_r3c1p3_for_3t3rn1ty_l1f3}**
