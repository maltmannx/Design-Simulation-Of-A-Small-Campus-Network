# Design Simulation Of A Small Campus Network - Based on Cisco Packet Tracer 8
小型园区网的设计模拟
## 系统要求
园区网共有一个总部，分成三个子部，每个子部门划分成两个VLAN，使其隔离及管理方便。用一组实验设备构建一个园区网，与校园网相连，实现到Internet的访问。

在一台两层交换机SW1上划分2个VLAN（Vlan 100和Vlan200）。两个VLAN均能通过路由器访问外网，但两个VLAN之间不能通信。

在一台三层交换机SW3上划分2个VLAN（Vlan 300和Vlan 400），两个Vlan之间能够通信。两个Vlan均只能通过路由器访问校园网(10.X.X.X)，而不能访问Internet。

另外一台两层交换机SW2和一台三层交换机SW4之间使用冗余连接，在两台交换机上均划分两个Vlan（Vlan 500和Vlan 600），要求Vlan500可以访问内网所有VLAN，Vlan600既可以访问内网，又可以访问Internet。

园区网路由器内采用静态路由或OSPF路由协议，使全网联通。

采用路由器将此园区网再与外网（校园网）相连，配置NAT协议。

采用Packet Tracer或者GNS模拟网络拓扑，给各VLAN划分IP地址、掩码、网关以及各网络设备接口的IP地址。

需要在SW1中的VLAN100里安装WWW、FTP、电子邮件等基本服务。用访问控制列表使VLAN300和VLAN500中的用户在上班时间(9:00-17:00)不允许访问FTP服务器和WWW服务器，但可以访问E-Mail服务器。

IP分配规则：IP范围：192.168.24.0-192.168.31.255

路由器Serial口使用：192.168.254.48-192.168.254.63

仓库中有对应的演示文稿，其中有部分代码实现

