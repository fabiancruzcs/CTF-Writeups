<h3 align="center"><strong>Read the Rules Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/xsskpq7.png" alt="Read The Rules" width="900" height="300"/>
</p>

#### Thought Process:
I started by reviewing the CTF event rules, where the flag format was specified as 'flag{[0-9a-f]{32}}', resembling an MD5 hash.

<p align="center">Rules:</p>
<p align="center">
  <img src="https://imgur.com/KoBuCzb.png" alt="Read The Rules" width="600" height="200"/>
</p>

I visited Naham's Discord server in search of clues. 

While there, a user casually mentioned that pressing 'Ctrl + U' allows for quick inspection of HTML source code. Intrigued, I followed the advice and inspected the HTML source code of the Rules page. To my surprise, the flag was embedded within the code. Flag found: `flag{90bc54705794a62015369fd8e86e557b}`

<p align="center">HTML:</p>
<p align="center">
  <img src="https://imgur.com/VXXBufa.png" alt="QR" width="900" height="400"/>
</p>
