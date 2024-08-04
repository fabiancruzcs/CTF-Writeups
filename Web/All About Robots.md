<h2 align="center"><strong>All About Robots Challenge</strong></h2>
<p align="center">
  <img src="https://imgur.com/UAIVzZ5.png" alt="All About Robots" width="900" height="400"/>
</p>

### Thought Process:
I navigated to `http://challenge.nahamcon.com:30998` and found myself on a page with little information, I clicked on "Learn More" which redirected me to a different page.

<p align="center">challenge.naham.com:30998 main page:</p>
<p align="center">
  <img src="https://imgur.com/AiHBfn2.png" alt="Robots main page" width="900" height="400"/>
</p>

Upon reading the first document titled "The Web Robots Pages", I didn't find anything particularly intriguing except for the mention of `/robots.txt`. 

Following this lead, I clicked on the link which directed me to the "About /robots.txt" landing page.

<p align="center">The Web Robots Pages:</p>
<p align="center">
  <img src="https://imgur.com/q3rk8F5.png" alt="robots main page" width="900" height="400"/>
</p>

While reading through it, I came across a reference to appending `/robots.txt` to the end of a website URL. 

<p align="center">Reference:</p>
<p align="center">
  <img src="https://imgur.com/2wPvZ0i.png" alt="reference" width="900" height="400"/>
</p>

I appended "/robots.txt" to "The Web Robots Pages" URL.

Appending example:
```
https://www.robotstxt.org/robots.txt
``` 

I found a generic user-agent "*" and an empty disallow parameter.

<p align="center">The Web Robots Pages:</p>
<p align="center">
  <img src="https://imgur.com/UtVwluu.png" alt="robots web page" width="700" height="100"/>
</p>

Remembering there was another page before the one I was currently on `http://challenge.nahamcon.com:30998/`

I repeated the procedure by appending "/robots.txt" to its end.

This time, the "Disallow" parameter contained a significant clue:

<p align="center">Disallow parameter:</p>
<p align="center">
  <img src="https://imgur.com/38uaMWI.png" alt="web page" width="700" height="100"/>
</p>

Naturally, I followed this clue by appending it to the same website I was already on, `challenge.naham.com:30998`, leading me to discover the flag.

URL:
```
http://challenge.nahamcon.com:30998/open_the_pod_bay_doors_hal_and_give_me_the_flag.html
```

Flag found: 
```
flag{3f19b983c1de42bd49af1a237d7e57b9}
```
