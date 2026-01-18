# Data Dictionary

## Overview
This document describes the variables and data structure used in the asylum seekers research project.

## Variables

### Demographic Variables
| Variable Name | Type | Description | Values/Range |
|--------------|------|-------------|--------------|
| age | Numeric | Age of the asylum seeker | 18-99 years |
| country_of_origin | Categorical | Country from which the asylum seeker fled | Various countries |
| education_level | Categorical | Highest level of education attained | Primary, Secondary, Tertiary, None |
| marital_status | Categorical | Marital status | Single, Married, Divorced, Widowed |

### Asylum Process Variables
| Variable Name | Type | Description | Values/Range |
|--------------|------|-------------|--------------|
| application_date | Date | Date asylum application was submitted | Date format |
| decision_date | Date | Date asylum decision was made | Date format |
| asylum_status | Categorical | Outcome of asylum application | Granted, Denied, Pending |
| processing_time | Numeric | Days between application and decision | 0+ days |

### Impact Variables
| Variable Name | Type | Description | Values/Range |
|--------------|------|-------------|--------------|
| mental_health_score | Numeric | Mental health assessment score | 0-100 |
| employment_status | Categorical | Current employment status | Employed, Unemployed, Student |
| housing_stability | Categorical | Housing situation stability | Stable, Temporary, Unstable |
| social_support | Numeric | Level of social support | 1-10 scale |

### Outcome Variables
| Variable Name | Type | Description | Values/Range |
|--------------|------|-------------|--------------|
| integration_score | Numeric | Overall integration score | 0-100 |
| economic_status | Categorical | Economic self-sufficiency | Dependent, Partially Independent, Independent |

## Data Collection
- **Collection Period**: [Specify dates]
- **Sample Size**: [Specify N]
- **Data Source**: [Specify source]

## Missing Data
- Missing values are coded as: `NaN` or `null`
- Missing data patterns: [Describe any systematic missing data]

## Notes
- All personal identifying information has been removed to protect participant privacy
- Data has been anonymized according to ethical research standards
- [Add any other relevant notes about the data]

## Version History
- v1.0 - Initial data dictionary (January 2026)
