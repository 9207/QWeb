# 概览
HTTP是Hypertext Transfer Protocol的缩写，意为超文本传输协议，最初的目的是为了提供一种发布和接受HTML页面的方法。

IP是Internet Protocol的缩写，意为网络协议，是用于分组交换网络的一种面向数据的协议。
> "分组交换"-- Packet Switching，亦可称为封包交换，是一种相对于电路交换的通信范例，分组在节点间单独路由，不需要在传输前先建立通信路径。

TCP是Transmission Control Protocol的缩写，意为传输控制协议，是一种面向连接的、可靠的、基于字节流的传输层通信协议。
> "可靠"是指数据包能可靠地送达，"基于字节流"是指为了传输，将高层数据转为无结构的字节流分段传输。

HTTP是一个客户端终端（用户）和服务端（网站）请求和应答的标准（TCP）。

# 构成HTTP基础的部分

### TCP/IP协议族

TCP/IP是一个网络通信模型，起名于协议家族的两个标准核心协议：TCP（传输控制协议）和IP（网际协议），是一个提供点对点的链接机制。

TCP/IP参考模型是一个抽象的分层模型，这个模型中，所有的TCP/IP网络协议都被归类为4个抽象的层。每一抽象层创建在低一层提供的服务上，并且为高一层提供服务。

- 应用层(application layer)
- 传输层(transport layer)
- 网络层(internet layer)
- 连接层(link layer)

HTTP协议位于应用层，依赖位于传输层的TCP协议提供服务，TCP协议依赖位于网络层的IP协议提供服务。

### IP协议
IP协议的任务是根据主机和目的主机的地址传送数据。
一次数据包的传输，需要满足各种条件，其中最重要的两个是IP地址（节点被分配到的地址）和MAC地址（网卡所属的固定地址）
通信依赖MAC地址，在数据进行中转时，会利用下一站中转设备的MAC地址来搜索下一个中转目标，此时会才用ARP协议解析地址，根据IP查出对应的MAC地址。

### TCP协议
为了确保可靠性，TCP协议采用了三次握手策略来建立连接:
> 发送端首先发送一个数据包(packet)给接收端，数据包带有SYN(synchronize)标记。接收端收到后，回传一个带有SYN/ACK(acknowlegement)标记的数据包。最后，发送端会发送一个带有ACK标记的数据包。完成连接的建立，开始传输数据。

# 参考
- [超文本传输协议 (wikipedia)](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)
- [TCP/IP协议族 (wikipedia)](https://zh.wikipedia.org/wiki/TCP/IP%E5%8D%8F%E8%AE%AE%E6%97%8F)
- [传输控制协议 (wikipedia)](https://zh.wikipedia.org/wiki/%E4%BC%A0%E8%BE%93%E6%8E%A7%E5%88%B6%E5%8D%8F%E8%AE%AE)
- [网络协议 (wikipedia)](https://zh.wikipedia.org/wiki/%E7%BD%91%E9%99%85%E5%8D%8F%E8%AE%AE)
- [TCP 协议简介 (阮一峰)](http://www.ruanyifeng.com/blog/2017/06/tcp-protocol.html)