# 🐱 BTC 网格自动交易系统

<div align="center">

![Cute Cat](https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif)

**一只可爱的小猫守护你的交易~ 喵~**

[![GitHub stars](https://img.shields.io/github/stars/wuyutanhongyuxin-cell/var_last?style=social)](https://github.com/wuyutanhongyuxin-cell/var_last)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Variational-orange.svg)](https://omni.variational.io)

</div>

---

## ✨ 功能特点

| 功能 | 描述 |
|:---:|:---|
| 🎯 | **智能网格交易** - 自动在价格区间内布置买卖订单 |
| 🛡️ | **RSI/ADX 风控** - 基于技术指标的风险控制 |
| ⏰ | **冷却机制** - 触发风控后自动冷却 15 分钟 |
| 📊 | **动态仓位** - 根据持仓自动调整买卖比例 |
| 🔄 | **自动撤单** - 智能撤销偏离价格的订单 |

---

## 🐾 快速开始

### 1. 打开交易平台

访问 [Variational OMNI](https://omni.variational.io/perpetual/BTC)

### 2. 运行脚本

按 \`F12\` 打开开发者工具，在 Console 中粘贴 \`var_grid.js\` 的全部内容

### 3. 设置仓位

在交易界面手动设置开仓大小，脚本会自动开始运行

---

## 🎮 常用指令

\`\`\`javascript
// 🚀 启动交易（间隔3秒）
btcAutoTrader.startAutoTrading(3000);

// 🛑 停止交易
btcAutoTrader.stopAutoTrading();

// 📊 查看状态
btcAutoTrader.getStatus();

// 🗑️ 取消所有挂单
btcAutoTrader.cancelAllOrder();

// 🔄 重置风控冷却
btcAutoTrader.resetRiskCooldown();

// 🧹 清空订单记录
btcAutoTrader.clearOrderHistory();
\`\`\`

---

## ⚙️ 参数配置

### 网格策略配置

\`\`\`javascript
static GRID_STRATEGY_CONFIG = {
    TOTAL_ORDERS: 18,           // 总订单数
    WINDOW_PERCENT: 0.12,       // 窗口宽度 12%
    SELL_RATIO: 0.5,            // 卖单比例 50%
    BUY_RATIO: 0.5,             // 买单比例 50%
    BASE_PRICE_INTERVAL: 10,    // 基础价格间距 $10
    SAFE_GAP: 20,               // 安全间距 $20
    MAX_MULTIPLIER: 15,         // 最大仓位倍数
    RSI_MIN: 30,                // RSI 下限
    RSI_MAX: 70,                // RSI 上限
    ADX_TREND_THRESHOLD: 25,    // ADX 趋势阈值
    ADX_STRONG_TREND: 30        // ADX 强趋势阈值
};
\`\`\`

---

## 🛡️ 风控机制

<div align="center">

\`\`\`
         ┌─────────────────┐
         │   市场状态检测   │
         └────────┬────────┘
                  │
    ┌─────────────┼─────────────┐
    ▼             ▼             ▼
┌───────┐   ┌───────────┐   ┌───────┐
│震荡市场│   │ 中等趋势  │   │强趋势 │
│ADX<25 │   │25<ADX<30 │   │ADX>30│
└───┬───┘   └─────┬─────┘   └───┬───┘
    │             │             │
    ▼             ▼             ▼
  正常交易     谨慎交易     触发风控
                            冷却15分钟
\`\`\`

</div>

---

## 📝 更新日志

### v2.0.0 (2026-01-29) 🐱

- ✅ 修复撤单功能选择器
- ✅ 修复平仓功能选择器
- ✅ 适配平台最新 UI 更新
- ✅ 优化确认按钮检测逻辑

### v1.0.0

- 🎉 初始版本发布
- 📊 网格交易核心功能
- 🛡️ RSI/ADX 风控系统

---

## ⚠️ 免责声明

<div align="center">

**本脚本仅供学习交流使用，不构成投资建议**

加密货币交易存在风险，请谨慎操作

使用本脚本造成的任何损失，作者概不负责

</div>

---

## 🎁 支持作者

如果觉得有帮助，欢迎使用邀请码注册：

| 邀请码 | 福利 |
|:---:|:---:|
| \`OMNINU3G7KVK\` | 返点原路返回 |
| \`OMNIBGZ4ETT9\` | 返点原路返回 |

---

<div align="center">

**Made with 💖 and lots of ☕**

![Cat Coding](https://media.giphy.com/media/VbnUQpnihPSIgIXuZv/giphy.gif)

*小猫咪陪你一起写代码~ 喵~*

</div>
