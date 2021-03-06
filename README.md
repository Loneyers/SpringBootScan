# SpringBootScan

SpringBoot 漏洞扫描

## 系统
```
linux:
  SpringScan_linux_386
  SpringScan_linux_amd64
mac:
  SpringScan_darwin_386
  SpringScan_darwin_amd64
windows:
  SpringScan_windows_386.exe
  SpringScan_windows_amd64.exe  
```
## 插件

*  cve-2016-4977
*  cve-2019-3799
*  cve-2020-5405
*  cve-2020-5410
*  spring unauth


## 使用

```
╰─$ ./SpringScan_darwin_amd64

 ______     ______   ______     __     __   __     ______        ______     ______     ______     __   __
/\  ___\   /\  == \ /\  == \   /\ \   /\ "-.\ \   /\  ___\      /\  ___\   /\  ___\   /\  __ \   /\ "-.\ \
\ \___  \  \ \  _-/ \ \  __<   \ \ \  \ \ \-.  \  \ \ \__ \     \ \___  \  \ \ \____  \ \  __ \  \ \ \-.  \
 \/\_____\  \ \_\    \ \_\ \_\  \ \_\  \ \_\\"\_\  \ \_____\     \/\_____\  \ \_____\  \ \_\ \_\  \ \_\\"\_\
  \/_____/   \/_/     \/_/ /_/   \/_/   \/_/ \/_/   \/_____/      \/_____/   \/_____/   \/_/\/_/   \/_/ \/_/

Author: Loneyer


  -d string
    	domain (default "domain.com")
  -l	list plugin
  -t string
    	cve type (default "cve-2020-2020")

```

列出所有SpringBoot 漏洞插件

```
╰─$ ./SpringScan_darwin_amd64 -l

 ______     ______   ______     __     __   __     ______        ______     ______     ______     __   __
/\  ___\   /\  == \ /\  == \   /\ \   /\ "-.\ \   /\  ___\      /\  ___\   /\  ___\   /\  __ \   /\ "-.\ \
\ \___  \  \ \  _-/ \ \  __<   \ \ \  \ \ \-.  \  \ \ \__ \     \ \___  \  \ \ \____  \ \  __ \  \ \ \-.  \
 \/\_____\  \ \_\    \ \_\ \_\  \ \_\  \ \_\\"\_\  \ \_____\     \/\_____\  \ \_____\  \ \_\ \_\  \ \_\\"\_\
  \/_____/   \/_/     \/_/ /_/   \/_/   \/_/ \/_/   \/_____/      \/_____/   \/_____/   \/_/\/_/   \/_/ \/_/

Author: Loneyer


SpringBoot plugin:
	 cve-2016-4977
	 cve-2019-3799
	 cve-2020-5405
	 cve-2020-5410
	 spring unauth

```

> 扫描 cve-2020-5410

```
╰─$ ./SpringScan_darwin_amd64 -d http://vul.test:38091 -t cve-2020-5410

 ______     ______   ______     __     __   __     ______        ______     ______     ______     __   __
/\  ___\   /\  == \ /\  == \   /\ \   /\ "-.\ \   /\  ___\      /\  ___\   /\  ___\   /\  __ \   /\ "-.\ \
\ \___  \  \ \  _-/ \ \  __<   \ \ \  \ \ \-.  \  \ \ \__ \     \ \___  \  \ \ \____  \ \  __ \  \ \ \-.  \
 \/\_____\  \ \_\    \ \_\ \_\  \ \_\  \ \_\\"\_\  \ \_____\     \/\_____\  \ \_____\  \ \_\ \_\  \ \_\\"\_\
  \/_____/   \/_/     \/_/ /_/   \/_/   \/_/ \/_/   \/_____/      \/_____/   \/_____/   \/_/\/_/   \/_/ \/_/

Author: Loneyer


[http://vul.test:38091] found springboot cve-2020-5410

```

> 扫描所有漏洞 


```
╰─$ ./SpringScan_darwin_amd64 -d http://vul.test:38091 -t all

 ______     ______   ______     __     __   __     ______        ______     ______     ______     __   __
/\  ___\   /\  == \ /\  == \   /\ \   /\ "-.\ \   /\  ___\      /\  ___\   /\  ___\   /\  __ \   /\ "-.\ \
\ \___  \  \ \  _-/ \ \  __<   \ \ \  \ \ \-.  \  \ \ \__ \     \ \___  \  \ \ \____  \ \  __ \  \ \ \-.  \
 \/\_____\  \ \_\    \ \_\ \_\  \ \_\  \ \_\\"\_\  \ \_____\     \/\_____\  \ \_____\  \ \_\ \_\  \ \_\\"\_\
  \/_____/   \/_/     \/_/ /_/   \/_/   \/_/ \/_/   \/_____/      \/_____/   \/_____/   \/_/\/_/   \/_/ \/_/

Author: Loneyer


[http://vul.test:38091] not found springboot cve-2016-4977

[http://vul.test:38091] found springboot cve-2039-3799
[http://vul.test:38091] not found springboot cve-2020-5405
[http://vul.test:38091] found springboot cve-2020-5410
[http://vul.test:38091] not found springboot unauth /env
[http://vul.test:38091] not found springboot unauth /actuator/env
```
```
