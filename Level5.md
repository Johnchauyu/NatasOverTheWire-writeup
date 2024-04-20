[URL](http://natas5.natas.labs.overthewire.org/)
username: natas5
password: Z0NsrtIkJoKALBCLi5eqFfcRN82Au2oD

The web page said access is disallowed. No further clue is found after inspecting the HTML code of the page.
![[Level5.png]]

Since no further clue could be found in the HTML code of the page, I try to inspect the network traffic of the web page.
And found that there is a cookie name "loggedin" with value 0
![[Level5_loggedinCookie.png]]

I used BurpSuite to intercept the HTTP request. Then I changed the value of cookie: loggedin to 1 and send the HTTP request. The password to the next level is then shown.
![[Level5_modifyCookie.png]]
