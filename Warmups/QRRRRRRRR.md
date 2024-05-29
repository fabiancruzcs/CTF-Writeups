<h3 align="center"><strong>QRRRRRRRR Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/QwDhz7b.png" alt="QRRRRRRRR" width="900" height="300"/>
</p>

Thought Process:

After downloading the QR code, I initially tried scanning it with my phone's regular scanner to rule out simpler possibilities. When that didn't work, I attempted to scan it using Python scripts and terminal tools with the pillow and pyzbar libraries, but these efforts also failed.

Python script used:

```py
Copy code
from PIL import Image
from pyzbar.pyzbar import decode

# Loads the image
img = Image.open("qrrrrrrrr.png")

# Decodes the QR code
result = decode(img)
for barcode in result:
    print(barcode.data.decode("utf-8"))
```

During my research, I discovered that rectangular QR codes are known as Data Matrix codes and require different handling for decoding. They are also referred to as rMQR (Rectangular Micro QR Code).

<p align="center">rMQR:</p>
<p align="center">
  <img src="https://imgur.com/pThspuD.png" alt="QR" width="600" height="100"/>
</p>

I struggled to find a way to scan it. I tried numerous scripts, imported various libraries, and searched extensively online, but couldn't find a solution. Eventually, I discovered a GitHub repository that mentioned using the QRQR app from the App Store for reading the code and suggested that the code could be resized.

GitHub repository:
```
https://github.com/OUDON/rmqrcode-python
```

After scanning the code with the QRQR app, I finally captured the flag: 

```
flag{a44557e380e3baae9c21c738664c6142}
```
