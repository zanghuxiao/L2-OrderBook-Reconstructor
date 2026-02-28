# L2 OrderBook Reconstructor

本项目基于 Level-2 行情数据构建事件驱动订单簿重建引擎，实现任意时间切片的盘口恢复，并在此基础上构建流动性指标与可视化分析框架，用于市场微观结构研究。

## 核心功能
- **事件驱动订单簿状态引擎**
- **支持多源数据（快照 / 逐笔成交 / 逐笔委托）整合**
- **整数化价格处理，规避浮点误差**
- **异常数据处理（乱序 / 撤单异常 / 倒挂修正）**。
- **吞吐量约 70,000+ events/sec**。
- **单元测试 + 集成测试覆盖核心逻辑**。

## 如何运行
1. 安装依赖：`pip install -r requirements.txt`
2. 生成数据：运行 `scripts/mock data generator.ipynb`
3. 清洗数据：运行 `scripts/data_cleaner.ipynb`
4. 验证引擎：运行 `test/test_integration.ipynb`
