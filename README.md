
# Predicting Airline Customer Satisfaction

Logistic regression on 25,976 passenger survey records — quantifying which cabin, loyalty, and service factors actually move satisfaction, and whether upgrading economy food service would pay off.

**Author:** Jeremy Juke | M.S. Business Intelligence & Data Analytics, Saint Mary's University of Minnesota (BIA 650, 2025)

---

## Problem

Airlines invest heavily in service improvements without always knowing which ones change customer satisfaction. Using passenger survey data, this project models satisfaction (satisfied / dissatisfied) across cabin classes and loyalty segments to answer a concrete investment question: **would upgrading food and drink service in economy cabins measurably improve satisfaction?**

## Data

- 25,976 passenger survey records (public airline passenger satisfaction dataset)
- Binary outcome: satisfied (1) / dissatisfied (0)
- Key predictors: cabin class (Business / Eco / Eco Plus), customer loyalty (loyal / disloyal), food-and-drink score, and related service ratings

## Method

Logistic regression with odds-ratio (point estimate) interpretation, evaluated by concordance statistics — chosen so every coefficient translates directly into a business statement stakeholders can act on.

## Results

**Model quality:** 81.3% concordant pairs, c-statistic = 0.833 — strong predictive performance for survey data.

**Key point estimates (odds ratios):**

| Effect | Odds Ratio |
|---|---|
| Business class vs. Eco Plus | **11.1x** satisfaction odds |
| Loyal vs. disloyal customer | 2.7x |
| Food & drink score (per 1-point increase) | **1.39x** (+39% odds) |
| Eco vs. Eco Plus | 0.88x |

**Descriptive findings:**

- Business class passengers account for the highest satisfaction share (33% of the total population satisfied); Eco passengers are the most dissatisfied segment (35% of total population)
- Loyal business-class passengers are the most satisfied group overall
- Disloyal customers show flat satisfaction regardless of class or food scores — service upgrades don't move customers who have already disengaged

## Answer to the business question

Yes, with targeting: each one-point improvement in food-and-drink scores raises satisfaction odds by ~39%, and the effect concentrates among **loyal economy passengers** — the segment where satisfaction is lowest but still responsive.

**Recommended implementation:**

1. Pilot food enhancements in Eco and Eco Plus cabins
2. Collect post-implementation data through follow-up sentiment surveys
3. Retrain the model on updated data to validate the probability estimates before full rollout

## Tools

Logistic regression (odds-ratio estimation, concordance evaluation), Excel, presentation delivered as a recorded stakeholder briefing

---

*Full analysis and presentation materials in this repository.*
