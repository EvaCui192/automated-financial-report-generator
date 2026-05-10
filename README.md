# Automated Financial Report Generator  
# Python 自动化财务报告生成器

## 1. Project Background 项目背景

本项目以 **万科 A** 为案例，构建一个 Python 自动化财务分析工具。项目使用已经整理好的 Excel 财务数据作为输入，自动读取财务数据、计算核心财务比率、生成财务趋势图，并输出结构化财务分析总结。

本项目的重点不是单独分析某一家公司的全部经营细节，而是展示一个可复用的财务分析自动化流程：

```text
标准化 Excel 财务数据
→ Python 自动读取
→ 自动计算财务指标
→ 自动生成图表
→ 自动输出财务分析总结
```

只要后续替换为相同格式的其他公司财务数据表，该流程也可以复用于其他上市公司分析。

This project uses **Vanke A** as a case study to build a Python-based automated financial report generator. The project takes a structured Excel financial dataset as input, automatically calculates key financial ratios, generates financial trend charts, and exports a structured financial analysis summary.

The purpose of this project is not only to analyse one company, but also to demonstrate a reusable financial analysis workflow:

```text
Standardised Excel financial data
→ Python data processing
→ Automatic financial ratio calculation
→ Chart generation
→ Financial summary export
```

---

## 2. Case Company 案例公司

| Item | Description |
|---|---|
| Company | Vanke A / 万科 A |
| Data Type | Annual financial statement data |
| Period | 2021–2025 |
| Unit | RMB 100 million / 亿元 |
| Input File | `万科财务数据.xlsx` |

---

## 3. Input Data Structure 输入数据结构

The input Excel file is stored in:

```text
data/raw/万科财务数据.xlsx
```

The worksheet contains annual financial data with the following fields:

| 字段 | 含义 |
|---|---|
| 年份 | Reporting year |
| 营业收入 | Revenue |
| 营业成本 | Operating cost |
| 毛利润 | Gross profit |
| 营业利润 | Operating profit |
| 净利润 | Net profit |
| 归母净利润 | Net profit attributable to shareholders |
| 货币资金 | Cash and cash equivalents |
| 流动资产 | Current assets |
| 总资产 | Total assets |
| 流动负债 | Current liabilities |
| 总负债 | Total liabilities |
| 短期借款 | Short-term borrowings |
| 一年内到期的非流动负债 | Non-current liabilities due within one year |
| 长期借款 | Long-term borrowings |
| 应付债券 | Bonds payable |
| 总有息债务 | Total interest-bearing debt |
| 股东权益合计 | Total shareholders' equity |
| 经营活动现金流量净额 | Net operating cash flow |
| 投资活动现金流量净额 | Net investing cash flow |
| 筹资活动现金流量净额 | Net financing cash flow |
| 利息费用 | Interest expense |
| 未分配利润 | Retained earnings / undistributed profit |
| 盈余公积 | Surplus reserve |
| 留存收益 | Retained earnings |

---

## 4. Financial Ratios Calculated 自动计算的财务指标

本项目自动计算以下核心财务指标：

| 指标 | 计算逻辑 |
|---|---|
| 营业收入增长率 | 本年营业收入 / 上年营业收入 - 1 |
| 毛利率 | 毛利润 / 营业收入 |
| 营业利润率 | 营业利润 / 营业收入 |
| 净利率 | 净利润 / 营业收入 |
| 归母净利率 | 归母净利润 / 营业收入 |
| 总资产回报率 ROA | 净利润 / 总资产 |
| 净资产收益率 ROE | 净利润 / 股东权益合计 |
| 资产负债率 | 总负债 / 总资产 |
| 流动比率 | 流动资产 / 流动负债 |
| 短期有息债务 | 短期借款 + 一年内到期的非流动负债 |
| 现金短债比 | 货币资金 / 短期有息债务 |
| 总有息债务占总资产比例 | 总有息债务 / 总资产 |
| 经营现金流净利润比 | 经营活动现金流量净额 / 净利润 |
| 利息费用率 | 利息费用 / 营业收入 |
| 留存收益占股东权益比例 | 留存收益 / 股东权益合计 |

---

## 5. Tools Used 使用工具

- Python
- pandas
- numpy
- matplotlib
- openpyxl
- Jupyter Notebook
- GitHub

---

## 6. Methodology 分析流程

