[URL](http://natas7.natas.labs.overthewire.org)
username: natas7
password: jmxSiH3SP6Sonf8dv66ng8v1cIEdjXWr

There are two buttons on the front page in this level.
![[Level7.png]]

When I press these 2 button, it is found that the request URL changes. Different page have their own query parameter.
![[Level7_homepage.png]]
![[Level7_aboutpage.png]]

Could not find any other function from that 2 buttons. I inspect the web page for further clue. Found a hint mentioning the password for the next level.
![[Level7_hint.png]]

I put the provided path (`/etc/natas_webpass/natas8`) into the query parameter of page, forming a link: `http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8`

Visiting the link will then give the password for the next level.