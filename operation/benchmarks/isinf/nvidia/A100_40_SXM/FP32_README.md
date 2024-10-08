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

https://github.com/FlagOpen/FlagGems. Commit ID: 801377f03ba4649bc2d839ff34e38be66ee8a633

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | True    | 0.28TFLOPS       | 0.27TFLOPS        | 1.42% | 1.41% |
| nativetorch | True    | 0.11TFLOPS      | 0.11TFLOPS      | 0.55%      | 0.55%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | 
| flaggems | 3887.72us       | 3906.56us        | 257.22op/s | 255.98op/s | 929892.76us | 3970.6us |
| nativetorch | 10044.82us       | 10056.7us        | 99.55op/s | 99.44op/s | 37919.1us | 10100.43us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1606.8W | 1638.0W | 62.4W   | /     | 258.32W       | 262.0W      | 2.45W        | 400W  |
| flaggems监控结果 | 1560.0W | 1638.0W | 78.0W   | /     | 254.87W       | 259.0W      | 3.57W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 1.162%    | 2.288%   | 49.38°C       | 27.499%        |
| flaggems监控结果 | 0.759%    | 2.288%   | 47.48°C       | 17.212%        |