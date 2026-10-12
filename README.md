# will the customer accept the coupon?
Full analysis Notebook: Module5.ipynb
Dataset: data/in-vehicle-coupon-recommendation.csv (https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation)

This project explores survey data collected on Amazon Mechnicl Turk, in which drivers were placed in different driving scenarios (destination, weather, time of day, who else was in the car, etc) and a coupon was given to one of the five venue types
1. Bar
2. Coffee House
3. carry-out & Takeaway
4. cheap Restuarant
5. Price Restaurant

The goal is to make someone accept a coupon so that the coupons could eventually be targetted more effectively, sending the right offer to the right person in the right situation 

## What we found
- Overall, a bit more than half of all offered coupons were acepted, but at the same time varies by coupon type, cheap, low-effort offers. Coffee house, cheap restaurants get accepted much often than expensive restaurant
-closer look at bar coupons had a below-average acceptance rate and represent a clear oppurtunity to be smarter about who receive them
-people who are regular visitors of bars accept the bar coupons at much higher rate and also when they had friends with them than with partners or kids with them
- Life stage matters too - younger, single people without kids accepted bar coupons more often than older married people with kids - which makes sense given that bars tend to be more social, less family-oriented venue.
- coupons that stayed valid for a full day were accepted more often than one's that expired in just 2 hours

# What we Recommend
- Send bar coupons to the regular visitors of the bars
- prioritize younger single people without kids
- default coupons to longer expiration window
- don't waste bar coupons on in-frequent visitors to the bar

# Next Steps
- Build predictive model(e.g logistic regression) using the single identified above(bar visit, frquency,passenger type, age, marital status, coupon expiration) to score how likely a given rider is to accept a coupon in real time
- Repeat the same for other coupon types
- validate with real-world A/B test before rolling out a live targeting strategy

Module5/
|-README.md
|-Prompt_coupon.ipynb
|-data/in-vehicle-coupon-recommendation.csv

Tools/Techologies
Python
Pandas
Numpy
Matplotlib
Seaborn
Jupyter Notebook


