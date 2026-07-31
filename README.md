# Trae PB-ROE 价值选股 Skill

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Trae](https://img.shields.io/badge/platform-Trae-7B68EE.svg)](https://trae.ai)

> 基于 PB-ROE 框架的 A 股价值选股工具，五维 17 因子量化评分系统。

## 简介

PB-ROE 是 A 股最经典的价值投资框架之一。核心理念：

**ROE 越高的公司，市场理应给予越高的 PB。如果一只股票的 PB 相对于其 ROE 明显偏低，就意味着它被市场低估了。**

本 Skill 将这一理念系统化为 **5 个维度 × 17 个因子** 的量化评分体系，覆盖估值、盈利质量、成长性、财务健康和安全边际，输出结构化的分析报告。

## 框架

| 维度 | 权重 | 因子数 | 核心指标 |
|------|------|--------|---------|
| 估值 | 30% | 3 | PB-ROE 偏离度、PB 行业分位、PB/ROE 性价比 |
| 盈利质量 | 25% | 4 | ROE 绝对值、ROE 5年稳定性、ROE 趋势、杜邦质量 |
| 成长性 | 20% | 3 | 营收 CAGR、净利润 CAGR、ROE 增长动量 |
| 财务健康 | 15% | 4 | 资产负债率、利息覆盖倍数、现金流质量、商誉占比 |
| 安全边际 | 10% | 3 | PB 历史分位、股息率、破净程度 |

## 评级标准

| 得分 | 星数 | 含义 |
|------|------|------|
| 85-100 | ★★★★★ | PB-ROE 黄金坑 |
| 70-84 | ★★★★☆ | 显著低估，重点关注 |
| 55-69 | ★★★☆☆ | 合理偏低，放入观察池 |
| 40-54 | ★★☆☆☆ | 估值合理，建议观望 |
| < 40 | ★☆☆☆☆ | 偏高或价值陷阱 |

## 安装

1. 下载 `SKILL.md` 文件
2. 放入 Trae 项目的 `.trae/skills/pb-roe-screening/` 目录
3. 在 Trae 中对话时，提到"PB-ROE 选股""价值股筛选"即可自动触发

```bash
# 直接 clone 使用
git clone https://github.com/你的用户名/trae-pb-roe-screening.git
cp -r trae-pb-roe-screening/.trae/skills/pb-roe-screening 你的Trae项目/.trae/skills/
```

## 使用示例

在 Trae 中直接输入：

- "用 PB-ROE 框架分析工商银行"
- "筛选 A 股 PB-ROE 排名前 20 的股票"
- "对比茅台、五粮液、泸州老窖的 PB-ROE 得分"

## 输出内容

每次分析输出：

1. 核心数据一览（PB / ROE / PB÷ROE / 市值）
2. 五维 17 因子逐项打分明细
3. 杜邦分析（ROE 驱动来源拆解）
4. 同行业 PB-ROE 回归定位
5. 综合评分 + 投资结论

## 注意事项

- 银行、保险等金融行业自动调整权重
- ROE 为负的公司不适用此框架
- 周期性行业标注"景气高点低 PB 陷阱"提示
- 轻资产公司（创业板/科创板）需结合 PE 辅助判断

## 许可

MIT License

## 免责声明

本工具仅供学习研究，不构成任何投资建议。股市有风险，投资需谨慎。
