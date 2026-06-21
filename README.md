# KPI Framework, Business Experiment Analysis & Decision Recommendation

## Student Information

**Name:** Shlok Sonawane
**Student ID:** 2511721
**Repository:** shlok-sonawane-2511721-part2-kpi-framework-business-experiment-analysis

---

# Project Overview

This project analyzes the results of a business experiment conducted to evaluate whether a new onboarding experience improves subscription conversion performance compared to the existing onboarding process.

The objective is to use business analytics techniques to define a KPI framework, identify the most important success metric, analyze experiment results, evaluate risks using guardrail metrics, and provide a data-driven business recommendation.

---

# Business Context

A subscription-based business conducted an A/B experiment to test a new onboarding experience.

Two groups were compared:

* **Control Group:** Existing onboarding experience
* **Treatment Group:** New onboarding experience

The business must determine whether the new onboarding experience should be launched based on measurable business outcomes.

---

# Business Problem Statement

The business needs to decide whether the new onboarding experience should be launched to all users.

This decision impacts:

* Revenue growth
* Customer acquisition
* Product adoption
* Customer experience

The primary objective is to increase subscription conversion while ensuring customer satisfaction and operational efficiency are maintained.

Before making a recommendation, evidence must demonstrate:

* Improvement in conversion performance
* Positive revenue impact
* No significant increase in business risk

---

# Dataset Description

The dataset contains experiment results for users who participated in the onboarding test.

### Key Variables

* User ID
* Group (Control/Treatment)
* Region
* Device Type
* Traffic Source
* Plan Type
* Landing Page Visit
* Trial Start
* Onboarding Completion
* Paid Conversion
* Revenue (30 Days)
* Refund Request
* Support Tickets
* Days to Convert
* Engagement Score

---

# Repository Structure

```text
part2_kpi_framework/

├── data/
│   └── campaign_experiment_data.xlsx

├── analysis/
│   ├── experiment_analysis.xlsx
│   └── hypothesis_test_notes.md

├── outputs/
│   ├── experiment_summary.xlsx
│   ├── recommendation_memo.md
│   └── kpi_tree.png

├── screenshots/
│   ├── summary_metrics.png
│   ├── hypothesis_test_output.png
│   └── kpi_tree_preview.png

└── README.md
```

---

# North Star Metric

## Paid Conversion Rate

### Definition

Paid Conversion Rate measures the percentage of users who become paying customers.

### Why It Was Selected

Paid Conversion Rate was chosen as the North Star Metric because:

* Directly measures business growth
* Closely linked to subscription revenue
* Reflects onboarding effectiveness
* Represents overall experiment success

### Why Other Metrics Are Supporting Metrics

The following metrics support the North Star Metric:

* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Revenue per User
* Engagement Score

These metrics help explain performance but do not directly represent business growth.

### Risk of Optimizing Blindly

Focusing only on conversion rate could:

* Increase refund requests
* Increase support burden
* Reduce customer satisfaction
* Create low-quality conversions

Therefore, guardrail metrics must also be evaluated.

---

# KPI Tree Summary

## North Star Metric

Paid Conversion Rate

### Primary KPI Drivers

#### 1. Acquisition Quality

Sub-drivers:

* Landing Page Visit Rate
* Trial Start Rate

#### 2. Onboarding Effectiveness

Sub-drivers:

* Onboarding Completion Rate
* Days to Convert

#### 3. Revenue Performance

Sub-drivers:

* Revenue per User
* Revenue per Converted User

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Engagement Score

A visual KPI tree is included in:

```text
outputs/kpi_tree.png
```

---

# Data Preparation & Validation

The experiment dataset was reviewed and validated before analysis.

Checks performed:

### Missing Values

Reviewed for all fields.

### Duplicate User IDs

Checked to ensure users were uniquely assigned.

### Group Counts

Control and Treatment group sizes were verified.

### Invalid Binary Values

Binary fields were reviewed for consistency.

### Revenue Outliers

Revenue values were reviewed for unusual observations.

### Segment Distribution

Distribution was compared across:

* Region
* Device Type
* Plan Type

This ensured balanced experiment groups.

---

# Experiment Analysis Approach

The analysis compared Control and Treatment groups across key business metrics.

Metrics evaluated:

* User Count
* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Average Revenue per User
* Average Revenue per Converted User
* Refund Rate
* Support Ticket Rate
* Engagement Score
* Average Days to Convert

Segment-level comparisons were also performed.

---

# Hypothesis Testing

## Objective

Determine whether the Treatment onboarding experience improves Paid Conversion Rate.

### Null Hypothesis (H0)

The Treatment experience does not improve Paid Conversion Rate.

### Alternative Hypothesis (H1)

The Treatment experience improves Paid Conversion Rate.

### Test Type

One-Tailed Hypothesis Test

### Significance Level

α = 0.05

### Decision Rule

* Reject H0 if p-value < 0.05
* Fail to Reject H0 if p-value ≥ 0.05

The detailed hypothesis testing notes are included in:

```text
analysis/hypothesis_test_notes.md
```

---

# Experiment Results Summary

| Metric                   | Control | Treatment |
| ------------------------ | ------- | --------- |
| User Count               | 693     | 715       |
| Paid Conversion Rate     | 3.17%   | 6.99%     |
| Average Revenue per User | 51.75   | 53.88     |
| Refund Rate              | 0.00%   | 0.42%     |
| Engagement Score         | 57.03   | 62.93     |

Key observations:

* Conversion rate improved significantly.
* Revenue increased.
* Engagement improved.
* Refund rate increased slightly but remained low.

---

# Guardrail Metrics Considered

The recommendation was not based solely on conversion performance.

The following guardrail metrics were evaluated:

### Refund Rate

Ensures conversion gains are not driven by low-quality customers.

### Support Ticket Rate

Measures operational burden and customer issues.

### Engagement Score

Measures customer quality and product interaction.

Results indicated no major business risk.

---

# Final Recommendation

## Recommendation: Launch

The Treatment onboarding experience demonstrated:

* Higher Paid Conversion Rate
* Higher Revenue per User
* Higher Engagement Score
* Acceptable Guardrail Performance

The analysis supports launching the new onboarding experience.

---

# Risks and Limitations

### Risks

* Future customer behavior may differ.
* Additional monitoring is required after launch.

### Limitations

* Results are limited to the experiment population.
* Some long-term impacts may not yet be visible.
* Revenue quality should continue to be monitored.

---

# Next Steps

1. Launch the new onboarding experience.
2. Continue monitoring guardrail metrics.
3. Track conversion performance after deployment.
4. Conduct follow-up optimization experiments.

---

# Screenshots Included

### Summary Metrics

```text
screenshots/summary_metrics.png
```

### Hypothesis Test Output

```text
screenshots/hypothesis_test_output.png
```

### KPI Tree Preview

```text
screenshots/kpi_tree_preview.png
```

---

# Conclusion

The experiment indicates that the new onboarding experience delivers meaningful business improvements. The Treatment group achieved higher conversion rates, stronger engagement, and increased revenue while maintaining acceptable risk levels.

Based on the available evidence, the recommended business decision is to launch the new onboarding experience.
