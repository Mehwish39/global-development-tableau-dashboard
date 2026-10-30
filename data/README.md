# Data

**The dataset is not included in this repository.**

## Source

Gapminder public development indicators, accessed through Plotly sample data:

- Gapminder data portal: https://www.gapminder.org/data/
- Plotly sample datasets: https://plotly.com/python-api-reference/generated/plotly.data.html (`plotly.express.data.gapminder()`)

Gapminder data can be reused freely with attribution to Gapminder.

## Structure used in this project

A long-format table: **one row per country × year × indicator**.
6,856 raw rows → 6,816 rows after cleaning · 142 countries · 12 years (1952–2007, every 5 years) · 4 indicators.

| Column | Type | Description |
|---|---|---|
| `record_id` | integer | Row identifier |
| `country_raw` | text | Country name (raw; needs trimming/case fix) |
| `continent_raw` | text | Continent (raw; needs trimming/case fix) |
| `year_raw` | integer | Year (1952–2007, 5-year steps) |
| `iso_alpha` | text | ISO 3-letter country code (used for the map) |
| `iso_num` | integer | ISO numeric country code |
| `indicator_code` | text | `HEALTH_LE`, `POP_TOTAL`, `ECON_GDP_PC`, `ECON_GDP_TOTAL` |
| `indicator_name_raw` | text | Indicator display name |
| `sdg_theme` | text | Related Sustainable Development Goal theme |
| `unit` | text | Unit of the value (years, people, constant international dollars) |
| `indicator_value` | decimal | The measured value |
| `income_context_raw` | text | Derived income-context label (raw) |
| `priority_band_raw` | text | Derived priority label: High / Medium Priority / Monitor (raw) |
| `source_dataset` | text | Source description |
| `source_note` | text | Notes (also used to identify duplicate rows) |

## Indicators

| Code | Indicator | Unit | Aggregation used |
|---|---|---|---|
| `HEALTH_LE` | Life expectancy at birth | Years | Average |
| `POP_TOTAL` | Population | People | Sum (single year only) |
| `ECON_GDP_PC` | GDP per capita | Constant international $ | Average |
| `ECON_GDP_TOTAL` | Estimated total GDP | Constant international $ | Not used in KPIs |
