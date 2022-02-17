# 0 



# 1 创建 NCP 工程

## 1.1 创建 Bootloader 工程

1、选择 Bootloader

![image-20220217153759888](docs/images/image-20220217153759888.png)



2、选择 UART XMODEM Bootloader

![image-20220217154523326](docs/images/image-20220217154523326.png)



3、命名工程

![image-20220217154550988](docs/images/image-20220217154550988.png)



4、选择芯片型号、编译工具

![image-20220217155222308](docs/images/image-20220217155222308.png)





5、创建的工程如下

![image-20220217161015619](docs/images/image-20220217161015619.png)



6、配置硬件

![image-20220217161155159](docs/images/image-20220217161155159.png)

![image-20220217161334595](docs/images/image-20220217161334595.png)



![image-20220217163900115](docs/images/image-20220217163900115.png)



![image-20220217163835531](docs/images/image-20220217163835531.png)

保存（Ctrl + S）

![image-20220217161405739](docs/images/image-20220217161405739.png)

![image-20220217161425019](docs/images/image-20220217161425019.png)



7、Generate 工程

![image-20220217161525534](docs/images/image-20220217161525534.png)

![image-20220217161602675](docs/images/image-20220217161602675.png)



8、编译工程

![image-20220217161627429](docs/images/image-20220217161627429.png)

成功编译如下

![image-20220217164013571](docs/images/image-20220217164013571.png)





## 1.2 创建 NCP 工程

1、选择NCP工程

![image-20220217164219723](docs/images/image-20220217164219723.png)



2、选择硬件流控

![image-20220217164307234](docs/images/image-20220217164307234.png)





3、选择文件存储位置

![image-20220217164353563](docs/images/image-20220217164353563.png)



4、选择芯片型号、编译工具

![image-20220217164439339](docs/images/image-20220217164439339.png)



5、配置硬件

![image-20220217164805858](docs/images/image-20220217164805858.png)

![image-20220217164831331](docs/images/image-20220217164831331.png)

![image-20220217164932155](docs/images/image-20220217164932155.png)



![image-20220217164958050](docs/images/image-20220217164958050.png)

保存。



6、Generate

![image-20220217165036158](docs/images/image-20220217165036158.png)

![image-20220217165058835](docs/images/image-20220217165058835.png)



7、编译工程

![image-20220217165128797](docs/images/image-20220217165128797.png)



编译成功如下：

![image-20220217165207634](docs/images/image-20220217165207634.png)



## 1.3 烧录程序至芯片









# 2 创建Host工程

## 2.1 创建

1、选择 ZigBee 工程

![image-20220217165612427](docs/images/image-20220217165612427.png)





2、选择 Host 工程

![image-20220217165641603](docs/images/image-20220217165641603.png)





3、选择网关

![image-20220217165712787](docs/images/image-20220217165712787.png)





4、选择存储位置

![image-20220217165759179](docs/images/image-20220217165759179.png)





5、Finish

![image-20220217165819131](docs/images/image-20220217165819131.png)



6、更改工程路径

![image-20220217170208907](docs/images/image-20220217170208907.png)



![image-20220217170308514](docs/images/image-20220217170308514.png)



![image-20220217170320994](docs/images/image-20220217170320994.png)

重新打开 `.isc` 文 件，工程路径如下：

![image-20220217170454723](docs/images/image-20220217170454723.png)



7、Generate

![image-20220217170512026](docs/images/image-20220217170512026.png)



## 2.2 编译

将创建的工程复制到 `Linux` 环境下使用 `make`命令进行编译

1、需要的协议栈目录如下：(app除外)

![image-20220217172439807](docs/images/image-20220217172439807.png)



2、进入网关工程所在目录，使用 `make` 命令编译工程：

![image-20220217172722176](docs/images/image-20220217172722176.png)

成功后生成可执行文件：

![image-20220217172950446](docs/images/image-20220217172950446.png)



查找串口号：`ls /dev/ttyUSB*`

启动网关： `./build/exe/Z3GatewayHost_Demo -p ttyUSB0` 



# 3 演示

