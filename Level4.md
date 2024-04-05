## Natas Level 4

[URL](http://natas4.natas.labs.overthewire.org/) <br>
username: natas4 <br>

Showed "Access disallowed" after accessing the website. <br>
![[Level4.png]] <br>

Inspected the source code of the page and no findings. <br>
Therefore, I clicked the "Refresh page" button and found that the text in the white box changes. <br>
![[Level4_refreshpage.png]] <br>
- Found that the file path shown in the browser changed
- There is a new link included in the text inside the white box

The change in file link indicate that the "Refresh page" button is not actually refreshing the page but bring me to a new page. <br>
Right after I am brought to another page, the original page (http://natas4.natas.labs.overthewire.org/) that I am browsing showed up in the text inside white box. <br>

The changes in the text make me suspect that it is detecting the [referer](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer) in my HTTP request. And I verified my suspect in the network tab of the browser. <br>
![[Level4_networktab.png]] <br>

The hidden password can be found by "curl" command with the modified referer header. <br>
![[Level4_curl.png]] <br>

It can also be done by BurpSuite. <br>
![[Level4_burp.png]]
