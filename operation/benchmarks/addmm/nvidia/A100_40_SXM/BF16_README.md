# 参评AI芯片信息

* 厂商：Nvidia

* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1
* 单服务器内使用卡数: 1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID: 3c10679326b32ea5f037db50cc397d41c0ff1934

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | True    | 234.35TFLOPS       | 249.1TFLOPS        | 75.11% | 79.84% |
| nativetorch | True    | 223.36TFLOPS      | 227.57TFLOPS      | 71.59%      | 72.94%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 586.68us       | 551.94us        | 1704.5op/s | 1811.8op/s | 7012544.35us | 595.59us |
| nativetorch | 615.56us       | 604.16us        | 1624.53op/s | 1655.19op/s | 137563.58us | 743.5us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1540.5W | 1794.0W | 149.78W   | /     | 397.42W       | 402.0W      | 4.11W        | 400W  |
| flaggems监控结果 | 1540.5W | 1794.0W | 149.78W   | /     | 399.7W       | 408.0W      | 3.88W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.678%    | 1.114%   | 62.96°C       | 2.534%        |
| flaggems监控结果 | 0.829%    | 1.116%   | 62.92°C       | 2.534%        |
