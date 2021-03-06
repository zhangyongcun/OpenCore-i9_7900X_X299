## 配置清单

参考文档：[OpenCore](https://dortania.github.io/OpenCore-Install-Guide/)

CPU：[i9 7900X ](https://ark.intel.com/content/www/us/en/ark/products/123613/intel-core-i9-7900x-x-series-processor-13-75m-cache-up-to-4-30-ghz.html) 10 核心 20线 **3.30 GHz**

主板：[技嘉X299](https://www.gigabyte.cn/Motherboard/X299-AORUS-Gaming-3-rev-10#kf) 

内存： 64G DDR4 

硬盘：[Intel® SSD 750 Series](https://ark.intel.com/content/www/us/en/ark/products/86742/intel-ssd-750-series-400gb-2-5in-pcie-3-0-20nm-mlc.html)

显卡：  [RX580 8G](https://www.gigabyte.com/tw/Graphics-Card/GV-RX580GAMING-8GD-rev-10-11-12#kf)

蓝牙：USB 蓝牙适配器，CSR 芯片，蓝牙版本为 4.0

键盘：秒控键盘 1代

鼠标：罗技蓝牙鼠标 M558

显示器：LG HDR 4K

![bigsur](src/bigsur.png)

## 安装步骤

### 设置 BIOS

##### BIOS：

- 【Fast Boot】  **Disabled**
- 【GSM Support】 **Disabled** （推荐关闭，我测试不关闭不影响）

##### Peripherals：

- 【USB Configuration > XHCI Hand-off】  **Enabled**  （重要！！！）

##### Chipset

- VT-d Disabled

### 制作安装盘：

打开磁盘工具，显示所有设置 （Command + 2），格式化为 MyVolume

![u](src/u.png)

下载 Big Sur 镜像并写入，详细请参考[苹果官网](https://support.apple.com/zh-cn/HT201372)

```
sudo /Applications/Install\ macOS\ Big\ Sur\ Beta.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

重启使用 U盘启动。

