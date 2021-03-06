# HP_ENVY13_D025_6200U_HD520_AX200_OC

| **电脑型号**   | **HP ENVY13 D025 笔记本电脑**                  |
| ---------- | ----------------------------------------- |
| **处 理 器**  | **英特尔 Core i5 6200U 2.30GHz双核**           |
| **主板芯片**   | **惠普 80DF(笔记本芯片组)**                       |
| **核 显**    | **英特尔HD Graphics 520(128MB/惠普)**          |
| **板载内存**   | **8GB(SK Hynix LPDDR3 1600MHz)**          |
| **内置硬盘**   | **西部数据 WDS100T2B0B-00YS70 (1TB/固态硬盘)**    |
| **显示器**    | **三星 SDC415A(13.3英寸)**                    |
| **声卡**     | **瑞昱@英特尔HighDefinition Audio控制器「ALC290」** |
| **网卡「更换」** | **英特尔 WiFi6 AX200 160MHz**                |

## 系统支持

- 此版本为最终版本，代号:“五系通杀-OC078”

- 实测支持系统

| 系统                | 最新版本     |
|:----------------- |:-------- |
| macOS Monterey    | 12.3     |
| macOS Big Sur     | 11.6.5   |
| macOS Catalina    | 10.15.7  |
| macOS Mojave      | 10.14.6  |
| macOS High Sierra | 10.13.6  |
| Windows 10        | 21H2     |
| Windows 11        | 21H2     |
| 统信UOS             | 家庭版 21.1 |

- 所属支持是指：通过OC引导改版本系统，且正常无错误
  - Windows需保留原生引导并移动指定目录，通过OC桥接引导
  - UOS（Linux）删除原生引导，通过OC识别

## itlwm.kext使用说明

- itlwm.kext+HeliPort.dmg
  以支持在Big Sur之前系统版本的Wi-Fi驱动！！！
  - 其实，这个东西可以全版本使用，但是我默认屏蔽了Big Sur 和Monterey，因为有更好的选择，没必要开启
  - 之所以用它是因为“AirportItlwm驱动”在Catalina及以下版本需要开启安全启动才可以用，而如果开启安全启动，则无法引导Big Sur 和Monterey
- itlwm.kext与AirportItlwm.kext优势对比
  - itlwm.kext
    - 优点，速度快，链接稳定，不限制系统版本
    - 缺点，需要搭配应用使用，欺骗系统有线形式链接
  - AirportItlwm.kext
    - 优点，原生系统UI匹配使用
    - 缺点，驱动单系统匹配，不通用（即五个系统版本五个不同驱动）

## 最终已知BUG（Macos）

1. 指纹（以前不可能，以后更不可能。。。）
2. 开机音（原因不详）
3. 隔空投送（英特尔网卡导致）
4. 开机花屏（仅一瞬间）

# 留言

- 很遗憾，世事无常，在经历了 进水 摔伤 磨损 时间的摧残，最终我的笔记本还是报废了
- 所以，这是我最后一次更新此笔记本EFI文件
- 后续，需要你们自己维护了
- 再见

# 关于6200U升级Ventura 13.0相关资料建议-未实测

- 

- 1. SMBIOS选七代的
  
  2. 更新Lilu，Whatevergreen等主干驱动到开发版
  
  3. 更新opencore到开发版
  
  4. hackintool注入七代缓冲帧（需要勾选仿冒）
  
  5. 添加引导参数：-igfxsklasfbl

- OC版本升级0.8.2

- 显卡驱动升级1.6.0并修改仿冒显卡参数
  
  | AAPL,ig-platform-id： | 00001B59     |
  | -------------------- | ------------ |
  | **device-id：**       | **16590000** |

- 至于实用与真实性，请自我评测吧，我没设备了，只能提供理论知识用于更新！

- 有需求的自我修改，此仓库文件为了稳定性不予修改

# 存档更新

我的博客:https://shaoxing.vercel.app/
EFI更新页:https://shaoxing.vercel.app/c128ce6e.html

# 捐赠

- 如果，你想捐赠我，请看下图 

![12:37](https://gcore.jsdelivr.net/gh/muzishaoxing/picture@main/shaoxing/20220323/12:37.png)
