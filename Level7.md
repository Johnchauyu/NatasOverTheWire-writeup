## Natas Level 7

[URL](http://natas7.natas.labs.overthewire.org) <br>
username: natas7 <br>

There are two buttons on the front page in this level. <br>
![Level7.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level7/Level7.png) <br>

When I press these 2 button, it is found that the request URL changes. Different page have their own query parameter. <br>
![Level7_homepage.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level7/Level7_homepage.png) <br>
![Level7_aboutpage.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level7/Level7_aboutpage.png) <br>

Could not find any other function from that 2 buttons. I inspect the web page for further clue. Found a hint mentioning the password for the next level. <br>
![Level7_hint.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level7/Level7_hint.png) <br>

I put the provided path (`/etc/natas_webpass/natas8`) into the query parameter of page, forming a link: `http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8` <br>

Visiting the link will then give the password for the next level. <br>
