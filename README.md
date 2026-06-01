# Acculturation Strategies, Acculturation Stress, and Work Engagement in Venezuelan Migrants in South America

## Overview

This dataset supports an exploratory analysis examining the relationship between acculturation strategies, acculturation stress, and work engagement among Venezuelan migrants living and working in five South American countries (Argentina, Chile, Colombia, Ecuador, and Peru).

The central research question was whether acculturation strategies — as defined by Berry's (1997) theoretical model — predict work engagement. A secondary question explored the role of occupational continuity (working in the same professional field as in Venezuela) as a predictor of engagement and a potential moderator of the stress–engagement relationship.

A narrative visualization of the full analysis is available at: `[portfolio URL]`

---

## Author

**Gabriel Ortiz Francisco**  
Psychometrics & Data Analysis Specialist  
Universidad Técnica Particular de Loja (UTPL), Ecuador

---

## Data Collection

- **Period:** 2017–2018
- **Method:** Online self-report survey (Google Forms)
- **Sampling:** Non-probabilistic convenience sample
- **Eligibility criteria:** Venezuelan nationals, currently residing and employed in one of the five target countries

---

## Sample

| Country | n | % |
|---|---|---|
| Chile | 65 | 36.9% |
| Ecuador | 58 | 33.0% |
| Argentina | 22 | 12.5% |
| Colombia | 21 | 11.9% |
| Peru | 10 | 5.7% |
| **Total** | **176** | **100%** |

- **Mean age:** 32.4 years (SD = 9.1)
- **Gender:** 55% women, 45% men
- **Working without formal contract:** 42%
- **Working in a different occupational field than in Venezuela:** 55%

---

## Instruments

### 1. Acculturation Strategies Scale
Based on Berry's (1997) bidimensional model. Four items, one per strategy, rated on a 0–5 scale:

| Variable | Description |
|---|---|
| `assimilation` | Preference for full adoption of host culture, abandoning culture of origin |
| `integration` | Preference for maintaining culture of origin while adopting host culture |
| `separation` | Preference for maintaining culture of origin without adopting host culture |
| `marginalization` | Indifference toward both cultures |

**Reference:** Berry, J. W. (1997). Immigration, acculturation, and adaptation. *Applied Psychology: An International Review, 46*(1), 5–34.

---

### 2. Acculturation Stress Scale for Latin American Immigrants
Developed by Ruiz et al. (2011). 24 items rated on a 0–5 Likert scale (0 = *this has not been a problem* to 5 = *this has affected me greatly*), organized into six subdimensions:

| Variable | Subdimension | Items |
|---|---|---|
| `stress_discrimination` | Perceived discrimination | Items related to contempt and exclusion by host-country nationals |
| `stress_outgroup` | Differences with outgroup | Items related to cultural and linguistic differences |
| `stress_legal` | Citizenship and legal status | Items related to irregular migration status |
| `stress_ingroup` | Relations with other immigrants | Items related to conflict with other Venezuelan migrants |
| `stress_distance` | Distance from origin | Items related to homesickness and lost contact |
| `stress_family` | Family rupture | Items related to family separation due to migration |
| `stress_total` | Total acculturation stress | Mean of all 24 items |

---

### 3. Utrecht Work Engagement Scale (UWES-9)
9 items rated on a 0–6 frequency scale (0 = Never, 6 = Always/Every day), organized into three dimensions:

| Variable | Dimension | Items |
|---|---|---|
| `vigor` | Vigor | Items 1, 2, 3 — energy, mental resilience, persistence |
| `dedication` | Dedication | Items 4, 5, 6 — enthusiasm, inspiration, pride |
| `absorption` | Absorption | Items 7, 8, 9 — immersion, concentration, flow |
| `engagement_total` | Total Work Engagement | Mean of all 9 items |

