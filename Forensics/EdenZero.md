**Challenge**: EdenZero

**Pts**: 50

**Solved**: 17

**Descriptio**

I attempted to open one of my most recent images, but encountered difficulty in doing so. Could you extend your assistance in resolving this issue.

Zip Password: Cyberlympics2023

Flag Format: acdfCTF{}

[flagishere.zip](https://github.com/parfaittolefo/Cyberlympics-CTF-Qualif-2023/blob/main/chal_files/flagishere.zip)


# Solution

First, extract the file from the zip. You will get `flagishere.jpg`. When you try to open the image, you get this error: _Could not load image “flagishere.jpg”._
Look at the file content with [ghex](https://github.com/GNOME/ghex). The Magic number show `%PDF-1.4%`, this mean that it is a PDF file. So rename 
the file like `flagishere.pdf`
When you open this PDF, you are not allow to read the flag !!! Use `pdftotext flagishere1.pdf` to get all text in the PDF. There are something..

    D9_Hd0c==0D_>bE`>bdN
    
From **ROT47** you will get _sh0w5_4ll_s0m3t1m35}_
Look for metadata from the pdf with `exiftool flagishere.pdf` to get _acdfCTF{c0mm3nt_buddy_

**FLAG:** acdfCTF{c0mm3nt_buddy_sh0w5_4ll_s0m3t1m35}
