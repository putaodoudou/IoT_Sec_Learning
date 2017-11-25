# loT_Sec_Learning
Simple loT_Sec learning notes.Created by ianpasm on 20171015.If there are something wrong,please tell me.Merci~ `Note`Paper from other authors.

Related website:<br>
[iChunqiu](https://www.ichunqiu.com/courses/gkaq)<br>
[ICSISIA](http://www.icsisia.com/)<br>
[安全客](http://bobao.360.cn/learning/detail/659.html)<br> 
[匡恩](http://www.kuangn.com/school/video/)<br>
[工匠安全](http://icsmaster.com/nav.html)<br>
[灯塔实验室](http://plcscan.org/blog/)<br>

## [IoT Situation Awareness](http://blog.csdn.net/liang890319/article/details/72840991):

### 1.Fields：
* 工控安全：
    * 工业4.0驱动制造业、过程控制、基础设施、其他工业控制系统(ICS)
    * 相关行业：
        * 火电厂、水电控制系统、新能源光伏发电站、电网调度、变电站、核电站、军工厂、交通枢纽、航天航空
    * 我国ICS存在的主要安全问题：
        * 缺乏完整有效的安全策略与管理流程
        * 工控平台比较脆弱
        * ICS网络比较脆弱
    * 建议：
        * 加强对工业控制系统的脆弱性(系统漏洞及配置缺陷)的合作研究，提供针对性的解决方案和安全保护措施
        * 尽可能采用安全的通信协议及规范，并提供协议异常行检测能力
        * 建立针对ICS的违规操作、越权访问等行为的有效监管
        * 建立完善的ICS安全保障体系，加强安全运维与管理
        * 加强针对ICS的新型攻击技术(如APT)的防范研究  

* 智能汽车安全：
    * 特斯拉汽车等智能汽车
* 智能家居安全

### 2.Research Points:
* 物联网安全网关
    * 问题
        * 物联网设备缺乏认证和授权标准，有些甚至没有相关设计，对于连接到公网的设备，这将导致可通过公网直接对其进行访问
        * 认证和授权的实现无法保证，可考虑额外加一层认证环节，只有认证通过才能对其进行访问．结合大数据分析提供自适应访问控制
    * 局限性
        * 安全网关更适用于对于固定场所中外部与内部连接之间的防护，如家庭，企业等，对于一些需要移动的设备的安全，如智能手环，或者内部使用无线通信的环境，则可能需要适应其他的方式来解决
    * 对于智能家居内部设备(如摄像头)的访问，可将访问视为申请，由网关记录并通知网关app，由用户在网关app端进行访问授权

* 应用层的物联网安全服务(主要是两个方面)
    * 大数据分析驱动的安全
    * 对于已有的安全能力的集成
    
    * 思路：
        * 在感知层与网络层的连接处提供一个安全网关，安全网关负责采集数据，如流量数据,设备状态等,这些数据上传到应用层，利用数据层的数据分析能力进行分析，根据分析结果，下发相应指令

* 漏洞挖掘研究(主要是两个方面)
    * 网络协议的漏洞挖掘－－＞网络层，大多采用云平台，属于云安全范畴
    * 嵌入式操作系统的漏洞挖掘－－＞感知层
        
* 物联网僵尸网络研究(主要有四个研究点)
    * 传播机理
    * 检测
    * 防护
    * 清除方法
        
* 区块链技术
    * 核心问题
        * 在信息不对称，不确定的环境下，如何建立满足经济活动赖以发生，发展的`信任`生态体系
        * 传统的中心化系统中，信任机制较为容易建立，存在一个可信第三方来管理所有的设备的身份信息．而物联网中设备过多，未来甚至可能回答到百亿级别，这会可信第三方造成巨大压力
    * 区块链系统网络是典型的P2P网络，具有分布式异构特征，而物联网天然具备分布式特征，网中的每一个设备都能管理自己在交互作用中的角色，行为和规则，对建立区块链系统的共识机制具有重要的支持作用

* 物联网设备安全设计(信息安全厂商可做的三点)
    * 提供安全的开发规范，进行安全培训，知道开发人员进行安全开发，提高产品的安全性
    * 将安全模块内置物联网产品中(如工控领域对于实时性的要求很高，而且一旦部署可能很多年都不再更换)
    * 对出场设备进行安全检测，及时发现设备中的漏洞并协助厂商进行修复

### 3.IoT Security Projects:
* TRUST
* OWASP Internet of Things Project(OWASP，Open Web Application Security Project)
* CSA(Cloud Security Alliance，CSA)
* NIST(National Institute of Standards and Technology，NIST)
* loT Security Foundation

### 4.Applications:
* 异常行为检测-->对应的物联网安全需求：攻击检测和防御、日志和审计
* 代码签名-->对应的物联网安全需求：设备保护和资产管理、攻击检测和防御
* 白盒密码-->对应的物联网安全需求：设备保护和资产管理
* over-thr air(OTA)-->对应的物联网安全需求：设备保护和资产管理
* 深度包检测(DPI)技术-->对应的物联网安全需求：攻击检测和防御
* 防火墙-->对应的物联网安全需求：攻击检测和防御
* 新技术的探索-->区块链 对应的物联网安全需求：认证

### 5.Attack Activities:
        2007年，攻击者入侵加拿大一个水利SCADA控制系统，破坏了取水调度的控制计算机
        2008年，攻击者入侵波兰某城市地铁系统，通过电视遥控器改变轨道扳道器，致四节车厢脱轨
        2010年，西门子首次监测到专门攻击该公司工业控制系统的Stuxnet病毒，也称为震网病毒
        2010年，伊朗政府宣布布什尔核电站员工电脑感染Stuxnet病毒，严重威胁核反应堆安全运营
        2011年，黑客入侵数据采集与监控系统，使美国伊利诺伊州城市供水系统的供水泵遭到破坏
        2011年，微软警告称最新发现的Duqu病毒可从工业控制系统制造商收集情报数据
        2012年，两座美国电厂遭USB病毒攻击，感染了每个工厂的工控系统，可被窃取数据
        2012年，发现攻击多个中东国家的恶意程序Flame火焰病毒，它能收集各行业的敏感信息
        2014年，黑客集团 Dragonfly 制造“超级电厂”病毒——阻断电力供应或破坏、劫持工业控制设备，全球上千座发电站遭到攻击
    
### 6.Related Terms:
        SCADA(Supervisory Control and Data Acquisition):数据采集与监视控制系统
        ICS(Industry Control System):工业控制系统
        DCS(Distributed Control System):分布式控制系统/集散控制系统
        PCS(Process Control System):过程控制系统
        ESD(Emergency Shutdown Device):应急停车系统
        PLC(Programmable Logic Controller):可编程序控制器
        RTU(Remote Terminal Unit):远程终端控制系统
        IED(Intelligent Electronic Device):智能电子设备
        HMI(Human Machine Interface):人机界面
        MIS(Management Information System):管理信息系统
        SIS(Supervisory Information System):生产过程自动化监控和管理系统
        MES(Manufacturing Execution System):制造执行管理系统




## ~~物联网信息安全~~：

    1. 物联网与信息安全
        1.1 物联网概述
            物联网(IoT--Internet of Things)定义：
                是一种通过使用射频识别、传感器、红外感应器、全球定位系统、激光扫描器等信息采集设备，按约定的协议，把任何物品与互联网连接起来，进行信息交换和通信，以实现智能识别、定位、跟踪、监控和管理的一种网络
            体系结构：
                感知控制层
                网络互联层
                资源管理层
                信息处理层
                应用层

        1.2 物联网安全问题分析
            物联网的安全问题：
                标签扫描引起的信息泄露
                射频标签受到恶意攻击
                用户可能被跟踪定位
                物联网的不安全因素可能通过互联网进行扩散
                核心技术依靠国外
                加密机制有待加强
                物联网的安全隐患会加剧工业控制网络的安全威胁
            安全需求：
                接入安全：感知节点的信任管理、身份认证、访问控制
                通信安全：网络拥塞、缺乏复杂加密算法、感知层和网络层的融合等都会使得信息安全受到攻击
                数据安全：云计算、网格计算、普适计算解决需求的同时也带来失去直接控制的危险，因此数据处理中的外包数据的安全和隐私保护技术更为重要
                系统安全：应用数据的隐私安全、服务质量和应用部署安全需求
            安全现状：
                感知层：目前主要是加密和认证，但仍需提高安全等级
                传输层：主要研究节点到节点的机密性
                应用层：目前主要的研究工作是数据库安全访问控制技术，但仍然需要信息保护技术、信息取证技术、数据加密检索技术

        1.3 物联网信息安全
            信息安全的定义：
                保持信息的保密性、完整性、可用性；另外，也包含真实性、可核查性、抗抵赖性和可靠性等
            信息安全的主要内容：
                硬件安全
                软件安全
                运行服务安全
                数据安全
            物联网信息安全技术：
                信息加密技术：数据安全协议、秘钥建立与分发机制、数据加密算法设计以及认证技术是关键
                认证与授权技术
                安全控制技术：需通过其他技术来提高传感器网络的安全性能，如节点与节点的身份认证；设计新的密钥协商方案；对传输层加密来解决窃听问题；采用跳频和扩频技术减轻网络堵塞问题
                安全审计技术
                隐私保护技术

        1.4 个人看法：
            从本质上解决问题，没有不透风的墙。网络安全问题更多的是预防，提高个人及企业的安全意识才能更好的解决问题。如今，我们所有人都参与在这其中，然而人们只关注自己在意的事情。


    2. 物联网的安全体系
        2.1 物联网的安全体系结构
            感知层
            网络层
            应用层

        2.2 物联网感知层安全
            安全挑战：
                感知层的网络节点被恶意控制-->安全性全部丢失
                感知节点所感知的信息被非法获取-->泄密
                感知层的普通节点被恶意控制-->密钥被控制者捕获
                感知层的普通节点被非法捕获
                感知层的节点受到DoS攻击
                接入物联网中的海量感知节点的标识、识别、认证和控制问题
            
            安全需求：
                机密性
                密钥协商
                节点认证
                信誉评估
                安全路由

            安全问题：
                DoS攻击
                节点被敌手捕获并控制
                接入物联网中的海量感知节点的标识、识别、认证和控制问题

            RFID的安全和隐私：
                主要隐私威胁：
                    非法跟踪
                    窃取个人信息和物品信息
                    扰乱RFID系统正常运行-->篡改、重放、屏蔽、失效、DoS攻击
                    伪造或克隆RFID标签
                
                主要安全隐患：
                    针对标签和阅读器的攻击：
                        数据窃听
                        中间人攻击
                        重放攻击
                        物理破解
                        信息篡改
                        拒绝服务攻击
                        屏蔽攻击
                        略读
                        其他攻击

                    针对后端数据库的攻击：
                        标签伪造与复制
                        RFID病毒攻击
                        EPC网络ONS(Object Name Service)攻击

                RFID系统的安全需求：
                    机密性
                    完整性
                    可用性
                    真实性
                    隐私性

                RFID的安全与隐私保护机制：
                    物理安全机制：
                        kill命令机制
                        电磁屏蔽
                        主动干扰
                        阻塞标签
                        可分离标签
                    逻辑安全机制：
                        散列锁定
                        临时ID
                        同步方法与协议
                        重加密
                        其他方法：
                            PFU
                            掩码
                                
            传感器网络安全与隐私
                无线传感器网络WSN
                安全技术：
                    基本安全框架：
                        SPINS
                        INSENS
                        TinySec
                        基于基站和节点通信的框架
                        安全协议LISP
                        LEAP
                    加密算法
                    密钥管理
                    安全路由：
                        广播认证
                        安全路由协议

            移动终端安全

        2.3 物联网网络层安全
            概述：
                安全挑战：
                    非法接入
                    DoS攻击、DDoS攻击
                    假冒攻击、中间人攻击
                    跨异构网络的网络攻击
                    信息窃取、篡改
                
                安全需求：
                    数据机密性
                    数据完整性
                    数据留机密性
                    DDoS攻击的检测和预防
                    认证与密钥(AKA)协商机制的一致性或兼容性
                        
                安全问题：
                    来自物联网接入方式的安全问题
                    来自物联网终端自身的安全问题
                    来自核心网络的安全

                TCP/IP的几种攻击类型
                    -->待补充<--

        2.4 物联网应用层安全
            概述：
                应用层的安全挑战：
                    大量终端的海量数据的识别和处理
                    智能变为低能
                    自动变为失控
                    灾难控制和恢复
                    非法人为干预
                    设备的丢失

                安全需求：
                    不同访问权限对同一数据库内容进行帅选
                    既能提供用户隐私保护又能正确认证
                    解决信息泄露追踪问题
                    进行计算机取证
                    销毁计算机数据
                    保护电子产品和软件的知识产权

            信任安全
            位置服务安全与隐私
            云安全与隐私
            信息隐藏和版权保护
            相关案例

    3. 数据安全
        3.1 数据安全的基本概念
        3.2 数据安全威胁与保障技术
        3.3 传统密码学
        3.4 现代密码学
        3.5 散列函数与消息摘要
        3.6 数字水印

    4. 隐私安全
        4.1 隐私的定义
        4.2 隐私度量
        4.3 隐私威胁
        4.4 数据库隐私
        4.5 位置隐私
        4.6 外包数据隐私

    5. 接入安全
        5.1 物联网的接入安全
        5.2 信任管理
        5.3 身份认证
        5.4 访问控制
        5.5 公钥基础设施
        5.6 案例分析

    6. 系统安全
        6.1 系统安全的概念
        6.2 恶意攻击
        6.3 入侵检测
        6.4 攻击防护
        6.5 网络安全通信协议

    7. 无线网络安全
        7.1 无线网络概述
        7.2 无线网络安全威胁
        7.3 WiFi安全技术
        7.4 3G安全技术
        7.5 ZigBee安全技术
        7.6 蓝牙安全技术
