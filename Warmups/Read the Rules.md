<h2 align="center"><strong>Read the Rules Challenge</strong></h2>
<p align="center">
  <img src="https://imgur.com/xsskpq7.png" alt="Read The Rules" width="900" height="300"/>
</p>

### Thought Process:
I started by reviewing the CTF event rules, where the flag format was specified as 'flag{[0-9a-f]{32}}', resembling an MD5 hash.

<p align="center">Rules:</p>
<p align="center">
  <img src="https://imgur.com/KoBuCzb.png" alt="Read The Rules" width="600" height="200"/>
</p>

While there, I did a quick inspection of the HTML source code pressing 'Ctrl + U'.

<p align="center">HTML source code:</p>
<p align="center">
  <img src="https://imgur.com/sjd9RIm.png" alt="QR" width="900" height="400"/>
</p>

Flag found: 
```
flag{90bc54705794a62015369fd8e86e557b}
```
