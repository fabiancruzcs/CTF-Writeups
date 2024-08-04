<h2 align="center"><strong>EICAR Challenge</strong></h2>
<p align="center">
  <img src="https://imgur.com/cE7nvy8.png" alt="EICAR" width="900" height="400"/>
</p>

<h3>Thought Process:</h3>

To examine the MD5 value of the eicar file, I used the `certutil` command in the Windows terminal:

```sh
certutil -hashfile eicar MD5
```

The terminal provided the following output:

```sh
MD5 hash of eicar:
44d88612fea8a8f36de82e1278abb02f
CertUtil: -hashfile command completed successfully.
```

The MD5 hash value for the file "eicar" was 44d88612fea8a8f36de82e1278abb02f.

Flag for the challenge: 

```
flag{44d88612fea8a8f36de82e1278abb02f}
```






