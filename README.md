# 🏴‍☠️ NahamCon CTF 2024

<h2>Event Description</h2>
NahamCon is a virtual cybersecurity conference and Capture The Flag (CTF) competition organized by NahamSec. It features educational talks and workshops by industry experts, focusing on ethical hacking and information security. Participants can compete in various cybersecurity challenges, ranging from web exploitation to reverse engineering. The event fosters a global community for networking and knowledge sharing, and offers prizes and recognition for top performers. </br>

<h2>Certificate of Completion</h2>
In this event, I participated as a solo player named <strong>cruzcs</strong>, representing my team <strong>NetRunners</strong>. </br> 
<br>

<p align="center">
🎯 Placed in the top 34% of teams.

| Certification | Team Members |
|--------------------|--------------------|
| <img src="https://imgur.com/1Vq1BUF.png" title="Certification" alt="Certification" width="900" height="300"/> | <img src="https://imgur.com/uLcLZIX.png" title="Members" alt="Members" width="900" height="300"/> |
<br>

<h2>Tools and Utilities Used:</h2>

| Used               | Description                                     |
|--------------------|-------------------------------------------------|
| Ncat               | Network tool for data transfer.                 |
| [ASCII Table](https://www.ascii-code.com)    | ASCII character reference.                       |
| [StegOnline](https://georgeom.net/StegOnline/upload) | Online steganography tool.                       |
| [StegHide](https://sourceforge.net/projects/steghide)  | Command-line steganography tool.                 |
| [Exif.tools](https://exif.tools)            | EXIF metadata viewer.                            |
| [CyberChef](https://gchq.github.io/CyberChef)        | Data encoding/decoding tool.                     |
| [GitHub repo rMQR](https://github.com/OUDON/rmqrcode-python) | Python rMQR code library.                      |


## CTF Contents
During NahamCon2024, I completed the following: </br>

- <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#warmups">NahamCon CTF 2024</a> </br>
  - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#warmups">Warmups</a> </br> 
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#copypasta-challenge">Copypasta</a> </br> 
    - <a href="https://github.com/fabiancruzcs/NahamConCTF2024?tab=readme-ov-file#eicar-challenge">EICAR</a> </br> 
    - [QRRRRRRRR]
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
