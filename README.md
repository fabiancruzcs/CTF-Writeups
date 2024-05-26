# 🏴‍☠️ NahamCon CTF 2024

<img src="https://img.shields.io/badge/Disclaimer-%E2%9A%A0%EF%B8%8F-red?style=for-the-badge" alt="Disclaimer">
Please be aware that this repository contains both the procedures for obtaining flags and the flags themselves. If you intend to solve the remaining CTF challenges during the extension period provided by the coordinators after the official event has ended, it's advisable to avoid reading further.

<h2>Event Description</h2>
NahamCon is a virtual cybersecurity conference and Capture The Flag (CTF) competition organized by NahamSec. It features educational talks and workshops by industry experts, focusing on ethical hacking and information security. Participants can compete in various cybersecurity challenges, ranging from web exploitation to reverse engineering. The event fosters a global community for networking and knowledge sharing, and offers prizes and recognition for top performers. </br>

<h2>Certificate of Completion</h2>
In this event, I participated as a solo player under the alias <strong>cruzcs</strong>, representing my team <strong>NetRunners</strong>. </br> 
<br>

<p align="center">
🎯 Placed in the top 34%.

| Certification | Team Members |
|--------------------|--------------------|
| <img src="https://imgur.com/1Vq1BUF.png" title="Certification" alt="Certification" width="900" height="300"/> | <img src="https://imgur.com/uLcLZIX.png" title="Members" alt="Members" width="900" height="300"/> |

<h2>Tools and Utilities Used:</h2>

