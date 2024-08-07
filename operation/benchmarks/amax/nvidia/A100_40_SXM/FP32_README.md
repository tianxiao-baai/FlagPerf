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

https://github.com/FlagOpen/FlagGems. Commit ID: 7042de1d8fb6f978596322faaeda6b55ca1ae5ec

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | : True    | 0.36TFLOPS       | 0.36TFLOPS        | 1.84% | 1.83% |
| nativetorch | : True    | 0.34TFLOPS      | 0.34TFLOPS      | 1.76%      | 1.75%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 18744.77us       | 18765.82us        | 53.35op/s | 53.29op/s | 2989468.51us | 18853.41us |
| nativetorch | 19601.09us       | 19630.08us        | 51.02op/s | 50.94op/s | 246469.82us | 19694.48us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1620.67W | 1716.0W | 80.37W   | /     | 268.39W       | 272.0W      | 1.56W        | 400W  |
| flaggems监控结果 | 1612.0W | 1638.0W | 73.54W   | /     | 268.85W       | 271.0W      | 1.97W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.623%    | 1.082%   | 48.21°C       | 64.375%        |
| flaggems监控结果 | 0.632%    | 1.073%   | 48.21°C       | 64.982%        |