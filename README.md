# Nike DCF Valuation Model

5-year discounted cash flow valuation of Nike in Excel, with WACC from CAPM, bear/base/bull scenarios and a sensitivity table.

## Result

Base-case fair value is **$68.26 per share**. Bear to bull range: **$54 to $85**.

| Step | $ millions |
|---|---|
| Sum of PV of free cash flow (Years 1-5) | 25,835 |
| PV of terminal value | 74,725 |
| Enterprise value | 100,561 |
| Less: total debt | (8,920) |
| Plus: cash | 10,750 |
| Equity value | 102,391 |
| Shares outstanding | 1,500M |
| **Fair value per share** | **$68.26** |

Terminal value is about 74% of enterprise value.

## Assumptions

- Last revenue $51,000M, growth 6% a year, operating margin 14%, tax rate 21%
- Free cash flow = EBIT x (1 - tax rate)
- Terminal growth 2.5% (Gordon Growth)
- WACC **9.18%** from CAPM: risk-free rate 4.3%, equity beta 1.10, equity risk premium 5.0% (cost of equity 9.8%), pre-tax cost of debt 4.5%, 90% equity / 10% debt weights

These inputs are assumptions and should be refreshed with current market data.

## Scenarios

| Scenario | Revenue growth | Operating margin | Fair value / share | vs base |
|---|---|---|---|---|
| Bear | 4% | 12% | $54.00 | -20.9% |
| Base | 6% | 14% | $68.26 | 0% |
| Bull | 8% | 16% | $84.54 | +23.8% |

## Sensitivity: fair value per share ($)

| WACC \ Revenue growth | 4% | 5% | 6% | 7% | 8% |
|---|---|---|---|---|---|
| 7.18% | 89.34 | 93.31 | 97.43 | 101.70 | 106.12 |
| 8.18% | 73.73 | 76.94 | 80.27 | 83.72 | 87.29 |
| 9.18% | 62.80 | 65.48 | **68.26** | 71.14 | 74.12 |
| 10.18% | 54.72 | 57.01 | 59.39 | 61.84 | 64.39 |
| 11.18% | 48.51 | 50.50 | 52.56 | 54.70 | 56.91 |

A 1-point change in WACC moves the base value by roughly $9 to $12 per share.

## Limitations

- Simplified model: free cash flow ignores capex, depreciation and working capital changes
- No comparison with the current market price
- Lease liabilities are not included in debt

## Files

- `nike-dcf-valuation.xlsx`: four sheets: DCF Model, WACC (CAPM), Scenarios and Sensitivity. All inputs are on the first two sheets, and the scenario and sensitivity tables recalculate from them
