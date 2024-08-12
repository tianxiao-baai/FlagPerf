# 参评AI芯片信息

* 厂商：ILUVATAR

* 产品名称：BI150
* 产品型号：BI150
* TDP：W

# 所用服务器配置

* 服务器数量：1


* 单服务器内使用卡数：1
* 服务器型号：
* 操作系统版本：Ubuntu 20.04.6 LTS
* 操作系统内核：linux5.4.0-148-generic
* CPU：
* docker版本：20.10.25
* 内存：
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本
FlagGems:>联系邮箱: contact-us@iluvatar.com获取版本(FlagGems-0710_pointwise_use_tid)

# 评测结果

## 核心评测结果

| 评测项  | 平均相对误差(with FP64-CPU) | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | 2.01E-07    | 0.16TFLOPS       | 0.16TFLOPS        | 0.66% | 0.65% |
| nativetorch | 1.66E-07    | 0.09TFLOPS      | 0.09TFLOPS      | 0.37%      | 0.37%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 3.61E-07    | 3329.21us       | 3357.1us        | 300.37op/s | 297.88op/s | 779528.2us | 3780.82us |
| nativetorch | 2.09E-07    | 5926.53us       | 5951.03us        | 168.73op/s | 168.04op/s | 6167.72us | 6243.39us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 2052.0W | 2071.0W | 26.87W   | /     | 140.0W       | 140.0W      | 0.0W        | 350W  |
| flaggems监控结果 | 2052.0W | 2090.0W | 38.0W   | /     | 169.91W       | 172.0W      | 6.35W        | 350W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 39.402%    | 2.389%   | 42.98°C       | 6.989%        |
| flaggems监控结果 | 38.954%    | 2.396%   | 48.47°C       | 6.989%        |