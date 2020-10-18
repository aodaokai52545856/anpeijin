# [解决WIN10 vpn 连接错误 “无法建立计算机与VPN服务器之间的网络连接,因为远程服务器未响应。”](https://www.yenb.com/631.html)

WIN10 自带的[vpn](https://www.yenb.com/tag/vpn)配置无法使用，因为需要修改[注册表](https://www.yenb.com/tag/注册表)才可以用

[错误](https://www.yenb.com/tag/错误)1：因为没有修改过[注册表](https://www.yenb.com/tag/注册表)，所以是报这样的[错误](https://www.yenb.com/tag/错误)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-52.jpg)](https://img.yenb.com/2019/10/unnamed-file-52.jpg)

解决[错误](https://www.yenb.com/tag/错误)1：

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-17.png)](https://img.yenb.com/2019/10/unnamed-file-17.png)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-53.jpg)](https://img.yenb.com/2019/10/unnamed-file-53.jpg)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-54.jpg)](https://img.yenb.com/2019/10/unnamed-file-54.jpg)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-55.jpg)](https://img.yenb.com/2019/10/unnamed-file-55.jpg)

1.按windows图标键 + R键 >在运行中输入regedit.exe，单击“确定”，进入[注册表](https://www.yenb.com/tag/注册表)编辑器

2.在[注册表](https://www.yenb.com/tag/注册表)编辑器”页面的左侧导航树点开 HKEY_LOCAL_MACHINE>SYSTEM>CurrentControlSet>Services>PolicyAgent

3.在右边空白处新建 > DWORD值”，名称为AssumeUDPEncapsulationContextOnSendRule

4.右键单击“AssumeUDPEncapsulationContextOnSendRule”，选择“修改”，进入修改界面，修改值为2(表示可以与位于NAT设备后方的服务器建立安全关联)

5.重启电脑

[错误](https://www.yenb.com/tag/错误)2：修改完[注册表](https://www.yenb.com/tag/注册表)，[错误](https://www.yenb.com/tag/错误)就变了，是因为认证的协议问题

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-56.jpg)](https://img.yenb.com/2019/10/unnamed-file-56.jpg)

解决错误2：

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-57.jpg)](https://img.yenb.com/2019/10/unnamed-file-57.jpg)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-58.jpg)](https://img.yenb.com/2019/10/unnamed-file-58.jpg)

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-59.jpg)](https://img.yenb.com/2019/10/unnamed-file-59.jpg)

1.打开更改适配器选项

2.打开安全选项，选择使用这些协议勾上

3.再此连接。连接成功

win10错误3：win10系统更新后，导致之前的[vpn](https://www.yenb.com/tag/vpn)连接不上了

[![解决WIN10 vpn 连接错误 ](https://img.yenb.com/2019/10/unnamed-file-18.png)](https://img.yenb.com/2019/10/unnamed-file-18.png)

1，在“注册表编辑器”页面的左侧导航树中
2，选择 HKEY_LOCAL_MACHINE>SYSTEM>CurrentControlSet>Services>RasMan>Parameters，在菜单栏上选择“编辑 > 新建 > DWORD值”。
3，名称为ProhibitIpSec
4，右键单击“ProhibitIpSec”，选择“修改”，进入修改界面。
5，在“数值数据”中输入0，修改完成后单击“确定”，并退出注册表编辑器。(不行就改为1，因为我遇到这个问题改为0解决了)
6，重启电脑。