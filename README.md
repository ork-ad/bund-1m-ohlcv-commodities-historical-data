# BUND 1m OHLCV Commodities Historical Data — Free Sample

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Dataset rows](https://img.shields.io/badge/full_dataset-2_723_099_rows-blue)](https://ork.ad/) [![Updated](https://img.shields.io/badge/weekly_update-every_Sunday-green)](https://ork.ad/) [![Full data on ork.ad](https://img.shields.io/badge/download-ork.ad-orange)](https://ork.ad/)

### → [**Download the full BUND dataset on ork.ad**](https://ork.ad/)

**BUND 1m OHLCV Commodities historical data** — ultra high-quality 1m OHLCV for **Euro Bund**. Extended-session energy and industrial metals — beyond US cash hours. Clean `time, open, high, low, close, volume` CSV for backtesting, algorithmic trading and quantitative research.

## Table of contents

- [Why this dataset?](#why-this-dataset)
- [Download sample CSV](#download-sample)
- [GitHub Pages preview](#github-pages)
- [Sample vs full dataset](#sample-vs-full-dataset)
- [Timeframes on ork.ad](#timeframes-on-orkad)
- [Weekly updates](#weekly-updates)
- [Data preview](#data-preview)
- [Schema](#schema)
- [Code examples](#code-examples)
- [Download full data on ork.ad](#download-full-data)

## Why this dataset?

- **Ultra high-quality 1m OHLCV** for **Euro Bund** (Commodities)
- **Extended-session energy and industrial metals — beyond US cash hours**
- **Clean CSV schema** — `time, open, high, low, close, volume` (no gaps in formatting)
- **Free evaluation sample** on GitHub (`1m`) · **13 timeframes** on [ork.ad](https://ork.ad/) · **2,723,099** `1m` rows in the full archive
- Built for **backtesting**, **algorithmic trading** and **quantitative finance** workflows
- **Weekly refresh** — [ork.ad](https://ork.ad/) every **Sunday**; GitHub `1m` sample updated in sync

> **Sample on GitHub** · `BUND_1m.csv` (106,200 rows, `2026-01-05` → `2026-07-03`). **Full archive on [ork.ad](https://ork.ad/)** — **2,723,099** `1m` rows (~136.69 MB), **13 timeframes** (``1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W``), `2012-08-20` → `2026-07-03`.

## Download sample

**[BUND_1m.csv](https://github.com/ork-ad/bund-1m-ohlcv-commodities-historical-data/blob/main/BUND_1m.csv)** on GitHub ([raw CSV](https://raw.githubusercontent.com/ork-ad/bund-1m-ohlcv-commodities-historical-data/main/BUND_1m.csv)) · [GitHub Releases](https://github.com/ork-ad/bund-1m-ohlcv-commodities-historical-data/releases) when the release workflow is active.

## GitHub Pages

Interactive chart & stats: **[https://ork-ad.github.io/bund-1m-ohlcv-commodities-historical-data/](https://ork-ad.github.io/bund-1m-ohlcv-commodities-historical-data/)**

## Sample vs full dataset

| | **Sample (this repo)** | **Full dataset ([ork.ad](https://ork.ad/))** |
|---|--:|---|
| Instrument | Euro Bund · Commodities | Euro Bund · Commodities |
| Timeframes | `1m` (sample) | **13** — `1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W` |
| 1m rows | 106,200 | **2,723,099** |
| Size | 5.52 MB | ~136.69 MB |
| Period | `2026-01-05` → `2026-07-03` | `2012-08-20` → `2026-07-03` |
| File | `BUND_1m.csv` | ZIP on [ork.ad](https://ork.ad/) |
| Updates | Weekly (Sunday) — GitHub sample | Weekly (Sunday) — all timeframes |

## Timeframes on ork.ad

This GitHub repository ships a **`1m` evaluation sample** only. On **[ork.ad](https://ork.ad/)**, each full asset archive is delivered as a ZIP with **13 gap-free OHLCV timeframes** (one CSV per timeframe):

**1m** · **3m** · **5m** · **15m** · **30m** · **1H** · **2H** · **4H** · **8H** · **12H** · **16H** · **1D** · **1W**

GitHub = `1m` sample · [ork.ad](https://ork.ad/) = all **13** timeframes above for the same instrument.

## Weekly updates

- **[ork.ad](https://ork.ad/)** — Full datasets on ork.ad are updated every Sunday.
- **GitHub (this repo)** — GitHub samples are refreshed weekly (every Sunday), in sync with ork.ad.

When a new `1m` sample is published on GitHub, the README, chart preview and CSV reflect the latest week of data.

## Data preview

First and latest rows from the GitHub sample **`BUND_1m.csv`**:

**First rows**

| time | open | high | low | close | volume |
| --- | --- | --- | --- | --- | --- |
| 2026-01-05T07:01:00Z | 127.021 | 127.184 | 127.021 | 127.184 | 16 |
| 2026-01-05T07:02:00Z | 127.184 | 127.201 | 127.159 | 127.159 | 10 |
| 2026-01-05T07:03:00Z | 127.159 | 127.176 | 127.159 | 127.17 | 11 |
| 2026-01-05T07:04:00Z | 127.17 | 127.171 | 127.159 | 127.165 | 7 |
| 2026-01-05T07:05:00Z | 127.165 | 127.2 | 127.164 | 127.194 | 9 |

**Last rows**

| time | open | high | low | close | volume |
| --- | --- | --- | --- | --- | --- |
| time | open | high | low | close | volume |
| 2026-07-03T19:55:00Z | 126.584 | 126.591 | 126.584 | 126.59 | 3 |
| 2026-07-03T19:56:00Z | 126.59 | 126.591 | 126.589 | 126.589 | 5 |
| 2026-07-03T19:57:00Z | 126.589 | 126.591 | 126.589 | 126.589 | 2 |
| 2026-07-03T19:58:00Z | 126.589 | 126.591 | 126.589 | 126.591 | 3 |

## Schema

```text
time,open,high,low,close,volume
```

## Code examples

### pandas

```python
import pandas as pd

df = pd.read_csv('BUND_1m.csv', parse_dates=['time'])
df.set_index('time', inplace=True)
print(df.describe())
print(df.resample('1h').agg({'open': 'first', 'high': 'max',
                              'low': 'min', 'close': 'last', 'volume': 'sum'}).head())
```

### backtrader

```python
import backtrader as bt
import pandas as pd

df = pd.read_csv('BUND_1m.csv', parse_dates=['time'])
df.set_index('time', inplace=True)

class PandasData(bt.feeds.PandasData):
    params = (('datetime', None), ('open', 'open'), ('high', 'high'),
              ('low', 'low'), ('close', 'close'), ('volume', 'volume'))

cerebro = bt.Cerebro()
cerebro.adddata(PandasData(dataname=df))
# cerebro.addstrategy(YourStrategy)
# cerebro.run()
```

### vectorbt

```python
import pandas as pd
import vectorbt as vbt

df = pd.read_csv('BUND_1m.csv', parse_dates=['time'])
close = df.set_index('time')['close']
fast, slow = vbt.MA.run(close, 10), vbt.MA.run(close, 50)
entries = fast.ma_crossed_above(slow)
exits = fast.ma_crossed_below(slow)
pf = vbt.Portfolio.from_signals(close, entries, exits, init_cash=10_000, freq='1min')
print(pf.stats())
```

## Download full data

The complete **BUND** archive on **[ork.ad](https://ork.ad/)** includes **13 OHLCV timeframes** (`1m`, `3m`, `5m`, `15m`, `30m`, `1H`, `2H`, `4H`, `8H`, `12H`, `16H`, `1D`, `1W`) — **2,723,099** rows at `1m`, plus all other timeframes in the same ZIP.

**[→ Get the full BUND dataset on ork.ad](https://ork.ad/)**

---
*GetData · BUND 1m OHLCV sample on GitHub · Full historical data on [ork.ad](https://ork.ad/) · 2026-07-05 UTC*