本项目按照以下步骤进行：

1. 读取 Excel 财务数据文件
2. 检查数据结构、年份范围和缺失值
3. 根据原始财务数据自动计算核心财务比率
4. 保存完整财务分析结果和财务比率表
5. 生成财务趋势图
6. 自动生成中文财务分析总结
7. 输出 `.csv`、`.xlsx`、`.txt` 和 `.png` 文件
8. 将 Notebook、数据、图表和结果文件上传至 GitHub

The analysis follows these steps:

1. Read the structured Excel financial dataset
2. Check data structure, year range and missing values
3. Automatically calculate key financial ratios
4. Export financial ratio tables and processed results
5. Generate financial trend charts
6. Automatically generate a written financial analysis summary
7. Export results in `.csv`, `.xlsx`, `.txt` and `.png` formats
8. Upload the notebook, data, outputs and charts to GitHub

---

## 7. Key Outputs 主要输出

### Processed Data 处理后数据

```text
data/processed/万科财务分析结果.csv
```

### Output Tables 输出表格

```text
outputs/万科财务比率表.csv
outputs/万科财务分析结果汇总.xlsx
```

### Text Summary 分析总结

```text
outputs/万科财务分析总结.txt
```

### Charts 图表

```text
charts/营业收入与利润趋势.png
charts/盈利能力指标趋势.png
charts/资产负债结构趋势.png
charts/偿债能力与债务压力趋势.png
```

---

## 8. Key Charts 主要图表

本项目生成以下核心图表：

1. **营业收入与利润趋势图**  
   展示营业收入、净利润和归母净利润的变化趋势。

2. **盈利能力指标趋势图**  
   展示毛利率、营业利润率、净利率和归母净利率的变化趋势。

3. **资产负债结构趋势图**  
   展示总资产、总负债和股东权益合计的变化趋势。

4. **偿债能力与债务压力趋势图**  
   展示资产负债率、总有息债务占总资产比例和现金短债比的变化趋势。

---

## 9. Project Structure 项目结构

```text
automated-financial-report-generator
│
├── README.md
├── requirements.txt
│
├── data
│   ├── raw
│   │   └── 万科财务数据.xlsx
│   │
│   └── processed
│       └── 万科财务分析结果.csv
│
├── notebooks
│   └── financial_report_generator.ipynb
│
├── outputs
│   ├── 万科财务比率表.csv
│   ├── 万科财务分析总结.txt
│   └── 万科财务分析结果汇总.xlsx
│
└── charts
    ├── 营业收入与利润趋势.png
    ├── 盈利能力指标趋势.png
    ├── 资产负债结构趋势.png
    └── 偿债能力与债务压力趋势.png
```

---

## 10. Reusability 可复用性

本项目的核心价值在于可复用性。只要用户按照相同格式整理新的公司财务数据 Excel 文件，程序就可以自动完成后续分析流程。

例如，如果需要分析其他公司，只需要：

1. 保持 Excel 列名和结构一致
2. 替换 `data/raw` 文件夹中的输入数据
3. 重新运行 Notebook
4. 自动生成新的财务比率表、图表和分析总结

The key value of this project is reusability. Users only need to update the input Excel file using the same structure, and the program can automatically generate financial ratios, charts and a written summary for another company.

---

## 11. Conclusion 结论

本项目展示了如何使用 Python 将财务报表分析流程自动化。通过读取标准化 Excel 财务数据，程序可以自动计算盈利能力、成长能力、偿债能力、债务压力和现金流质量等指标，并生成图表和文字总结。

该项目说明，Python 不仅可以用于数据处理，也可以帮助财务分析人员提高重复性报表分析工作的效率。

This project demonstrates how Python can automate financial statement analysis. By reading structured Excel financial data, the program automatically calculates profitability, growth, leverage, liquidity and cash flow indicators, and generates charts and a written summary.

The project shows how Python can improve efficiency in repetitive financial analysis workflows.

---

## 12. Notes 说明

本项目仅用于学习、作品集展示和财务分析自动化流程演示，不构成投资建议。

本项目使用的财务数据基于已整理的公开财务报表信息。历史财务表现不代表未来结果。


This project is for educational and portfolio demonstration purposes only. It does not constitute investment advice.

The financial data is based on organised public financial statement information. Historical performance does not guarantee future results.
