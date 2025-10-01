# Xcel Energy TOU vs Flat Rate Calculator

I'm an Xcel customer in Denver with solar and an EV, and I was trying to figure out if the new TOU pricing changes make sense for my household. I built this spreadsheet to help, and I'm sharing it here in case it helps other folks in the same boat.

## ⚠️ Important Disclaimer

**This spreadsheet could have errors. There are no warranties or guarantees.**

I built this for my own use and I'm sharing it as-is. You are 100% responsible for:
- Verifying all rates and formulas are correct
- Confirming the data matches your specific situation
- Double-checking any calculations before making decisions
- Consulting Xcel's official rate schedules

**Use this at your own risk.** That being said, I would appreciate hearing about any [issues here](https://github.com/alexwelch/xcel-tou-analysis/issues)

## What This Does

This calculator helps you figure out whether Xcel's Time-of-Use (TOU) pricing or flat rate pricing will cost you less money. It also includes a section for solar owners to calculate production credits. 

**The key finding:** The break-even point is around **15.4% on-peak usage** (18.6% in summer). 

- If more than 15.4% of your electricity usage happens during peak hours (5-9 PM weekdays) → flat rate is probably better
- If less than 15.4% is during peak hours → TOU is probably better

## Who Might Find This Useful

- Xcel customers in Colorado trying to decide between TOU and flat rate
- Solar owners who want to calculate production credits under each plan
- EV owners optimizing charging schedules
- Anyone who's confused by the rate changes and wants to see the actual numbers

## Current Rates (as of October 1, 2025)

**TOU Pricing:**
- On-peak (5-9 PM weekdays): $0.18331/kWh (non-summer), $0.21277/kWh (summer)
- Off-peak (all other times): $0.06792/kWh (non-summer), $0.07884/kWh (summer)

**Flat Rate:**
- All hours: $0.08570/kWh (non-summer), $0.1038/kWh (summer)

*Summer = June, July, August, September*

**Please verify these rates against your own Xcel bill.** Rates can change and may vary by location.

## How to Use This

### Step 1: Download the Spreadsheet
Grab `TOU_analysis.xlsx` from the [latest release](link-to-your-release).

### Step 2: Input Your Data

**Usage Cost Analysis (rows 13-15):**
- **On-Peak Usage %**: Your best guess at what percentage of your monthly electricity gets used between 5-9 PM on weekdays. You might be able to glean some of it from your bill or energy monitoring tools if you have them (my solar monitoring system shows me hour by hour consumption).
- **Total Energy Consumed (kWh)**: Get this from your Xcel bill - it's your total monthly usage. 

**Solar Production Credits (rows 29-31) - skip if you don't have solar:**
- **On-Peak Production %**: Estimate what percentage of your solar production happens during 5-9 PM. Your solar monitoring system probably has this information. For most people this is pretty low since the sun is setting. This is on of the big concerns with the new TOU hours.
- **Total Energy Produced (kWh)**: Your monthly solar production from your monitoring system.

### Step 3: Look at the Results

**Usage Cost Comparison (rows 22-24):**
- If the difference is **positive** → flat rate saves you money
- If the difference is **negative** → TOU saves you money

**Production Credits (rows 36-38, solar only):**
- If the difference is **negative** → TOU gets you more credits
- If the difference is **positive** → flat rate gets you more credits

**Indifference Point (rows 45-46):**
- This shows the exact on-peak percentage where both plans cost the same
- Compare your actual usage to this number to see which side you're on

## Real-World Examples

### Example 1: EV Owner, No Solar
You charge your EV overnight and have pretty typical daytime usage. You might use less than 15% of your power on-peak. **TOU likely saves you money.**

### Example 2: Home All Day
You work from home, run appliances throughout the day, cook dinner around 6 PM, do laundry in the evening. Your on-peak usage might be 25-30%. **Flat rate would be better.**

### Example 3: Solar + EV
Your solar covers most daytime usage, you charge your EV overnight, and you export power during peak hours. Your on-peak grid usage is probably 5-10%. **TOU likely saves you money on both usage and production credits.**

## The Math Behind It

The break-even formula is:

x = (Flat Rate - Off-Peak Rate) / (On-Peak Rate - Off-Peak Rate)


Where `x` = the proportion of your usage during on-peak hours

**Non-summer:**
x = (0.08570 - 0.06792) / (0.18331 - 0.06792) = 15.4%


**Summer:**
x = (0.1038 - 0.07884) / (0.21277 - 0.07884) = 18.6%


This is called an "indifference point" - the point where you'd be indifferent between the two pricing options because they cost exactly the same.

## Tips for Shifting Usage Off-Peak

If you're close to the break-even point, here are some ways to reduce on-peak usage:

- **EV charging**: Set your charger to start after 9 PM
- **Dishwasher/laundry**: Run them after 9 PM or on weekends
- **Pool pumps**: Schedule for off-peak hours
- **Thermostats**: Pre-cool your house before 5 PM in summer
- **Meal prep**: Use slow cookers or instant pots that you can set during off-peak times

## Where I Got the Data

- [Xcel Energy TOU Rate Schedule](https://co.my.xcelenergy.com/s/billing-payment/residential-rates/time-of-use-pricing)
- [Colorado Public Radio article on the TOU changes](https://www.cpr.org/2025/02/21/xcel-is-changing-when-it-charges-more-for-peak-time-energy-use/)
- My own Xcel bills

**Again: Please verify these rates yourself.** I could have made mistakes copying them over.

## Want to Help?

If you find errors, have suggestions, or want to share your results:
- Open an [Issue](https://github.com/alexwelch/xcel-tou-analysis/issues)
- Submit a pull request or reach out to me using this issues form if you want to improve the spreadsheet.
- Share your feedback - I'd love to know if this was helpful or if something's confusing

## More Disclaimers (Because They're Important)

- This is for educational purposes only
- Your actual costs will vary based on fees, charges, and your specific rate plan
- I'm not affiliated with Xcel Energy
- Rates can change - always check Xcel's official schedules
- This doesn't account for transmission charges, distribution charges, or other fees on your bill
- Seriously, double-check everything before making any decisions. I read that once you change away from TOU, you can't change back for a year.

## License

MIT License - use it, modify it, share it. No restrictions.

## About This Project

I built this because I was trying to optimize my own bill and couldn't find a simple calculator anywhere. Figured if I needed it, other folks probably do too. 

If this helps you save some money or just understand your bill better, that's awesome. If you find mistakes, please let me know so I can fix them.
