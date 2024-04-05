[URL](http://natas1.natas.labs.overthewire.org) <br>
username: natas1 <br>
password: g9D9cREhslqBKtcA2uocGHPfMZVzeFK6 <br>

Indicated by the hint, password should be hidden by similar way as Level 0 does. <br>


When trying to right click in the white box, a window will pop out saying that "right click has been disabled". <br>
![[Level1_popup.png]]

One easy solution is that you can right click outside the white box and you can inspect the website. <br>
![[Level1_rc.png]]

Another solution is to use Linux command "curl -u" <br>
![[curl.png]]
Password is obtained after curl result is returned <br>
![[CurlResult.png]]
Password can also be found by inspecting the page <br>
![[Level1_InsepctResult.png]] 
