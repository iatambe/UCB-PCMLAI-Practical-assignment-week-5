# Investigating some parameters affecting coupon acceptance

## Project objective

The goal of this project is to investigate some possible characteristics that differentiate drivers who accepted the offered coupon from those who didn't. Our investigation uses the tools of exploratory data analysis, data visualization, etc.

## Data description

Our data comes from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The data can be found in the [data/coupons.csv](data/coupons.csv) file.

Each data point contains information about the driver (such as age, gender, income, marital status), their driving environment (such as presence of other passengers, weather, distance to the place the coupon was offered), and the characteristics of the coupon offered (type of establishment, expiry time), as well as whether the driver accepted the coupon.

## Findings

### Findings for cheaper (under $20 per person) restaurant coupons

Below are some plots showing how acceptance rates of the coupons varied for some different parameters.

- Time of day:
\
![](Plots/Restaurant(<20)CouponAcceptanceRateByTimeOfDay.png)
\
From the graph, we see people are not as likely to accept the coupon at early morning (7AM) and late night (10PM),
and are reasonably likely to accept the coupon at less-early morning (10AM),
but are very likely to accept the coupon in the afternoon and evening (2PM, 6PM).

- Age group:
\
![](Plots/Restaurant(<20)CouponAcceptanceRateByAgeGroup.png)
\
From the graph, we see that there is not a lot of variance (only up to ~ 11 percentage points), but drivers age 25 and under seem most consistent in being more likely to accept the coupon.

- Passenger type
\
![](Plots/Restaurant(<20)CouponAcceptanceRateByPassenger.png)
\
From the graph, we see the driver is more likely to accept the coupon when they are not alone, and even more likely to accept when the other passengers are not kids.

- Expiry time
\
![](Plots/Restaurant(<20)CouponAcceptanceRateByExpiry.png)
\
From the graph, we see that there is a clear increase (by nearly 25 percentage points) in acceptance rates when the expiry is 1 day instead of 2 hours.

### Findings for bar coupons

- In total, about 41% of the bar coupons were accepted.

- Among those who went to bars 3 or fewer times a month, 37% of the bar coupons were accepted.
Among those who went to bars more than 3 times a month, 76% of the bar coupons were accepted.

- The bar coupon acceptance rate among drivers who go to a bar more than once a month and are over the age of 25 was 69%.
The bar coupon acceptance rate among all other drivers was 34%.

- The bar coupon acceptance rate among drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry was 71%.
The bar coupon acceptance rate among all other drivers was 38%.

- The bar coupon acceptance rate among drivers who:
  - go to bars more than once a month, had passengers that were not a kid, and were not widowed, was 67%.
  - go to bars more than once a month and are under the age of 30 was 72%.
  - go to cheap restaurants more than 4 times a month and income is less than 50K was 46%.

## Recommendations

### Recommendations for cheaper (under $20 per person) restaurant coupons

We suggest: 

- focusing on a time range such as 1PM-7PM to maximize coupon acceptance, or possibly 9AM-7PM.
- targeting the under-25 age group.
- targeting drivers who are not alone, and especially drivers with other adult passengers.
- using coupons with the an expiry time of 1 day instead of 2 hours.

### Recommendations for bar coupons

We suggest targeting drivers who visit bars more frequently, and who are in their 20s.

