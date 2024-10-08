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
| flaggems | True    | 0.41TFLOPS       | 0.41TFLOPS        | 0.13% | 0.13% |
| nativetorch | True    | 0.36TFLOPS      | 0.36TFLOPS      | 0.12%      | 0.12%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 7930.28us       | 7921.66us        | 126.1op/s | 126.24op/s | 816985.95us | 3327.31us |
| nativetorch | 8929.59us       | 8942.59us        | 111.99op/s | 111.82op/s | 15540.94us | 3126.66us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1638.0W | 1716.0W | 120.84W   | /     | 283.48W       | 287.0W      | 4.09W        | 400W  |
| flaggems监控结果 | 1657.5W | 1716.0W | 101.32W   | /     | 314.62W       | 318.0W      | 4.19W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 2.332%    | 1.402%   | 52.33°C       | 21.43%        |
| flaggems监控结果 | 0.635%    | 1.386%   | 52.63°C       | 21.43%        |
