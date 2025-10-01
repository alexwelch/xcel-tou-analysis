# Xcel Energy TOU vs Flat Rate Calculator

A spreadsheet tool to help Xcel Energy customers in Colorado determine whether Time-of-Use (TOU) pricing or flat rate pricing makes more financial sense for their household.

## Background

In 2025, Xcel Energy changed their TOU peak hours to 5-9 PM on weekdays (previously 3-7 PM). This calculator helps you understand the break-even point and estimate your annual costs under each pricing structure.

**Key Finding: The break-even point is 15.4% on-peak usage** (18.6% during summer months June-September).

- If **more than 15.4%** of your usage is during peak hours → **Flat rate is better**
- If **less than 15.4%** is during peak hours → **TOU is better**

## Who Should Use This?

- Xcel Energy residential customers in Colorado
- Households with solar panels (includes production credit analysis)
- EV owners trying to optimize charging costs
- Anyone considering opting out of TOU pricing

## Current Rates (as of October 1, 2025)

**TOU Pricing:**
- On-peak (5-9 PM weekdays): $0.18331/kWh (non-summer), $0.21277/kWh (summer)
- Off-peak (all other times): $0.06792/kWh (non-summer), $0.07884/kWh (summer)

**Flat Rate:**
- All hours: $0.08570/kWh (non-summer), $0.1038/kWh (summer)

*Summer months: June, July, August, September*

## How to Use

### 1. Download the Spreadsheet
Download `TOU_analysis.xlsx` from the [latest release](link-to-your-release).

### 2. Input Your Data

**For Usage Cost Analysis (rows 13-15):**
- **On-Peak Usage %**: Estimate what percentage of your monthly electricity usage happens between 5-9 PM on weekdays
- **Total Energy Consumed (kWh)**: Enter your total monthly consumption from your Xcel bill

**For Solar Owners (rows 29-31):**
- **On-Peak Production %**: Estimate what percentage of your solar production happens during peak hours (5-9 PM)
- **Total Energy Produced (kWh)**: Enter your monthly solar production

### 3. Interpret Results

**Usage Cost Comparison (rows 22-24):**
- **Positive difference** = Flat rate saves you money
- **Negative difference** = TOU saves you money

**Production Credits (rows 36-38, solar only):**
- **Negative difference** = TOU earns you more credits
- **Positive difference** = Flat rate earns you more credits

**Indifference Point (rows 45-46):**
- Shows the exact on-peak percentage where both pricing structures are equal
- Compare your actual usage pattern to this threshold

## Example Scenarios

### Scenario 1: EV Owner, No Solar
- Charges EV overnight (off-peak)
- Typical daytime usage
- **Estimated on-peak usage: 10-15%**
- **Recommendation: Stay on TOU** ✅

### Scenario 2: Home All Day, High Evening Usage
- Work from home, run appliances throughout day
- Cook dinner, laundry in evening
- **Estimated on-peak usage: 25-30%**
- **Recommendation: Switch to Flat Rate** ✅

### Scenario 3: Solar + EV
- Solar covers most daytime usage
- EV charges overnight
- Exports during peak hours
- **Estimated on-peak usage: 5-10%**
- **Recommendation: Stay on TOU** ✅ (benefits from both low usage costs and high export credits)

## The Math

The indifference point formula:

x = (Flat Rate - Off-Peak Rate) / (On-Peak Rate - Off-Peak Rate)


Where `x` = proportion of usage during on-peak hours

**Non-summer calculation:**
x = (0.08570 - 0.06792) / (0.18331 - 0.06792)
x = 0.01778 / 0.11539
x = 0.154 (15.4%)


**Summer calculation:**
x = (0.1038 - 0.07884) / (0.21277 - 0.07884)
x = 0.02496 / 0.13393
x = 0.186 (18.6%)


## Tips for Reducing On-Peak Usage

If you're close to the break-even point, here are ways to reduce on-peak usage:

- **EV charging**: Set timer to start after 9 PM
- **Dishwasher/laundry**: Run after 9 PM or before 5 PM
- **Pool pumps**: Schedule for off-peak hours
- **Smart thermostats**: Pre-cool before 5 PM in summer
- **Cooking**: Use slow cookers, instant pots during off-peak

## Data Sources

- [Xcel Energy TOU Rate Schedule](https://co.my.xcelenergy.com/s/billing-payment/residential-rates/time-of-use-pricing)
- [Colorado Public Radio: Xcel TOU Changes](https://www.cpr.org/2025/02/21/xcel-is-changing-when-it-charges-more-for-peak-time-energy-use/)
- Rates effective October 1, 2025

## Contributing

Found an error? Have suggestions? 

- Open an [Issue](link-to-issues)
- Submit a pull request
- Share your results and feedback

## Disclaimer

This calculator is for educational purposes only. Actual costs may vary based on:
- Additional fees and charges on your Xcel bill
- Seasonal rate changes
- Your specific rate plan
- Transmission and distribution charges

Always verify with your actual Xcel Energy bill and consult their official rate schedules.

## License

This project is released under the MIT License. Feel free to use, modify, and share.

## About

Created by an Xcel customer trying to optimize their solar + EV setup. Shared freely to help the Colorado community make informed decisions about TOU pricing.

---

**Questions?** Open an issue or discuss in the [r/Denver](https://reddit.com/r/denver) community.
