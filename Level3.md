[URL](http://natas3.natas.labs.overthewire.org) <br>
username: natas3 <br>

Same as previous level, hint stated that nothing is on this website. <br>
Inspecting the page gives another hint this time, claiming that nothing can be found on the HTML source code of the page, not even Google. <br>
![Level3_hint.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level3/Level3_hint.png) <br>

The statement "Not even Google will find it this time..." reminds me of robots.txt, a file that tells search engine crawlers which site can be accessed by the crawler, also a very common way to hide information in CTF. <br>

You may refer to [https://developers.google.com/search/docs/crawling-indexing/robots/intro](https://developers.google.com/search/docs/crawling-indexing/robots/intro) for more information. <br>

Tried to access the folder path /robots.txt and found another path <br>
![Level3_robotstxt.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level3/Level3_robotstxt.png) <br>
 
Tried to access the stated folder path and found a users.txt file <br>
![Level3_secretpath.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level3/Level3_secretpath.png) <br>

Access the users.txt and found the hidden password <br>
![Level3_userstxt.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level3/Level3_userstxt.png) <br>


