# Visualising Customer Churn with Tableau and Python

This is a visualisation project where I aim to showcase the capabilities of Tableau and Python in visualising a dataset. 

In this project, I analyse churn in the telecommunication industry, which is a mature field of research. In telecommunication, churning is a popular issue for service providers, 
since offerings are typically on a prepaid subscription basis, and customers have a wealth of choice from different service
providers, so jumping between them to get the best deals is relatively easy. It is, therefore, in the responsibility of the Customer Relationship 
Management (CRM) team to deeply understand customers’ current experience with the services offered and take steps to prevent
cancellations before they happen.

Preventing churn is important, mainly because of costs. It is shown that, in the telecommunication sector, the costs of acquiring a new customer 
can be up to six times greater than those of retaining an existing customer, and the difference is even larger if there are more competitors within a market.

# The questions to answer

The project aims to understand the following problems:

1. Understand the company’s performance in this quarter in terms of customer retention.
2. Understand the behaviours of churning customers.
3. Understand the characteristic differences between staying and churning customers.

# The data

I conducted my analysis on the Telecom Customer Churn dataset, originated from Maven Analytics and made available on Kaggle. 
The dataset is available at https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics/data.

The data contains information about 7043 customers in a telecommunication company in the United States in the second quarter of 2022. 
It has 38 fields, of which 22 are categorical and 16 are numeric. The dataset covers numerous angles including:
- Demographic information (e.g. age, gender)
- Location (e.g. city, zip code)
- Service information and statistics (e.g. contract type, subscriptions, charges, refunds, revenues)
- Marketing statistics (e.g. offers)
- Customer status: tenure in months, status (churned, stayed, joined).

# The tools

I used Tableau and Python for this project. You can find the full packaged workbook (`telecom_churn.twbx`) and the Python notebook (`customer-churn-notebook.ipynb`)
within this repo. The extracted data resides in the `data` directory, and all visuals are in the `visuals` directory.

# The results

I deliberately made the visuals to speak for themselves, so there is little caption needed.

## Quarter performance in customer retention

1. Of all customers who are not known to be newly joined, 28.4% churned. This ratio represents almost one in four customers that joined the company.

![py_stayed-vs-churned](https://github.com/user-attachments/assets/14f82197-02b8-42d4-8024-7d22cd98596e)

## Churner behaviours

2. Competitor is the number one reason customers are leaving the company. Of the five categories of churn, those who churned because of competitors account
for 45% of all who churned.

![tableau_Churn categories](https://github.com/user-attachments/assets/b1f365af-8535-4144-9efb-c8ee9bddc8b1)

3. The top two reasons of customers leaving for competitors are to seek
better offers and better devices from them.

![tableau_Churn reasons text](https://github.com/user-attachments/assets/c6e479e5-3307-4ddd-8f5d-f8cb49d20625)

4. Customers are churning considerably more at over $65/month
charge. There is also a cohort of customers taking low-priced offers (from $18 – 21/month)
and leaving after a short period of time (Figure 5 further highlights the mean and median
tenure of this cohort). The mean tenure for this cohort is 6.85 months, while the median is
just 1 month.

![tableau_Monthly charge dist](https://github.com/user-attachments/assets/4b66741b-8f35-4798-9ab8-c02c94afda0a)

![tableau_Histograms of Monthly Charge against Average (above) and Median (below) Customer Tenure (Churners Only)](https://github.com/user-attachments/assets/ad261659-c55f-4736-ae8f-4e04335d84de)

5. Most churners leave the company in the first five months of signing up.

![tableau_Time to Churn](https://github.com/user-attachments/assets/a7870585-4b40-422a-bd63-5011508a5320)

6. In terms of the five marketing offers the company is running, Offer E
leads to the greatest number of churners. It is also the only offer with more churners than
stayers. Offer B is the best performing in terms of retaining customers.

![tableau_Offer Slopegraph](https://github.com/user-attachments/assets/22a3df76-1766-4bee-92fa-654026acc0e7)

## Characteristic differences between Stayers and Churners

7. Customers aged 35 – 45 are most likely to stay, and customers aged 65+
are most likely to churn. Customers aged 18 – 25 are least likely to churn. This suggests a
higher tolerance level in younger cohorts.

![py_age-dist-by-cohort](https://github.com/user-attachments/assets/fb721c6e-6d86-4d91-a0df-89e0ef24f19d)

8. Male customers are slightly more likely to stay than female customers.
There is not a significant difference in gender in those who churned.

![py_gender-count](https://github.com/user-attachments/assets/29cfb31d-9554-4da2-b66e-f810fdb4618c)

9. In terms of charges, churners are paying more than stayers, both
monthly (Subplot 1) and throughout their whole tenure. (Subplot 2) Churners are paying
considerably more than stayers in extra data. (Subplot 3) Some long-staying churners (40+
months) are paying more long-distance charges than their stayed counterparts. (Subplot 4)
Since charges are regressed on tenure, there is overall a positive trend in both stayers and
churners for all subplots. (i.e. as they stay longer, they pay more)

![py_tenure-vs-charge](https://github.com/user-attachments/assets/60ef7f37-229c-46a6-846c-d3691b9371c4)

10. The majority of churners (first 2 churner bars in the revenue
distribution) generated less than $1,000 in total revenues, while the majority of stayers
generated up to $5,000.

![py_revenue-by-cohort](https://github.com/user-attachments/assets/b706d85a-a10c-45ab-b722-a0e652688988)

11. Stayers are referring more people to join than churners, on average.
The slope of the trend line for stayers are steeper than that for churners, meaning that, on
average, stayers also tend to refer more than churners as they stay longer.

![py_tenure-vs-referrals](https://github.com/user-attachments/assets/78568617-16a7-43bc-a9bd-8347063cdf35)

# Business recommendations 

The data already spoke for itself; these are some recommendations to improve customer retention based on statistics from
this dataset:

- Reviewing quality of products/services that led to customers churning early on in their tenure.
- Implementing competitor analysis to understand current market pricings, in order to stay competitive.
- Directing Marketing to focus on younger cohorts for future campaigns, particularly those under 45.
- Offering more incentives for staying longer, such as extra data, distance charge waivers, and higher internet speeds. The same incentives can also be offered for referring customers to the service.
- Considering withdrawing Offer E from the market, and directing budgets to high- performing offers, such as Offer B.
- Reviewing staff training practices, and reviewing audio records of staff interactions with customers to address service quality concerns.