**Reference:** Schaufeli, W. B., Bakker, A. B., & Salanova, M. (2006). The measurement of work engagement with a short questionnaire: A cross-national study. *Educational and Psychological Measurement, 66*(4), 701–716. Psychometric properties validated in Latin American samples: Mexico (Hernández et al., 2016), Ecuador (Portalanza et al., 2017), and Puerto Rico (Rodríguez et al., 2014).

---

## Variables in the Dataset

### Demographic and labor variables

| Column | Variable | Values |
|---|---|---|
| `country` | Host country | 1 = Argentina, 2 = Chile, 3 = Colombia, 4 = Ecuador, 5 = Peru |
| `age` | Age in years | Continuous |
| `gender` | Gender | 1 = Woman, 2 = Man |
| `marital_status` | Marital status | 1 = Single, 2 = Partnered, 3 = Married, 4 = Divorced |
| `education` | Highest education level | 1 = Primary, 2 = Secondary, 3 = Technical, 4 = University, 5 = Postgraduate |
| `residence_time` | Time living in host country | 1 = < 1 year, 2 = 1–2 years, 3 = 2–3 years, 4 = > 3 years |
| `previous_migration` | Lived in another foreign country before | 1 = Yes, 2 = No |
| `same_sector` | Currently working in same occupational field as in Venezuela | 1 = Yes, 2 = No |
| `tenure` | Tenure in current job | 1–4 ordinal scale |
| `job_match` | Perceived fit between current role and qualifications | Ordinal |
| `employment_status` | Employment status | 1–4 categories |
| `contract_type` | Type of work contract | 1 = Permanent, 2 = Temporary, 3 = Project-based, 4 = No contract, 5 = Other |

### Scale items and computed scores
Item-level responses for all three instruments are included, along with pre-computed subdimension and total scores as described in the instruments section above.

> **Note:** See Sheet 2 of the dataset file for a complete variable codebook, including item wording and response labels.

---

## Key Findings

1. **Acculturation strategies did not predict work engagement.** Integration — the dominant strategy (76% of sample) — showed a near-zero correlation with engagement (r = .026, p = .737). The only significant correlation was with Assimilation (r = .177, p = .019).

2. **Occupational continuity was the strongest predictor of engagement.** Migrants working in the same field as in Venezuela reported significantly higher engagement than those who changed fields (M = 4.34 vs. 3.41, p < .001, d ≈ 0.68). This effect remained the only significant predictor in a multiple regression model controlling for all acculturation variables, stress, age, education, and time of residence (β = −.338, p = .004).

3. **Occupational continuity did not moderate the stress–engagement relationship.** The interaction term (stress × same field) was negligible (β = .045, p = .83, ΔR² ≈ 0), indicating that field continuity and stress operate as independent predictors of engagement.

4. **Separation strategy predicted higher acculturation stress** (r = .211, p = .005), particularly across perceived discrimination, outgroup differences, ingroup conflict, and distance from origin subdimensions.

---

## Analysis

All analyses were conducted in Python using pandas, scipy, and statsmodels. Scripts are available in the accompanying repository.

Statistical methods used:
- Pearson correlations
- Independent samples t-tests
- One-way ANOVA
- Multiple linear regression with standardized coefficients
- Moderation analysis (interaction term method)
- Chi-square test of independence

---

## Limitations

- Non-probabilistic convenience sample (N = 176)
- Cross-sectional design; causal inference is not supported
- Data collected 2017–2018; the Venezuelan migration context has evolved substantially since then
- Small subgroup sizes for some countries (Peru n = 10, Colombia n = 21) limit country-level comparisons
- Results should be interpreted as exploratory

---

## License

This dataset is shared under a **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share and adapt the material for any purpose, provided appropriate credit is given.

---

## Citation

If you use this dataset, please cite it as:

> Ortiz Francisco, G. (2025). *Acculturation strategies, acculturation stress, and work engagement in Venezuelan migrants in South America* [Dataset]. OSF. https://doi.org/[DOI]

---

## Contact

For questions about the dataset or the analysis, please open an issue in the accompanying repository or reach out via LinkedIn.
