# Data dictionary

The nine CSV files in `data/raw/stocks/` share these columns:

| Column | Meaning |
| --- | --- |
| `DATE` | Trading date. |
| `SERIES` | Exchange series code (for example, `EQ` or `E1`). |
| `OPEN` | Opening price. |
| `HIGH` | Highest price for the session. |
| `LOW` | Lowest price for the session. |
| `PREV. CLOSE` | Previous session's closing price. |
| `LTP` | Last traded price in the source file. |
| `CLOSE` | Closing price. |
| `VWAP` | Volume-weighted average price. |
| `52W H` | 52-week high value included in the source file. |
| `52W L` | 52-week low value included in the source file. |
| `VOLUME` | Reported trading volume. |
| `VALUE` | Reported traded value/turnover. Values use comma grouping and should be parsed carefully if converted to numbers. |
| `NO. OF  TRADES` | Number of trades reported for the session. |

## Data notes

- The AIRTELPP CSV uses two-digit years in `DATE` and the `E1` series code; the other supplied files use four-digit years and `EQ`. Normalize these fields before combining the CSVs if consistent types are required.
- `VALUE` contains quoted strings with Indian-style digit grouping (for example, lakh/crore grouping), so remove grouping commas before numeric conversion.
- The project owner identifies NSE as the source. The archive does not include the exact download URL, retrieval date, collection method, or redistribution terms. Add those details when available and confirm permission before publishing the raw data.
