## VM虛擬機ip地址以及網絡配置(centerOS7)

使用ip addr指令查看當前ip地址

![image-20200805164328698](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805164328698.png)

###### 進入到 cd /etc/sysconfig/network-scripts目錄下編輯 vi ifcfg-ens33 

幹開始可看到的文件內容是這樣的...下面

![image-20200805164147167](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805164147167.png)



修改ONBOOT=yes,並且自己手動添加ip地址和網關子網掩碼

ONBOOT=yes

IPADDR=192.168.146.133(自己自定義的地址)

NETMASK=255.255.255.0(子網掩碼)

GATEWAY=192.168.146.2(網關-->這個是你虛擬機的網關，打開你虛擬機的-->編輯-->虛擬網絡編輯器-->選擇NAT模式-->點擊NAT設置就可以看到網關ip )

![image-20200805170934534](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805170934534.png)

修改的內容

![image-20200805170331383](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805170331383.png)

保存退出，

重啟網卡 service network restart

![image-20200805165042991](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805165042991.png)

然後使用 ip addr查看就有ip地址了

![image-20200805165327857](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805165327857.png)

關閉防火墻 systemctl stop firewalld.service

![image-20200805165229154](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805165229154.png)

然後打開Xshell輸入用戶密碼就可以連上了

![image-20200805165526766](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805165526766.png)

ping  www.baidu.com 拼一下耶可以拼通

![image-20200805171827645](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805171827645.png)
