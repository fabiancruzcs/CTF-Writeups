<h3 align="center"><strong>That's Not My Base Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/y1Z080l.png" alt="Read The Rules" width="900" height="300"/>
</p>

#### Thought Process:
At first glance, the text `F#S<YRXdP0Fd=,%J4c$Ph7XV(gF/*]%C4B<qlH+%3xGHo)` from the CTF prompt piqued my curiosity, leading me to search for an open-source tool online to decode it.

I utilized `https://gchq.github.io/CyberChef`, which offers various decoding techniques. After experimenting with multiple methods, I discovered that the text was encoded in Base92.

<p align="center">CyberChef Tool:</p>
<p align="center">
  <img src="https://imgur.com/J2I4pX2.png" alt="CyberChef" width="900" height="400"/>
</p>

Reflecting on the challenge header "That's Not My Base," it indicated that the encoded text used a different "base," steering me in the right direction. 

The flag found is: `flag{784454a9509196a33dba242c423c057a}`
