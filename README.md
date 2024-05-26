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
| Ncat               | Network tool for data transfer.                 |
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
    - [Read The Rules]
    - [Technical Support]
    - [That's Not My Base]
    - [Twine]
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
