# Balance Guardian

Balance Guardian is an expert advisor designed to monitor the trading account's profit and loss targets and take necessary actions when these targets are hit. It is developed by Forex Robot Easy Team and more information about this product can be found at [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/balance-guardian-review-optimize-forex-trading-limits/).

## Features

- Ability to set profit target and maximum loss target in account currency
- Automatic closure of all open trades when profit target or maximum loss target is hit
- Deactivation of all expert advisors when profit target or maximum loss target is hit

## Usage

The expert advisor uses two global variables to specify the profit target and maximum loss target:

```mql5
input double profitTarget = 100.0;       // Profit target in account currency
input double maxLossTarget = 50.0;       // Maximum loss target in account currency
```

By default, the `balanceGuardianActive` variable is set to `true` to activate the Balance Guardian functionality. When the profit target or maximum loss target is hit, all open trades are closed and expert advisors are deactivated.

The expert advisor includes the following functions:

### 1. `OnTick()`

This function is executed on every tick and checks if the profit target or maximum loss target is hit. If either target is hit, it closes all open trades using the `CloseAllTrades()` function and deactivates expert advisors using the `DeactivateExpertAdvisors()` function.

### 2. `CloseAllTrades()`

This function iterates through all open trades and closes them using the `OrderClose()` function. It also prints the status of each trade closure.

### 3. `DeactivateExpertAdvisors()`

This function deactivates all expert advisors using the `ExpertRemove()` function. It also prints a message indicating the deactivation of expert advisors.

### 4. `OnInit()`

This function is executed during the expert advisor's initialization. It sets up the initial balance of the trading account and prints it.

### 5. `OnDeinit(const int reason)`

This function is executed during the expert advisor's deinitialization. It prints the reason for deinitialization.

### 6. `OnStart()`

This function is executed when the expert advisor starts. It prints a start message.

## Disclaimer

Forex Robot Easy Team is not the official developer of Balance Guardian. This code is provided as a sample that demonstrates how the expert advisor may work based on the product's description. To find the official developer of this product and obtain detailed reviews and trading results, please refer to [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/balance-guardian-review-optimize-forex-trading-limits/).

Please note that the effectiveness and performance of this expert advisor may vary depending on market conditions and individual trading strategies. It is recommended to thoroughly test the expert advisor on a demo account before using it on a live account.
