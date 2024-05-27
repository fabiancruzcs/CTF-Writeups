<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
</head>
<body>

<h3 align="center"><strong>EICAR Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/cE7nvy8.png" alt="EICAR" width="900" height="400"/>
</p>

<h4>Thought Process:</h4>
<p>To examine the MD5 value of the <code>eicar</code> file, I utilized the <code>certutil</code> command in the Windows terminal. Specifically, I used the following command:</p>

<pre><code>certutil -hashfile eicar MD5</code></pre>

<p>Upon execution, the terminal provided the following output:</p>

<pre><code>MD5 hash of eicar:
44d88612fea8a8f36de82e1278abb02f
CertUtil: -hashfile command completed successfully.</code></pre>

<p>I observed that the MD5 hash value for the file "eicar" was <code>44d88612fea8a8f36de82e1278abb02f</code>. Recognizing this hash as the potential flag, I utilized it for the challenge: <code>flag{44d88612fea8a8f36de82e1278abb02f}</code>.</p>

</body>
</html>
