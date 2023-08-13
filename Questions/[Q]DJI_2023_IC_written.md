# **information**

**company:**  DJI

**year:**  2023

**job:**  digital IC designer

**type:**  written

**source:**  [08.01大疆创新2022数字芯片笔试](https://blog.csdn.net/weixin_44072819/article/details/123823650?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-123823650-blog-128962075.235%5Ev38%5Epc_relevant_default_base&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-123823650-blog-128962075.235%5Ev38%5Epc_relevant_default_base&utm_relevant_index=3)

锐评：这都什么题。。。

# **content**

**1、stuck-at故障模型**

扩展阅读：[故障模型和故障建模](https://www.cnblogs.com/harrypotterisdead/p/15650827.html)

**故障模型（fault model）**：

在开发、制造或者使用芯片时，描述芯片某处错误行为的抽象表示，设计者或用户可以通过此得知发生错误的信息。ps：给故障导致的行为归类。

**好处** ：减少考虑的情况；便于针对性的测试用例和故障模拟；便于评估错误覆盖率，比较ATPG生成的测试集效果

**抽象等级**：system → RTL → gate → transistor → physical （抽象等级越右越低，故障模型越具体，参与故障建模的单元越多）

常用的抽象模型主要是gate、switch（transistor）、functional（RTL）这三个

​		***functional**：*  memory fault model：可分为：stuck-at；transition；coupling；decoder；

​		***gate***  ：本层分析假设：网表中门不会出错，仅有互联线会出现障碍，分类：stuck at（线上电平永远固定在0或1，single指n条互联线中只有1条出错或者multiple指任意导线都可能存在故障）；bridging指两条或更多互联线意外相连；delay指门的引脚对特定刺激集以及特定转换的转换响应太慢，可进一步分为path delay/transition delay fault

​       ***switch:***   一般被认为是一种理想开关，常见的故障类型：stuck short ；stuck open    fault mode



**2、芯片中电迁移**

EM=电迁移，当电流密度较高时会导致金属离子向电子流方向漂移，一般发生在设备部署多年之后。



**3、Cache-主存-辅存三级存储系统中各级存储器**

cache：用于存放CPU当前访问频繁的程序和数据、速度快、容量小

《计算机组成原理》（有时间还是得看一遍）

计算机的主存指：

​		*RAM（random access memory）* ：即电脑的内存条；

​		*ROM（read only memory）：*用途比较少，电脑存放boot的地方，启动电脑时，先读rom中的内容，如bios系统，检测硬件是否正常。

计算机的辅存：

​		外部存储器，比如光盘、硬盘、U盘等等。



**4、综合工具**



**5、DFT故障模型**

看1、的扩展阅读



**6、芯片中时钟树的综合质量评价标准**

时钟网络延迟、时钟信息偏差、时钟树功耗



**7、降低芯片静态压降的方法**

减小封装电感、降低工作效率（存疑！）



**8、异步处理**

静志配置信号可以不做异步处理（这都是啥？？？）

异步处理需要考虑发送和接收时钟之间的频率关系



**9、通用逻辑门**

通用逻辑门：可以组合搭建出任何逻辑电路

NAND、NOR（NAND的速度比NOR快，所以NAND用的比较多）
