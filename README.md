NO WICK STRATEGY — STATUS UPDATE
Generated: 2026-06-15 14:30 AEST
============================================================

## CURRENT PHASE: Phase 5 (New Pair Universe)
  Running grid search on 15 new FX pairs (EUR/JPY, GBP/AUD, GBP/NZD, etc.)
  Status: IN PROGRESS — background job running

## 8 LOCKED PAIRS (Phase 5b)
  GBP/JPY  | 877 trades | 65.1% WR | PF 1.87 | sess 10-19 AEST
  NZD/JPY  | 349 trades | 65.0% WR | PF 1.86 | sess 10-19 AEST
  USD/CHF  | 582 trades | 65.5% WR | PF 1.90 | sess 22-03 AEST (wraps)
  CAD/JPY  | 232 trades | 65.5% WR | PF 1.90 | sess 17-23 AEST
  AUD/CHF  | 184 trades | 65.8% WR | PF 1.92 | sess 22-01 AEST (wraps)
  AUD/CAD  | 160 trades | 65.6% WR | PF 1.91 | sess 15-23 AEST
  AUD/JPY  | 143 trades | 65.0% WR | PF 1.86 | sess 18-23 AEST
  AUD/USD  |  60 trades | 65.0% WR | PF 2.00 | sess 17-20 AEST
  TOTAL:   2,587 trades across 6.4 years (~404/yr, ~34/month)

## PINE SCRIPTS v2 (all 8 generated, clean syntax)
  /Users/jamesfinlay/Trading/Results/NoWick_*_v2.pine
  Fixes: strategy.cancel() on expiry, swing[1] SL, DST-safe timezone, 
         single entry call, multi-line ternary/semicolon syntax fixed

## TV VALIDATION — OANDA:GBPJPY (2026 only)
  Result: 41W / 26L = 61.2% WR | PF 1.38 | 67 trades (Jan-Jun 2026)
  VERDICT: VALID — within expected variance
  - mintick confirmed 0.001, pip=0.01 on OANDA (identical to FX feed)
  - 67 trades → 95% CI = ±11.7% → range 49.5% to 72.9% is all normal
  - TV only loads 6 months of OANDA data (vs Python's 6.4 years)
  - OANDA is correct feed (matches Python backtest data source)
  - FX:GBPJPY showed 71.2% — inflated by different broker candle construction
  Chart: OANDA:GBPJPY 15m | v2 only loaded | old v1 removed

## NEXT STEPS
  1. Phase 5 results → identify new locked pairs from 15 new pairs
  2. Generate Pine v2 scripts for any new locked pairs
  3. TV spot checks for best new pairs
  4. Phase 6: Forward test top pairs on OANDA demo
