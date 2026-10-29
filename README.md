# Grant Screening & Ranking for NCDOT
A Python-based pipeline to screen, evaluate, and rank federal grant opportunities based on eligibility, funding criteria, and alignment with the North Carolina Department of Transportation (NCDOT)'s strategic priorities.

## Problem Statement
Every week, hundreds of new federal funding opportunities are posted on Grants.gov. Somewhere in that pile is money that North Carolina is eligible for and needs for broadband, disaster recovery, public health, workforce training, and more. But nobody has time to read it all. It is often the case that opportunities are discovered late or missed, and the money goes to states that found the posting first.

For the NCDOT, the challenge is not only finding eligible grants but also determining which opportunities best align with its strategic priorities and funding needs.

## Project Overview
This project uses Python to analyze 1,600+ federal grant opportunities and identify potential funding sources for the NCDOT.

I designed a four-stage pipeline including eligibility filtering, category-based scoring, weighted evaluation, and final ranking to generate a prioritized list of five recommended grants.

## Methodology
### 1. Eligibility Filtering
I implemented hard eligibility filters to exclude grants that:
- Were classified as forecasted opportunities.
- Had already passed their application deadlines.
- Did not meet NCDOT's applicant eligibility requirements.

### 2. Category-Based Scoring
I developed a scoring framework based on five criteria:
| Criterion | Description |
|---|---|
| Funding Category | Prioritizes transportation and infrastructure-related grants. |
| Grant Type | Assigns points based on grant type. |
| Average Award Amount | Uses a nonlinear scoring function to evaluate funding amounts. |
| Expected Number of Awards | Considers the anticipated number of recipients. |
| Application Deadline | Prioritizes grants with approximately one month remaining. |

### 3. Weight Evaluation & Final Ranking
I combined weighted scores across the criteria to calculate each grant's final score.

Grants were then ranked by overall scores to identify the most promising opportunities for NCDOT.

## Result
### Top 5 Recommended Grants
1. Development of Fiscal Year 2027 Commercial Vehicle Safety Plans to Support National Safety Goals
2. FY26 Bus Safety, Accessibility and Innovation Notice of Funding Opportunity
3. RESTORE Act Centers of Excellence Research Grants Program
4. RESTORE Act Direct Component – Non-Construction Activities
5. RESTORE Act Direct Component – Construction and Real Property Acquisition Activities

## Tools
- **Python**: Data processing and scoring logic
- **pandas**: Data cleaning, filtering, and manipulation
- **NumPy**: Scoring functions

## Key Takeaways
Through this project, I explored how data analytics can support real-world decision-making.

The project also strengthened my experience with data preprocessing, rule-based filtering, and quantitative scoring.

## Project Context
*The rankings reflect my own assumptions and analytical methodology, rather than official NCDOT funding decisions.*
