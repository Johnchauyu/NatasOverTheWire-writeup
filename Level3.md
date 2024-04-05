[URL](http://natas3.natas.labs.overthewire.org)
username: natas3
password: G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q

Same as previous level, hint stated that nothing is on this website.
Inspecting the page gives another hint this time, claiming that nothing can be found on the HTML source code of the page, not even Google.
![[Level3_hint.png]]

The statement "Not even Google will find it this time..." reminds me of robots.txt, a file that tells search engine crawlers which site can be accessed by the crawler, also a very common way to hide information in CTF.

You may refer to https://developers.google.com/search/docs/crawling-indexing/robots/intro for more information.

Tried to access the folder path /robots.txt and found another path
![[Level3_robotstxt.png]]

Tried to access the stated folder path and found a users.txt file
![[Level3_secretpath.png]]

Access the users.txt and found the hidden password
![[Level3_userstxt.png]]


