<h3 align="center"><strong>Twine Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/S1mB3Gs.png" alt="Twine" width="900" height="300"/>
</p>

#### Thought Process:
For this challenge, I received an image and an interesting CTF prompt, hinting that the flag might be hidden within the image. My initial instinct was to examine the image's metadata, so I used the open-source tool `ExifTool` by Phil Harvey to extract it. However, I couldn't find any meaningful traces of the flag in the metadata.
Output from `command line ExifTool`:

<p align="center">ExifTool cmd output:</p>
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
