# Crypto-Exchange-Real-Time-Risk-Monitoring-System

This project simulates a real-time risk monitoring system used in a derivatives / crypto exchange.

The goal is to reproduce the core risk control logic used in high-leverage trading platforms, including:

- Volatility monitoring
- VaR risk model
- Margin & leverage control
- Liquidation engine
- Stress test engine
- Insurance fund simulation
- ADL (Auto Deleveraging)
- Final risk dashboard

The system is implemented using Python + pandas with real BTC market data.

---

## Risk System Architecture

```
Market Data
   ↓
Rolling Volatility / VaR
   ↓
Margin Model (Initial / Maintenance)
   ↓
Account Risk Calculation
   ↓
Liquidation Engine
   ↓
Bankrupt Detection
   ↓
Insurance Fund
   ↓
ADL (Auto Deleveraging)
   ↓
Risk Dashboard / Monitor
```

This flow simulates the core risk control pipeline used in derivatives exchanges.

---

## Project Structure

```
01_market_data.ipynb
02_volatility_var.ipynb
03_margin_model.ipynb
04_liquidation_engine.ipynb
05_stress_test.ipynb
06_insurance_fund_adl.ipynb
07_final_risk_dashboard.ipynb
```

Each notebook represents one module in an exchange risk system.

---

## Module Description

### 01 Market Data

Load BTC price data

- return
- rolling return
- price series

Used for risk calculation.

---

### 02 Volatility + VaR

Rolling volatility

VaR model:

VaR = exposure × volatility × Z

Supports:

- 95%
- 99%

Used for dynamic risk control.

---

### 03 Margin Risk Model

Simulates exchange margin logic

- initial margin
- maintenance margin
- risk ratio
- leverage

Used to determine liquidation trigger.

---

### 04 Liquidation Engine

Multi-account simulation

- different balance
- different exposure
- different leverage
- risk ranking

Detects liquidation accounts.

---

### 05 Stress Test Engine

Extreme market simulation

-10%
-20%
-30%

Checks:

- liquidation count
- bankrupt accounts
- risk concentration

Used for tail risk analysis.

---

### 06 Insurance Fund + ADL

When bankrupt occurs:

loss → insurance fund

If fund insufficient:

trigger ADL

ADL queue based on:

profit × leverage

Simulates real exchange ADL logic.

---

### 07 Final Risk Dashboard

Final monitoring panel shows:

- price
- volatility
- VaR
- liquidation count
- bankrupt count
- insurance fund
- ADL status
- top risk accounts

This is similar to a real exchange risk monitor.

---

## Purpose

This project is built to understand how exchange risk systems work.

Focus areas:

- Derivatives risk
- Margin trading risk
- Liquidation risk
- Liquidity risk
- Insurance fund risk
- ADL mechanism

The goal is to combine trading risk experience with quantitative risk models.

---

## Background

Experience in:

- FX trading risk
- Precious metals trading
- Derivatives risk control
- Margin trading risk management

Currently studying:

- Python
- Quant risk
- Exchange risk system
- Crypto derivatives risk
