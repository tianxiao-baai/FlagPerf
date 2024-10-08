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
| flaggems | True    | 0.34TFLOPS       | 0.34TFLOPS        | 0.11% | 0.11% |
| nativetorch | True    | 0.24TFLOPS      | 0.24TFLOPS      | 0.08%      | 0.08%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 3141.34us       | 3203.07us        | 318.34op/s | 312.2op/s | 524416.01us | 3281.54us |
| nativetorch | 4515.39us       | 4515.84us        | 221.46op/s | 221.44op/s | 15994.08us | 4539.99us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1612.0W | 1716.0W | 147.08W   | /     | 329.5W       | 335.0W      | 5.44W        | 400W  |
| flaggems监控结果 | 1599.0W | 1794.0W | 195.0W   | /     | 397.94W       | 405.0W      | 4.08W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.719%    | 1.152%   | 54.11°C       | 18.899%        |
| flaggems监控结果 | 0.599%    | 1.138%   | 56.76°C       | 16.186%        |
