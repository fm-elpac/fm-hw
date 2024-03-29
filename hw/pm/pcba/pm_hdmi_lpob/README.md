# HDMI 低速引出板

型号及版本: `pm_hdmi_lpob v0.1`


## 说明

HDMI 接口 (A 型) 一共有 19 个引脚 (算上外壳是 20 个),
其中 1 ~ 12 为高速差分信号 (共 12 个, 含信号屏蔽),
本电路板引出其余的低速信号 (共 8 个).

本电路板共有 3 个连接器:
HDMI 插头 (A 型), HDMI 插座 (A 型), 2.54mm 排针 (8 针).
其中 1 ~ 12 高速信号直接通过, 其余 8 个通过排针旁路引出.

本电路板可用于 DDC/CI (i2c), CEC, 调试 (小米电视) 等功能.


## 电路板信息

| 参数 | 值 | 备注 |
| :--- | :- | :--- |
| 层数 | 2 | |
| 长宽 | 48mm x 19mm | |
| 板厚 | 1.6mm | |
| 材质 | FR-4 | |
| 铜厚 | 35um (1oz) | |

### 材料清单 (BOM)

| 序号 | 名称 | 数量 | 参考价格 (CNY) | 备注 |
| :--: | :--- | ---: | -------------: | :--- |
| 1 | HDMI-A 插头夹板 (1.6mm) | 1 | 0.38 | |
| 2 | HDMI-A 插座夹板 (1.6mm) | 1 | 0.42 | |
| 3 | 2.54mm 排针 (1x8) | 1 | 0.08 | |
| 总计 | | 3 | 0.88 | |

+ PCB 成本 (每片): 约 2.5

+ PCBA 成本 (每片): 约 3.4


## HDMI 引脚定义

参考资料:
+ <https://pinoutguide.com/Video/hdmi_pinout.shtml>

HDMI 插头 (A 型):

| 序号 | 名称 | 说明 | 信号类型 | 位置* |
| :--: | :--- | :--- | :------: | :---: |
| 1 | TMDS 数据 2 + | 差分信号 (数据) | 高速 | 1 |
| 2 | TMDS 数据 2 屏蔽 | | 信号屏蔽 | 2 |
| 3 | TMDS 数据 2 - | 差分信号 (数据) | 高速 | 1 |
| 4 | TMDS 数据 1 + | 差分信号 (数据) | 高速 | 2 |
| 5 | TMDS 数据 1 屏蔽 | | 信号屏蔽 | 1 |
| 6 | TMDS 数据 1 - | 差分信号 (数据) | 高速 | 2 |
| 7 | TMDS 数据 0 + | 差分信号 (数据) | 高速 | 1 |
| 8 | TMDS 数据 0 屏蔽 | | 信号屏蔽 | 2 |
| 9 | TMDS 数据 0 - | 差分信号 (数据) | 高速 | 1 |
| 10 | TMDS 时钟 + | 差分信号 (时钟) | 高速 | 2 |
| 11 | TMDS 时钟 屏蔽 | | 信号屏蔽 | 1 |
| 12 | TMDS 时钟 - | 差分信号 (时钟) | 高速 | 2 |
| 13 | CEC | 用于 HDMI CEC 功能 | **低速** | 1 |
| 14 | HEAC+ | (可选) ARC, HEC 等功能 | **低速** | 2 |
| 15 | SCL | 用于 DDC 功能 (i2c) | **低速** | 1 |
| 16 | SDA | 用于 DDC 功能 (i2c) | **低速** | 2 |
| 17 | GND | 接地 (DDC/CEC/HEC) | | 1 |
| 18 | +5V | 电源 (EDID/DDC) | | 2 |
| 19 | HEAC- | (可选) ARC, HEC 等功能 | **低速** | 1 |
| 20 | 接地 | 插头外壳 | | |

注:

+ 位置: `1` 表示在连接器的上方一侧, `2` 表示在连接器的下方一侧.


## 电路板制造记录

| 序号 | 日期 | 版本 | 厂家 | 测试结果 | 备注 |
| :--: | :--- | :--- | :--- | :------- | :--- |
| 1 | 2024-01-03 | pm_hdmi_lpob v0.1 | JLC | 成功 | (1) |

注:

+ (1) 阻焊颜色: 白 (丝印颜色: 黑)

  测试成功: 所有功能符合预期, 工作正常.
