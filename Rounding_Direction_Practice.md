# Rounding signed readings to a step

[Download the practice workbook](Rounding_Direction_Practice.xlsx). It contains a blank `Starter` sheet and a formula-based `Answers` sheet. The six readings are original synthetic data. All step sizes are positive.

## Tasks

1. On `Starter`, fill `D7:D12` with each reading rounded down to the multiple in column C, using `FLOOR`.
2. Fill `E7:E12` with each reading rounded toward zero to a whole number, using `ROUNDDOWN`.
3. Fill `F7:F12` with the lower integer, using `INT`.
4. Compare the negative reading with the exact negative multiple. Explain why an exact multiple stays unchanged under `FLOOR`, while its integer result can differ.
5. Change `B7` to `-14.1`. The formula answers should update to `-14.5`, `-14`, and `-15`. Restore `B7` to `12.8` afterward.

The yellow cells are the answer area. The `Answers` sheet links to the readings and steps on `Starter`, so an input change also updates the worked solutions. Use the formula bar to inspect a result. The exercise can be completed offline without an account.

<details>
<summary>Formula hints and answer key</summary>

Enter `=FLOOR(B7,C7)` in D7, `=ROUNDDOWN(B7,0)` in E7, and `=INT(B7)` in F7. Copy the formulas down to row 12.

| Reading | Positive step | FLOOR | ROUNDDOWN to 0 places | INT |
| ---: | ---: | ---: | ---: | ---: |
| 12.8 | 0.5 | 12.5 | 12 | 12 |
| -12.8 | 0.5 | -13 | -12 | -13 |
| 0 | 0.5 | 0 | 0 | 0 |
| 12.5 | 0.5 | 12.5 | 12 | 12 |
| -12.5 | 0.5 | -12.5 | -12 | -13 |
| 0.6 | 0.25 | 0.5 | 0 | 0 |

With a positive step, `FLOOR` selects the nearest multiple less than or equal to the reading. `ROUNDDOWN` moves toward zero. `INT` selects the lower integer. In the negative nonmultiple case, -13 is below -12.8, while -12 is closer to zero.

</details>

Original exercise contributed by the maintainer of [SheetTutor](https://sheettutor.top/), a free browser-based Excel practice site with no signup required. The workbook is self-contained; the website is optional. These new materials are contributed under this repository's MIT license.
