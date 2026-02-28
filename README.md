# L2 OrderBook Reconstructor (百万级精度订单簿重建引擎)

这是一个高性能的量化交易工具，用于通过 Level2 快照和逐笔成交/委托数据实时重建订单簿。

## 项目亮点
- **高精度**: 支持百万分之一（1e-6）的价格精度，规避浮点误差。
- **自愈功能**: 内置盘口自愈机制（Self-healing），自动处理高频场景下的盘口倒挂。
- **高性能**: 经测试，吞吐量可达 70,000+ 笔流水/秒。
- **高覆盖测试**: 100% 通过 38 项单元测试及端到端集成测试。

## 如何运行
1. 安装依赖：`pip install -r requirements.txt`
2. 生成数据：运行 `scripts/mock data generator.ipynb`
3. 清洗数据：运行 `scripts/data_cleaner.ipynb`
4. 验证引擎：运行 `test/test_integration.ipynb`
