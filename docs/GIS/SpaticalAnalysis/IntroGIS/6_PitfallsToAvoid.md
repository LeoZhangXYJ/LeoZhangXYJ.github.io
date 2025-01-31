# 6 Pitfalls to Avoid

## Representing Count

**Problem:**  
If we sum the **number** of individuals in each polygon, we get two maps that appear to be giving us two completely different population distribution patterns.

**Solution:**  
Represent count as **ratios**, such as the number of deaths per number of people or the number of people per square kilometer.

## MAUP

**MAUP:** Modifiable Aerial Unit Problem

Continuing with the uniform point distribution from the last section, let’s assume that as part of the survey, two variables (v1 and v2) were recorded for each point.

1. It’s obvious from the adjoining scatter plot that there is little to no correlation between variables v1 and v2 at the individual level; both the slope and coefficient of determination, $R^2$, are close to 0.
2. For example, if we aggregated v1 and v2 using the uniform aggregation scheme highlighted earlier, we get the following relationship: $R^2$ = 0.03.
3. If we aggregate the same point data using the non-homogeneous aggregation scheme, we get yet another characterization of the relationship between v1 and v2: $R^2$ = 0.75.
