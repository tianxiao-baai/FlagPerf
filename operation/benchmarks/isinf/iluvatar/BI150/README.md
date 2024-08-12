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
| flaggems | 0.00E+00    | 0.1TFLOPS       | 0.1TFLOPS        | 0.43% | 0.42% |
| nativetorch | 0.00E+00    | 0.05TFLOPS      | 0.05TFLOPS      | 0.18%      | 0.18%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 0.00E+00    | 5118.75us       | 5142.98us        | 195.36op/s | 194.44op/s | 321684.18us | 5600.41us |
| nativetorch | 0.00E+00    | 11853.5us       | 11859.15us        | 84.36op/s | 84.32op/s | 12240.24us | 12208.26us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 2109.0W | 2128.0W | 20.81W   | /     | 164.0W       | 164.0W      | 0.0W        | 350W  |
| flaggems监控结果 | 2093.8W | 2109.0W | 30.4W   | /     | 164.63W       | 165.0W      | 0.48W        | 350W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 44.675%    | 2.393%   | 48.83°C       | 31.989%        |
| flaggems监控结果 | 47.973%    | 2.399%   | 48.44°C       | 19.489%        |