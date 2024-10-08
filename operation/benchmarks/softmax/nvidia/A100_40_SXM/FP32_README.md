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
| flaggems | True    | 0.32TFLOPS       | 0.32TFLOPS        | 1.63% | 1.63% |
| nativetorch | True    | 0.25TFLOPS      | 0.25TFLOPS      | 1.27%      | 1.27%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 30461.69us       | 30479.36us        | 32.83op/s | 32.81op/s | 1493095.44us | 9403.05us |
| nativetorch | 39113.73us       | 39139.33us        | 25.57op/s | 25.55op/s | 517653.19us | 16028.46us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1628.82W | 1638.0W | 36.71W   | /     | 257.2W       | 275.0W      | 12.28W        | 400W  |
| flaggems监控结果 | 1626.86W | 1638.0W | 40.18W   | /     | 254.58W       | 271.0W      | 10.57W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 1.037%    | 1.669%   | 50.57°C       | 61.849%        |
| flaggems监控结果 | 0.878%    | 1.663%   | 50.09°C       | 52.351%        |
