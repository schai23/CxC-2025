# TouchBistro Customer Spend Insights Report

## Problem Statement
This analysis addresses Problem #2 from the TouchBistro datathon: examining how order type impacts average bill size and tip amount.

## Methodology

### Data Preparation
- Merged venue and bill datasets using the venue_xref_id field
- Filtered out invalid entries (bills with zero or negative values)
- Calculated tip percentage as (payment_total_tip / bill_total_billed) * 100
- Grouped data by order_take_out_type_label to analyze spending patterns

### Analysis Approach
1. **Descriptive Statistics**: Calculated mean, median, and count for bill size, tip amount, and tip percentage by order type
2. **Visualization**: Created bar charts to compare metrics across different order types
3. **Simple Modeling**: Used linear regression to quantify the relationship between order type, bill size, and tip amount

## Key Findings

1. **Bill Size Variation by Order Type**
   - Delivery orders have the highest average bill at $48.12
   - Bar tabs show the second highest average at $41.50
   - Online orders average $40.30 per bill
   - Dine-in orders average $38.12 per bill
   - Takeout orders have the lowest average bill at $33.83, which is 30% smaller than delivery orders

2. **Tipping Behavior Analysis**
   - Bar tab orders receive the highest average tip amount at $4.85
   - Dine-in orders receive the second highest average tip at $4.16
   - Takeout orders average $1.25 in tips
   - Delivery orders average $1.21 in tips
   - Online orders receive the lowest average tip at only $0.48

3. **Order Type Impact on Revenue**
   - Despite having a mid-range average bill size, dine-in orders dominate in terms of volume with over 7.3 million transactions
   - Dine-in orders generate the highest total tip revenue at approximately $30.4 million
   - Takeout orders represent the second highest volume with 914,417 transactions
   - Bar tabs, while fewer in number (213,773), generate significant tip revenue at approximately $1.04 million
   - Online orders show the lowest tipping rate, suggesting potential for improvement in digital tipping prompts

## Business Implications

These insights can help TouchBistro restaurant clients:

- **Optimize Service Focus**: Since bar tabs and dine-in orders generate the highest tips, restaurants might want to prioritize service excellence in these areas
- **Improve Digital Tipping**: The significantly lower tips for online orders ($0.48 average) indicate an opportunity to improve digital tipping interfaces
- **Balance Order Types**: While delivery orders have the highest average bill ($48.12), they represent a smaller portion of orders and generate lower tips than dine-in service
- **Staff Allocation**: With dine-in representing the vast majority of orders, proper staffing during peak dine-in periods is crucial
- **Takeout Strategy**: The high volume of takeout orders (914,417) with relatively low average bills ($33.83) suggests an opportunity for upselling or combo promotions

## Limitations and Future Work

This analysis was conducted with limited time and could be extended in several ways:
- Incorporate time-based analysis (day of week, time of day patterns)
- Segment by restaurant concept to identify industry-specific patterns
- Include geographic analysis to detect regional differences in tipping culture
- Develop predictive models to forecast revenue by order type
- Investigate why online orders have such low tip rates compared to other order types

## Conclusion

Understanding the relationship between order type, bill size, and tipping behavior provides valuable insights for restaurant operations. This analysis demonstrates clear differences in customer spending patterns across different order types, offering actionable intelligence for TouchBistro clients. The most significant finding is the large disparity in tipping behavior between in-person experiences (bar tabs, dine-in) and digital ordering methods (online orders), suggesting opportunities for improvement in digital payment interfaces.