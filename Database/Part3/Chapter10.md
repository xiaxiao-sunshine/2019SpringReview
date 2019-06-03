# Chapter10: 数据存储和查询

## 10.1 物理存储介质概述

* 高速缓冲存储器(cache)
* 主存储器(main memory)
* 快闪存储器(flash memory)
* 磁盘存储器(magnetic-disk storage)
* 官学存储器(optical storage)
* 磁带存储器(tape storage)

&emsp;&emsp;存储设备层次结构:

<img style="width:600px" src="img/1.PNG">

## 10.2 磁盘和快闪存储器

### &emsp; 10.2.1 磁盘的物理特性
* 盘片(platter)
* 磁道(track)
* 扇区(sector) <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="读写信息的最小单位"/>
* 读写头(read-write head)
* 磁盘臂(disk arm)
* 柱面(cylinder)
* 磁盘控制器(disk controller) <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="坏扇区重映射(remapping of bad sector"/> <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="校验和(checksum)"/>

&emsp;&emsp;在存储区局域网体系结构中，大量的磁盘通过高速网络与许多计算机服务器项链。通常磁盘采用独立磁盘冗余阵列(Redundant Array of Independent Disk, RAID)技术进行本地化组织。
### &emsp; 10.2.2 磁盘性能的度量
* 容量
* 访问时间(access time) <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="寻道时间(seek time)"/> <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="旋转等待时间(rotational latency time"/>
* 数据传输率(data-transfer rate)
* 可靠性 <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="平均故障时间(Mean Time TO Failure, MTTF"/>

### &emsp;10.2.3 磁盘块访问的优化
* 缓冲(buffering)
* 预读(read-ahead)
* 调度(scheduling) <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="磁盘臂调度算法(disk-arm-scheduling)"/> <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="电梯算法(elevator algorithm)"/>
* 文件组织(file organization)
* 非易失性写缓冲区(nonvolatile write buffer) <input type="button" style="border-width:0;background:#FF8C00;padding:4px;border-radius:4px" value="非易失性随机访问存储器(NonVolatile Random-Access Memory, NV-RAM)"/>
* 日志磁盘(log disk)

### &emsp;10.2.4 快闪存储 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="NOR"/>  <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="NAND"/>

* 擦除块(erase block)
* 转换表(translation table)
* 损耗均衡(wear leveling)
* 闪存转换层(flash translation layer)

## 10.3 RAID <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="Redundant Array of Independent Disk"/>

### &emsp;10.3.1 通过冗余提高可靠性 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="冗余(redundancy)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="镜像(mirroring)"/>

### &emsp;10.3.2 通过并行提高性能 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="数据拆分(striping data)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="比特及拆分(bit-level striping)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="块级拆分(block-level striping)"/>

### &emsp;10.3.3 RAID 级别
&emsp;&emsp;镜像提供了高可靠性，但它十分昂贵。拆分提供了搞数据传输率，但不能提高可靠性。
* RAID 0 级: 拆分但没有冗余
* RAID 1 级: 拆分+镜像
* RAID 2 级: 内存风格的纠错码组织结构(Error-Correcting-Code, ECC), 使用奇偶校验码
* RAID 3 级: 位交叉的奇偶校验组织结构
* RAID 4 级: 块交叉的奇偶校验组织结构
* RAID 5 级: 块交叉的分布奇偶校验位的组织结构
* RAID 6 级: P+Q冗余方案，应对多张磁盘发生故障的情况

<img style="width:450px" src="img/2.PNG">

### &emsp;10.3.4 RAID 级别的选择
* RAID 0 级用于数据安全性不是很重要的高性能应用
* RAID 3比特及拆分 不如 RAID 5块级拆分
* RAID 6 级可靠性很高












