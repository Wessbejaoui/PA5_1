# PA5_1
This repo contains the code for the module 5 assignment

### Problem statement:

The final product is a brief report highlighting the differences between customers who did and did not accept the coupons. This practice will allow us to investigate customer behavior and predict the best demographics to benefit from these coupons.

### Data cleaning: 

The data provided is generated from a survey. I initially reviewed the understand the amount of missing information, and if dropping those lines would lead to a better prediction result. However, through this exercise, I decided to keep the missing data and account for it by filling in "NA" instead. The rationale mainly accounts for those who had most of the survey with negligible missing data.

### Results

## The acceptance rate of all coupons is 56.84%:

Among all the coupon recipients, more than half would accept the coupon by either immediately acting upon it or using it before the expiration date. It is worth noticing that coupons are a powerful tool to convert customers for <$20 restaurants and to-go orders. This observation is not true for more expensive restaurants and bars, which could potentially be due to many factors, including people's desire to be seated at restaurants, or indulge in a way without kids or responsibilities, which is the case for the bar. 

![Coupon_acceptance_distribution](https://github.com/user-attachments/assets/b6fa50de-711a-4452-9318-4458129ef085)

## The weather impact on the couponing business model:

As shown below in this histogram, the temperature tends to impact the acceptance rate of coupons. During warm weather, people tend to spend time outside, take their kids out, socialize in groups, and so on. The data shows that between a cold day (30 - 40°F) and a warm day (70 - 80°F), the coupon acceptance rate has tripled. While this seems to be a straightforward result in terms of human behavior prediction and the rationale of when to offer coupons, it remains plausible that these coupons are not spread uniformly. Instead, customers tend to choose some coupons over others.

![temperature_distribution](https://github.com/user-attachments/assets/7dd643ba-d587-4003-85fc-8a12f85b080e)

## Bar coupons model, let's dive in:

The proportion of bar coupons that were accepted is 41.00%. For this observation, I will further investigate the data to understand the profile of the 41% demographics and further capitalize on that acceptance rate. 

![acceptance_vs_rejection_bar_coupons](https://github.com/user-attachments/assets/c019d27e-6118-4f33-a925-e7a7d71caf20)

The barplot below proposes a distribution of coupon acceptance based on the rate of frequenting a bar. It turns out that we could separate the demographics into 2 groups: those who go to the bar more than 3 times/month have a higher chance of using the coupons they receive, twice the probability of those who go to the bar 3 times or less each month. The low acceptance rate was represented at 37.06% while the high acceptance rate was 76.88%. This information is useful and compelling to investigate even further.

![acceptance_rate_by_bar_visit_group](https://github.com/user-attachments/assets/958142cc-586e-4ec8-8ecf-99fdb303efe3)

## Who are the folks who accepted the coupon?

To better understand this data, I introduced the age factor to better represent this demographic. The comprehensive histoplot below breaks down the age categories in function of the acceptance rate and the bar visiting frequency. While it is easy to spot some interesting data right off the bat, such as:
- The absence of those who are between the ages of 31 and 50 in the "gt8" category
- The occurrence of seeing under-21 subjects in bars
- The distribution of subjects aged 25 and above in age is not conclusive enough to draw any findings, in my opinion.
  
This data reveals that there is something else that could be drawn from this data that does not meet the eye right away.

![average_y_score_by_bar_visit_frequency_and_age](https://github.com/user-attachments/assets/afa87034-d019-4200-9d3f-bf4145629ee9)

In the same vein as the observations above, it remains interesting that folks would possibly make decisions in groups, such as friends, family, a coworker, etc. It is possible that some of the decision impact could have been influenced by circumstances, just like the weather temperature, but in this case, the passengers would have a say in whether the coupon gets used or not. Here, I am going to include that information and add a twist where I eliminate certain occupations from this data. The histogram below represents the rate of acceptance under these added conditions to consider (No kid passengers, only certain occupations)

![average_acceptance_rate_by_bar_visit_frequency_and_passenger_type_excluding_kids_and_certain_occupations](https://github.com/user-attachments/assets/9d861fca-f135-4bdb-9c81-63ade7728485)

The data shows that a regular bar goer would always be influenced by the presence of a partner or a friend to increase the acceptance rate of a bar coupon. This is consistent among all 3 groups, and the information could be interpreted in many ways. The one thing we can conclude from this is that a drink is much appreciated with company. 

### Findings

**General Coupon Effectiveness:**

The overall coupon acceptance rate is 56.84%, which signals strong potential for digital or location-based couponing campaigns.

Coupons are especially effective for low-cost food venues (<$20 restaurants and to-go orders), but not as much for bars or expensive restaurants.

**Weather Strongly Influences Coupon Use:**

Acceptance triples in warmer temperatures (70–80°F) compared to colder days (30–40°F).

This implies that seasonal targeting may be critical, summer campaigns may perform much better for family or social-oriented coupons.

**Bar Visit Frequency as a Key Predictor:**

Customers who go to bars more than 3 times/month are more than twice as likely to accept bar coupons (76.88% vs 37.06%).

Frequency-based segmentation could greatly improve ROI for bar coupon promotions.

**Age-Specific Behavior Has Nuance:**

While those under 25 tend to engage more with bar coupons, there's insufficient clarity for ages 25+, likely due to sample size or category overlap.

The data showed unexpected trends, such as under-21s in the "gt8" bar visit group, suggesting either outliers or data inconsistencies worth revisiting.

**Passengers Influence Decisions:**

Acceptance rates are higher when drivers are accompanied by a partner or friend compared to being alone.

When kids or specific occupations (farming/fishing/forestry) are excluded, acceptance rates rise, supporting the idea that social context matters.

**Compound Demographic Segments Matter:**

When looking at drivers who either:

go to bars more than once a month and are over 25

or are under 30 and go out often

or go to cheap restaurants frequently and make under $50K
These groups had significantly higher coupon acceptance than others.

This shows that targeting based on lifestyle clusters (age, income, habits) is more predictive than any one feature alone.

### Next steps

To better predict and influence customer behavior, several strategic steps can be taken based on the findings from the analysis.
First, developing a predictive model using machine learning techniques can help estimate the likelihood of coupon acceptance based on features like age, income, bar or restaurant visit frequency, companion type, weather conditions, and destination.

Additionally, clustering techniques like K-means can segment customers into behavioral groups, such as social drinkers, budget-conscious families, or solo commuters, enabling more targeted promotions. Creating features that capture combinations of behaviors, for example, young social travelers or low-income high-frequency diners, can further enhance model performance and insight clarity.

We can also investigate time-based behavior, such as the day of the week or time of day, which may reveal optimal windows for offering specific coupons, such as happy hour discounts or weekend family deals. 

Finally, visualization tools such as Plotly and Seaborn can further allow stakeholders to easily visualize trends, monitor acceptance rates, and make timely, data-driven marketing decisions. Together, these steps offer a comprehensive approach to optimizing coupon strategies and maximizing customer engagement.
