<h2 align="center"><strong>QRRRRRRRR Challenge</strong></h2>
<p align="center">
  <img src="https://imgur.com/QwDhz7b.png" alt="QRRRRRRRR" width="900" height="300"/>
</p>

<h3>Thought Process:</h3>

After downloading the QR code, I tried scanning it with my phone's regular scanner to check if it was possible. When that didn't work, I attempted to scan it using Python scripts and terminal tools with the `pillow` and `pyzbar` libraries but didn't work.

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

I searched extensively online for a possible solution and came across a GitHub repository that mentioned using the `QRQR app` from the App Store to read the code.

GitHub repository:
```
https://github.com/OUDON/rmqrcode-python
```

Scanned the code using the QRQR app and got the flag: 

```
flag{a44557e380e3baae9c21c738664c6142}
```