| Used               | Description                                     |
|--------------------|-------------------------------------------------|
| certutil           | Windows tool for managing certificates and generating hashes. |
| ncat               | Network tool for data transfer.                 |
| [ASCII Table](https://www.ascii-code.com)    | ASCII character reference.                       |
| [StegOnline](https://georgeom.net/StegOnline/upload) | Online steganography tool.                       |
| [StegHide](https://sourceforge.net/projects/steghide)  | Command-line steganography tool.                 |
| [Exif.tools](https://exif.tools)            | EXIF metadata viewer.                            |
| [CyberChef](https://gchq.github.io/CyberChef)        | Data encoding/decoding tool.                     |
| [GitHub repo rMQR](https://github.com/OUDON/rmqrcode-python) | Python rMQR code library.                      |
| pillow              | Python Imaging Library fork for image processing.                |  
| pyzbar | Library to read barcodes and QR codes.                  |

## CTF Contents
During NahamCon2024, I completed the following challenges: </br>

- <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#%EF%B8%8F-nahamcon-ctf-2024">NahamCon CTF 2024</a> </br>
  - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#warmups">Warmups</a> </br> 
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#copypasta-challenge">Copypasta</a> </br> 
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#eicar-challenge">EICAR</a> </br> 
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#qrrrrrrrr-challenge">QRRRRRRRR</a> </br>  
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#read-the-rules-challenge">Read The Rules</a> </br>  
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#technical-support-challenge">Technical Support</a> </br>  
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#thats-not-my-base-challenge">That's Not My Base</a> </br>  
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#twine-challenge">Twine</a> </br>  
    - [Uriel] 
  - [Web]
    - [All About Robots]

## Warmups:

<h3 align="center"><strong>Copypasta Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/TKF21HE.png" alt="copypasta" width="900" height="400"/>
</p>

#### Thought Process:
I began by establishing a connection to the server through the Windows terminal using the command: </br>
```sh
ncat.exe challenge.nahamcon.com 31476
```

and got the following output: </br>
```sh
I'd just like to interject for a moment. What you're referring to as Linux, is
in fact, GNU/Linux, or as I've recently taken to calling it, GNU plus Linux.
Linux is not an operating system unto itself, but rather another free component
of a fully functioning GNU system made useful by the GNU corelibs, shell
utilities and vital system components comprising a full OS as defined by POSIX.

Many computer users run a modified version of the GNU system every day, without
realizing it. Through a peculiar turn of events, the version of GNU which is
widely used today is often called Linux, and many of its users are not aware
that it is basically the GNU system, developed by the GNU Project.
                                          
There really is a Linux, and these people are using it, but it is just a part of
the system they use. Linux is the kernel: the program in the system that
allocates the machine's resources to the other programs that you run. The kernel
is an essential part of an operating system, but useless by itself; it can only
function in the context of a complete operating system. Linux is normally used
in combination with the GNU operating system: the whole system is basically GNU
with Linux added, or GNU/Linux. All the so-called Linux distributions are really
distributions of GNU/Linux!
```

As I navigated through the text, I stumbled upon the term "GNU (GNU's Not Unix)," which was entirely new to me but proved to be quite enlightening. </br>

Feeling intrigued by the suggestive title of the CTF challenge, "copypaste," I decided to heed its implied advice. I copied all the text and pasted it into a .txt file, anticipating that the flag might be hidden within. Sure enough, my intuition proved correct, and I successfully uncovered the flag: `flag{1f68e019b29650f6e8ea15a7808f76fd}`.
</br>

<p align="center">.txt file</p>
<p align="center">
  <img src="https://imgur.com/6wxGoxw.png" alt="text file" width="600" height="300"/>
</p>

<h3 align="center"><strong>EICAR Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/cE7nvy8.png" alt="EICAR" width="900" height="400"/>
</p>

To examine the MD5 value of the `eicar` file, I utilized the `certutil` command in the Windows terminal. Specifically, I used the following command: 
```sh
certutil -hashfile eicar MD5. 
```

</br>
Upon execution, the terminal provided the following output:

```sh
MD5 hash of eicar:
44d88612fea8a8f36de82e1278abb02f
CertUtil: -hashfile command completed successfully.
```

I observed that the MD5 hash value for the file "eicar" was 44d88612fea8a8f36de82e1278abb02f. Recognizing this hash as the potential flag, I utilized it for the challenge: `flag{44d88612fea8a8f36de82e1278abb02f}`

<h3 align="center"><strong>QRRRRRRRR Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/QwDhz7b.png" alt="QRRRRRRRR" width="900" height="400"/>
</p>

After downloading the QR code, I tried scanning it with my phone's regular scanner, but it didn't work. I then attempted to scan it using Python scripts and terminal tools with the `pillow` and `pyzbar` libraries, but these efforts also failed.

Python script used:
```py
from PIL import Image
from pyzbar.pyzbar import decode

# Loads the image
img = Image.open("qrrrrrrrr.png")

# Decodes the QR code
result = decode(img)
for barcode in result:
    print(barcode.data.decode("utf-8"))
```

During my research, I discovered that rectangular QR codes are known as Data Matrix codes and require different handling for decoding. They are also referred to as `rMQR (Rectangular Micro QR Code)`.

<p align="center">rMQR</p>
<p align="center">
  <img src="https://imgur.com/pThspuD.png" alt="QR" width="600" height="100"/>
</p>

I struggled to find a way to scan it. I tried numerous scripts, imported various libraries, and searched extensively online, but couldn't find a solution. Eventually, I discovered a GitHub repository that mentioned using the QRQR app from the App Store for reading the code and suggested that the code could be resized.

After scanning the code with the QRQR app, I finally captured the flag: `flag{a44557e380e3baae9c21c738664c6142}` 

<h3 align="center"><strong>Read the Rules Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/xsskpq7.png" alt="Read The Rules" width="900" height="400"/>
</p>

I started by reviewing the CTF event rules, where the flag format was specified as 'flag{[0-9a-f]{32}}', resembling an MD5 hash.

<p align="center">Rules</p>
<p align="center">
  <img src="https://imgur.com/KoBuCzb.png" alt="Read The Rules" width="600" height="200"/>
</p>

I visited Naham's Discord server in search of clues. 

While there, a user casually mentioned that pressing 'Ctrl + U' allows for quick inspection of HTML source code. Intrigued, I followed the advice and inspected the HTML source code of the Rules page. To my surprise, the flag was embedded within the code. Flag found: `flag{90bc54705794a62015369fd8e86e557b}`

<p align="center">HTML</p>
<p align="center">
  <img src="https://imgur.com/VXXBufa.png" alt="QR" width="900" height="400"/>
</p>

<h3 align="center"><strong>Technical Support Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/9hSaRrD.png" alt="Technical Support" width="900" height="400"/>
</p>

This challenge was aimed at making participants aware of the event's ticketing system for assistance with CTF challenges or technical issues. 
Found the flag within the ctf-open-ticket channel on the discord server. `flag{a98373a74abb8c5ebb8f5192e034a91c}`

<p align="center">Ticketing System</p>
<p align="center">
  <img src="https://imgur.com/TKMYoOn.png" alt="Ticketing System" width="500" height="400"/>
</p>

<h3 align="center"><strong>That's Not My Base Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/y1Z080l.png" alt="Read The Rules" width="900" height="400"/>
</p>

At first glance, the text `F#S<YRXdP0Fd=,%J4c$Ph7XV(gF/*]%C4B<qlH+%3xGHo)` from the CTF prompt piqued my curiosity, leading me to search for an open-source tool online to decode it.

I utilized `https://gchq.github.io/CyberChef`, which offers various decoding techniques. After experimenting with multiple methods, I discovered that the text was encoded in Base92.

<p align="center">CyberChef Tool</p>
<p align="center">
  <img src="https://imgur.com/J2I4pX2.png" alt="CyberChef" width="900" height="400"/>
</p>

Reflecting on the challenge header "That's Not My Base," it indicated that the encoded text used a different "base," steering me in the right direction. 

The flag found is: `flag{784454a9509196a33dba242c423c057a}`

<h3 align="center"><strong>Twine Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/S1mB3Gs.png" alt="Twine" width="900" height="400"/>
</p>

For this challenge, I received an image and an interesting CTF prompt, hinting that the flag might be hidden within the image. My initial instinct was to examine the image's metadata, so I used the open-source tool `ExifTool` by Phil Harvey to extract it. However, I couldn't find any meaningful traces of the flag in the metadata.
Output from `command line ExifTool`:

<p align="center">ExifTool cmd output</p>
<p align="center">
  <img src="https://imgur.com/jKsCtDi.png" alt="ExifTool-Output" width="500" height="400"/>
</p>

Moving on, I explored the possibility of `steganography`, where data is concealed within images. I downloaded the open-source tool `steghide` to investigate the image for hidden messages.

Integrating `steghide` into my system for ease of use in the `command line`, I attempted to decrypt the hidden content using various passwords but without success.
The command for extracting the hidden message is:
```sh
steghide extract -sf twine.jpg
```

Seeking assistance, I reached out to the NahamCon Discord community and opened a ticket for help.

While waiting for a response, I discovered a method to run multiple `steghide commands` simultaneously using the `-p` parameter. I tested various passwords like "twine," "string," and "thread." 
Examples from the commands I used were:
```sh
steghide extract -sf twine.jpg -p twine
steghide extract -sf twine.jpg -p string
steghide extract -sf twine.jpg -p thread
```

However, I later received a hint from the Discord admins suggesting that steganography might not be necessary for this challenge. They asked me, "Is there another name for what is shown in the picture?"

This hint redirected my focus, leading me to consider the image's original filename, `phpxpoEjO`. I revisited the image's `metadata` and pondered its implications. Despite my efforts, I didn't make progress.

<p align="center">ExifTool online tool:</p>
<p align="center">
  <img src="https://imgur.com/QGr4OLj.png" alt="ExifTool-online-output" width="700" height="500"/>
</p>

Upon seeking further assistance from the Discord community, I was advised that the challenge could be solved using only resources available on my phone. Realizing that my previous approaches were leading me astray, I decided to try a different approach.

I uploaded the image to `https://georgeom.net/StegOnline/upload` and analyzed it using the strings category. Finally, I uncovered the flag within the image.

Flag found: `flag{4ac54e3ba5f8f09049f3ad62403abb25}`

<p align="center">StegOnline tool output:</p>
<p align="center">
  <img src="https://imgur.com/YiCfc8p.png" alt="ExifTool-Output" width="600" height="500"/>
</p>

