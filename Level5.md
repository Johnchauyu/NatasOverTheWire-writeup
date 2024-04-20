## Natas Level 5

[URL](http://natas5.natas.labs.overthewire.org/) <br>
username: natas5 <br>

The web page said access is disallowed. No further clue is found after inspecting the HTML code of the page. <br>
![Level5.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level5/Level5.png) <br>

Since no further clue could be found in the HTML code of the page, I try to inspect the network traffic of the web page. <br>
And found that there is a cookie name "loggedin" with value 0. <br>
![Level5_loggedinCookie.png]((https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level5/Level5_loggedinCookie.png) <br>

I used BurpSuite to intercept the HTTP request. Then I changed the value of cookie: loggedin to 1 and send the HTTP request. The password to the next level is then shown. <br>
![Level5_modifyCookie.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level5/Level5_modifyCookie.png) <br>
