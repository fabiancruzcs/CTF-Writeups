<h3 align="center"><strong>EICAR Challenge</strong></h3>
<p align="center">
  <img src="https://imgur.com/cE7nvy8.png" alt="EICAR" width="900" height="300"/>
</p>

#### Thought Process:
To examine the MD5 value of the `eicar` file, I utilized the `certutil` command in the Windows terminal. Specifically, I used the following command: 
```sh
certutil -hashfile eicar MD5. 
```

Upon execution, the terminal provided the following output:
```sh
MD5 hash of eicar:
44d88612fea8a8f36de82e1278abb02f
CertUtil: -hashfile command completed successfully.
```

I observed that the MD5 hash value for the file "eicar" was 44d88612fea8a8f36de82e1278abb02f. Recognizing this hash as the potential flag, I utilized it for the challenge: `flag{44d88612fea8a8f36de82e1278abb02f}`
