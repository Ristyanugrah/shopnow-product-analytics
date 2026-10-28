# ShopNow Product Analytics: Retention, Cohort & Feature Adoption

## Project Overview

This project analyzes user behavior and product performance for ShopNow, focusing on user engagement, customer retention, cohort performance, and feature adoption.

Using Python and Pandas, the analysis explores how users interact with product features, how retention differs across subscription plans, and which early user activities are associated with Day-30 retention.

The goal is to translate behavioral data into actionable insights that can support product optimization and customer engagement strategies.

## Business Objectives

- Measure user engagement through Daily Active Users (DAU), Weekly Active Users (WAU), and Monthly Active Users (MAU).
- Calculate the overall Day-30 customer retention rate.
- Compare retention performance across Free, Basic, and Pro plans.
- Analyze monthly signup cohorts and their retention patterns.
- Identify the most widely adopted product features.
- Compare feature adoption between retained and non-retained users.
- Identify frequently used features during the first seven days among retained users.
- Develop data-driven recommendations to improve early engagement and retention.

## Dataset Overview

The analysis uses two datasets:

**1. Users Dataset**
- `user_id` — Unique user identifier
- `signup_date` — User registration date
- `plan` — Subscription plan
- `country` — User's country
- `retained_day30` — Indicator of Day-30 retention

**2. Events Dataset**
- `user_id` — User identifier associated with an event
- `event_date` — Event date
- `event_name` — Type of user activity
- `plan` — Subscription plan associated with the event
- `day_since_signup` — Number of days since registration

### Dataset Summary

| Metric | Value |
|---|---:|
| Total users | 600 |
| Total events | 38,806 |
| Unique event types | 10 |
| Subscription plans | 3 |
| Signup period | January–February 2024 |
| Event observation period | January–March 2024 |

The notebook reports no missing values in either dataset and confirms that the users table contains 600 unique users.

## Tools & Technologies

- **Python** — Data analysis and processing
- **Pandas** — Data manipulation and aggregation
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Google Colab / Jupyter Notebook** — Interactive analysis

## Analysis Performed

### 1. User Engagement Analysis

Calculated and visualized:
- Daily Active Users (DAU)
- Weekly Active Users (WAU)
- Monthly Active Users (MAU)

These metrics help examine user activity patterns across daily, weekly, and monthly periods.

### 2. Day-30 Retention Analysis

Calculated the overall retention rate using:

`Retention Rate = Retained Users / Total Users × 100%`

The analysis also compares retained and non-retained users to understand the proportion of users who remain active according to the dataset's Day-30 retention indicator.

### 3. Retention by Subscription Plan

Compared Day-30 retention rates across Free, Basic, and Pro plans to identify differences in user retention.

### 4. Cohort Retention Analysis

Grouped users by signup month and tracked their activity across subsequent calendar months.

A cohort retention table and heatmap were created to visualize how retention changes over time.

### 5. Feature Adoption Analysis

Calculated the percentage of users who used each feature at least once, based on unique users recorded for each event type.

The analysis also compares feature adoption across subscription plans.

### 6. Retained vs. Non-Retained Users

Compared feature adoption rates between users classified as retained and non-retained.

This helps identify behavioral differences that may be useful for developing retention strategies.

### 7. First Seven-Day Feature Usage

Analyzed feature usage during the first seven days after signup among users marked as retained.

This analysis explores which early activities are common among users who subsequently meet the Day-30 retention definition.

## Key Findings

The notebook reports the following results:

### Overall Retention

- Total users: **600**
- Retained users: **249**
- Non-retained users: **351**
- Day-30 retention rate: **41.50%**

### Retention by Subscription Plan

| Plan | Day-30 Retention Rate |
|---|---:|
| Pro | 77.01% |
| Basic | 50.00% |
| Free | 27.89% |

The Pro plan has the highest reported retention rate, while the Free plan has the lowest.

### Feature Adoption and Early Engagement

The notebook compares feature adoption across plans and retention groups. Its preliminary findings highlight the following:

- Voucher usage (`use_voucher`) shows a substantial reported adoption gap between retained and non-retained users.
- The first-seven-day analysis identifies `app_open` as the most frequently used feature among retained users in the reported results.
- Cohort retention analysis provides a framework for examining how user activity changes after signup.

**Important:** Feature-level percentages and rankings should be verified against the final notebook outputs before being treated as definitive findings. Some charts use manually entered values rather than values generated directly from the analysis tables.

## Strategic Recommendations

### 1. Strengthen Early User Engagement

Simplify the onboarding experience and guide new users from opening the application toward meaningful product activities, such as viewing products, searching, and adding items to the cart.

### 2. Improve Retention Among Free Users

Investigate barriers faced by Free-plan users and test targeted onboarding, feature education, and engagement campaigns.

### 3. Encourage Relevant Voucher Usage

Explore whether relevant voucher offers and clearer voucher discovery can encourage users to engage more frequently with the product.

Voucher usage is associated with a higher reported retention rate in this analysis, but further testing is required to determine whether encouraging voucher usage improves retention.

### 4. Monitor Cohort Performance

Track retention by signup cohort to identify whether changes in onboarding or product experiences correspond with improvements in user retention.

### 5. Build a Product KPI Monitoring Framework

Monitor DAU, WAU, MAU, Day-30 retention, and feature adoption regularly to evaluate product performance and identify areas requiring further investigation.

## Limitations

- The analysis covers 600 users and 38,806 recorded events.
- The event observation period ends on March 31, 2024.
- Monthly cohort retention is based on recorded activity and may be affected by the length of the observation period.
- The dataset's `retained_day30` indicator is used as provided; its exact business definition should be confirmed.
- Feature adoption differences do not establish that a feature causes higher retention.
- Hardcoded chart values should be replaced with values calculated directly from the analysis tables.
- Recommendations should be validated through additional analysis or controlled experiments before implementation.

## Repository Structure

```text
shopnow-product-analytics/
├── shopnow_product_analytics.ipynb
├── README.md
└── data/
    └── README.md
```

The `data/` directory is optional. If the source datasets cannot be shared, document the required filenames and columns in `data/README.md` rather than uploading confidential or restricted data.

## How to Run

1. Clone or download this repository.
2. Open `shopnow_product_analytics.ipynb` in Google Colab or Jupyter Notebook.
3. Upload the required users and events datasets.
4. Update the dataset paths in the notebook.
5. Execute the notebook cells in order.
6. Review the generated tables, visualizations, and exported CSV files.

Before publishing, ensure that the notebook runs from beginning to end without errors and that all reported metrics match the final outputs.

## Author

**Risty Anugrah Dwi Septiana**

- GitHub: [Ristyanugrah](https://github.com/Ristyanugrah)
- Data Analytics Portfolio: [data-analytics-portfolio](https://github.com/Ristyanugrah/data-analytics-portfolio)
- Portfolio Website: [risty-portfolio.vercel.app](https://risty-portfolio.vercel.app/)

---

*This project was developed for data analytics practice and portfolio development, focusing on user engagement, customer retention, cohort analysis, and product feature adoption.*
