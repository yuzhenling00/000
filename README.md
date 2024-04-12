[新建文本文档.txt](https://github.com/yuzhenling00/000/files/14954295/default.txt)[新建文本文档.txt](https://github.com/yuzhenling00/000/files/14954292/default.txt)[节点云服务命令.txt](https://github.com/yuzhenling00/000/files/14954290/default.txt)[阿里服务器.txt](https://github.com/yuzhenling00/000/files/14954286/default.txt)[节点本地设置.txt](https://github.com/yuzhenling00/000/files/14954283/default.txt)[新建文本文档 (2).txt](https://github.com/yuzhenling00/000/files/14954279/2.txt)   # 000 [ SHIB挖矿。 ] ( https://github.com/yuzhenling00/000/files/14954112/shib.txt )

[节点详细教程.txt](https://github.com/yuzhenling00/000/files/14954274/default.txt)

[需要的硬件支持.docx](https://github.com/yuzhenling00/000/files/14954277/default.docx)

[Uploading 新建文本文档 (2).txt…]Microsoft Windows [版本 10.0.19045.2006]
(c) Microsoft Corporation。保留所有权利。

C:\Users\Administrator> ipconfig /all

Windows IP 配置

   主机名  . . . . . . . . . . . . . : WIN-QVIHCLR81EV
   主 DNS 后缀 . . . . . . . . . . . :
   节点类型  . . . . . . . . . . . . : 混合
   IP 路由已启用 . . . . . . . . . . : 否
   WINS 代理已启用 . . . . . . . . . : 否

以太网适配器 以太网:

   连接特定的 DNS 后缀 . . . . . . . :
   描述. . . . . . . . . . . . . . . : Realtek PCIe GbE Family Controller
   物理地址. . . . . . . . . . . . . : 22-35-5C-08-04-B4
   DHCP 已启用 . . . . . . . . . . . : 是
   自动配置已启用. . . . . . . . . . : 是
   本地链接 IPv6 地址. . . . . . . . : fe80::a4b1:ec4:5223:18c3%3(首选)
   IPv4 地址 . . . . . . . . . . . . : 192.168.0.101(首选)
   子网掩码  . . . . . . . . . . . . : 255.255.255.0
   获得租约的时间  . . . . . . . . . : 2023年4月15日 20:53:47
   租约过期的时间  . . . . . . . . . : 2023年4月15日 23:53:47
   默认网关. . . . . . . . . . . . . : 192.168.0.1
   DHCP 服务器 . . . . . . . . . . . : 192.168.0.1
   DHCPv6 IAID . . . . . . . . . . . : 102905180
   DHCPv6 客户端 DUID  . . . . . . . : 00-01-00-01-2B-CC-49-E2-22-35-5C-08-04-B4
   DNS 服务器  . . . . . . . . . . . : 192.168.1.1
                                       192.168.0.1
   TCPIP 上的 NetBIOS  . . . . . . . : 已启用

以太网适配器 vEthernet (Default Switch):

   连接特定的 DNS 后缀 . . . . . . . :
   描述. . . . . . . . . . . . . . . : Hyper-V Virtual Ethernet Adapter
   物理地址. . . . . . . . . . . . . : 00-15-5D-2E-D3-43
   DHCP 已启用 . . . . . . . . . . . : 否
   自动配置已启用. . . . . . . . . . : 是
   本地链接 IPv6 地址. . . . . . . . : fe80::9906:23d1:f557:de17%12(首选)
   IPv4 地址 . . . . . . . . . . . . : 172.25.192.1(首选)
   子网掩码  . . . . . . . . . . . . : 255.255.240.0
   默认网关. . . . . . . . . . . . . :
   DHCPv6 IAID . . . . . . . . . . . : 201332061
   DHCPv6 客户端 DUID  . . . . . . . : 00-01-00-01-2B-CC-49-E2-22-35-5C-08-04-B4
   DNS 服务器  . . . . . . . . . . . : fec0:0:0:ffff::1%1
                                       fec0:0:0:ffff::2%1
                                       fec0:0:0:ffff::3%1
   TCPIP 上的 NetBIOS  . . . . . . . : 已启用

C:\Users\Administrator>
()


[<<<pinode搭建步骤>>>
1.【查看系统版本】
   Win+R--输入winver 回车
（必须是 Win10 专业版 2004是最高的）
（如果版本号显示的是 1809、1903、1909 等，则需要下载易升升级到 2004以上版本，20H1或者20H2都可以）
（升级链接https://go.microsoft.com/fwlink/?LinkID=799445）检查电脑是否符合升级，符合点击下一步，不符合换系统！

2.【如何查看是否已开启bios虚拟化】
任务管理器--在CPU栏查看“虚拟化”是否开启。

3.【开启bios虚拟化】
重启
疯狂按F2、F12、DEL、ESC 等键进入BIOS
找到“高级”--“cpu菜单”--“Intel（R） Virtualization 技术”和VT-d
根据屏幕右面提示，比如按F7是向上选，F8是向下选，按一下这类按键，
就能把打开和关闭状态来回切换，根据屏幕提示保存bios，重启电脑进入windows即可

4.【开启hyper-v】
打开控制面板--程序和功能--启用或关闭Windows功能--勾选hyper-v--重启

5.【安装WSL2 】
搜索栏--《Windows PowerShell》以管理员身份打开,
第一步执行：dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
第二步：再执行：dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
浏览器输入：https://docs.microsoft.com/zh-cn/windows/wsl/wsl2-kernel 下载 WSL2安装包
运行安装后：设置默认，搜索栏--《Windows PowerShell》以管理员身份打开， 执行：wsl --set- default-version 2

6.【安装Pinode和docker】

7.【设置防火墙入站规则】
电脑—开始—设置—输入《防火墙》—打开《windows defender防火墙设置》 
《防火墙和网络保护》—《高级设置》
入站规则，新建规则，选择《端口》，《TCP》、《特定本地端口》31400-31409，《允许连接》，默认《三个选项》，名称随便填。Uploading 节点本地设置.txt…]()





[Pi Network节点介绍 教程.docx](https://github.com/yuzhenling00/000/files/14954284/Pi.Network.docx)





[Upl这个阿里服务器自带阿里云盾，要去控制台放通端口

阿里云服教程：
1，安装openvpn，命令
wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh
输入名称，可以不输入，直接回车

1 选择协议：输入1 udp；
2 是选择openvpn使用的端口，默认1194，或自定义；
3 是选择DNS,我喜欢用2 Google；
4 是选择openvpn配置文件的文件名，自定义或默认，我选择默认，直接回车；
5 按任意键安装Openvpn，

回车即可开始安装。

2：安装redir，用于端口转发
apt-get install redir

安装完成之后，添加端口映射：
redir :31400 10.8.0.2:31400&redir :31401 10.8.0.2:31401&redir :31402 10.8.0.2:31402&redir :31403 10.8.0.2:31403&redir :31404 10.8.0.2:31404&redir :31405 10.8.0.2:31405&redir :31406 10.8.0.2:31406&redir :31407 10.8.0.2:31407&redir :31408 10.8.0.2:31408&redir :31409 10.8.0.2:31409

到这，服务端就配置完成，退出服务器之后，下载openvpn配置文件，地址
服务器/root/client.ovpn 


将这个配置导入到节点电脑的openvpn就ok了
感谢三哥发上来oading 阿里服务器.txt…]()







[Uploa系统镜像CentOS7.6
重置服务器密码，确认然后重启

安装OPENVPN：
wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh

配置文件目录：
/root
一键 GOST 脚本
wget --no-check-certificate -O gost.sh https://raw.githubusercontent.com/KANIKIG/Multi-EasyGost/master/gost.sh && chmod +x gost.sh && ./gost.sh

GOST 安装完毕以后，后续可以使用 ./gost.sh 命令，进行调出使用


 进阶优化
不想被监控，卸载监控服务指令

1、使用 root 权限执行以下命令：

sh /usr/local/qcloud/YunJing/uninst.sh && \
sh /usr/local/qcloud/stargate/admin/uninstall.sh && \
sh /usr/local/qcloud/monitor/barad/admin/uninstall.sh
2、重启服务器

reboot
3、为了保险起见删除 /usr/local/qcloud 文件夹（可选）

执行：

rm -rf /usr/local/qcloud
如无任何输出，则已卸载干净。

节点绑定机器码后的选项:
2-3-1-2-1-1-2
或
1-2-1-2-2-1ding 节点云服务命令.txt…]()




[Uploading 新建文本文8.218.22.123
root(小写)
Aa123123



https://pinode.cc/


http://pi-node.cn/


8.218.22.123档.txt…]()







[Uploadi8.218.22.123
root(小写)
Aa123123



https://pinode.cc/


http://pi-node.cn/


8.218.22.123ng 新建文本文档.txt…]()







[节点介绍 2.docx](https://github.com/yuzhenling00/000/files/14954296/2.docx)






[节点介绍 1.docx](https://github.com/yuzhenling00/000/files/14954297/1.docx)









.
.
.
.
.
.
 下载picheck github名字账号  muratyurdakul75      picheck
