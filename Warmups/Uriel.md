<h3 align="center"><strong>Uriel Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/hMCCWZg.png" alt="Uriel" width="900" height="300"/>
</p>

#### Thought Process:
For this challenge, I received a large blob of text, which was said to originate from a web address bar. Initially unsure of its meaning, I researched and discovered that the percentage (%) symbol in URLs acts as an escape character, indicating the start of a percent-encoded sequence. This sequence consists of the "%" sign followed by two hexadecimal digits, representing the ASCII code of a specific character. 

URL encoding ensures compatibility and consistency across various web platforms and protocols by using the "%" sign as the escape character to standardize the representation of special characters.

Armed with this knowledge, I began decoding the blob of text using an ASCII table. I utilized a Python script with the `urllib.parse` library to decode the URL-encoded sequence.

First, I ran the script to decode the initial sequence:
```py
import urllib.parse

# The encoded string
encoded_str = "%25%36%36%25%36%63%25%36%31%25%36%37%25%37%62%25%33%38%25%36%35%25%36%36%25%36%35%25%36%32%25%33%36%25%33%36%25%36%31%25%33%37%25%33%31%25%33%39%25%36%32%25%33%37%25%33%35%25%36%31%25%33%34%25%36%32%25%33%37%25%36%33%25%33%36%25%33%33%25%33%34%25%36%34%25%33%38%25%33%38%25%33%35%25%33%37%25%33%38%25%33%38%25%36%34%25%36%36%25%36%33%25%37%64"
# Decoding the percent-encoded string
decoded_str = urllib.parse.unquote(encoded_str)

# Printing the decoded string
print(decoded_str)
```

Output:
```py
python URLdecoder-script.py
%66%6c%61%67%7b%38%65%66%65%62%36%36%61%37%31%39%62%37%35%61%34%62%37%63%36%33%34%64%38%38%35%37%38%38%64%66%63%7d
```

Following the challenge hint from the prompt, "it happened twice," I decoded the resulting sequence again:
```py
import urllib.parse

# The encoded string
encoded_str = "%66%6c%61%67%7b%38%65%66%65%62%36%36%61%37%31%39%62%37%35%61%34%62%37%63%36%33%34%64%38%38%35%37%38%38%64%66%63%7d"
# Decoding the percent-encoded string
decoded_str = urllib.parse.unquote(encoded_str)

# Printing the decoded string
print(decoded_str)
```

Output:
```py
python URLdecoder-script.py
flag{8efeb66a719b75a4b7c634d885788dfc}
```

This process revealed the flag. `flag{8efeb66a719b75a4b7c634d885788dfc}`
