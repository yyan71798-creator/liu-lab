# A Novel Single-Diode Microwave Rectifier With a Series Band-Stop Structure

> **论文作者：** Changjun Liu, Feifei Tan, Hexin Zhang, Qijuan He
> **期刊：** IEEE Transactions on Microwave Theory and Techniques
> **时间：** 2017
> **DOI：** 10.1109/TMTT.2016.2626286

## 1. 论文简介

本文提出了一种采用**串联带阻结构（Series Band-Stop Structure）**的单二极管微波整流器。

核心思路是使用一段 **λg/8 短路微带线**串联在肖特基二极管前，通过微带线同时实现：

* 基波频率下的阻抗匹配
* 二次谐波的阻断与回收
* 减小整流器尺寸

相比传统整流器，该方法省去了输入端的级联带通/低通滤波器。

## 2. 主要设计

* 工作频率：**2.45 GHz**
* 二极管：**HSMS 282 Schottky**
* 串联微带线：**λg/8 短路微带线**
* 微带线特性阻抗：约 **146 Ω**
* C1：**6.8 pF**
* C2：**20 pF**
* 基板：**F4B-2**
* 基板厚度：**1 mm**
* 相对介电常数：**2.65**
* 损耗角正切：**0.0012**
* 设计/仿真软件：**Agilent ADS**

## 3. 工作原理

在基波 `f₀ = 2.45 GHz` 下：

> λg/8 短路微带线表现为感性阻抗，用于补偿二极管的容性阻抗。

在二次谐波 `2f₀` 下：

> λg/8 微带线等效为 λg/4 短路传输线，呈现开路，从而反射二次谐波，实现谐波回收。

因此，这段微带线同时承担了**阻抗匹配 + 谐波抑制**两个功能。

## 4. 实验结果

在 2.45 GHz 下，实测结果为：

| 输入功率       |        负载 |      整流效率 |
| ---------- | --------: | --------: |
| 13 dBm     |     640 Ω |     64.6% |
| 17 dBm     |     600 Ω |     73.0% |
| **20 dBm** | **580 Ω** | **80.9%** |
| 22 dBm     |     515 Ω |     60.0% |

最高微波-直流转换效率：

**80.9% @ 2.45 GHz，20 dBm，580 Ω**

实物尺寸约为：

**18 mm × 16 mm（0.23λg × 0.20λg）**。

## 5. 论文要点

**一句话总结：**

> 用一段 λg/8 短路微带线替代传统输入滤波器，同时完成二极管阻抗匹配和二次谐波回收，从而实现小型化、高效率的单二极管微波整流器。

## 6. 关键词

`Microwave Rectifier`
`Schottky Diode`
`Harmonic Recycling`
`Band-Stop Structure`
`2.45 GHz`
`Wireless Power Transmission`
`ADS`
