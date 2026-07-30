# Analysis-on-INEC-dataset-

# Table of content 

* [Description](#description)
* [Business Introduction](#business-introduction)
* [Problem/Overview](#problem/Overview)
* [Procedure](#procedure)
* [Insights](#insights)
* [Recommendation](#recommendation)

## Description

This project analyzes electoral data from the INEC Election Dataset, covering 
1,000 polling units across four geopolitical zones in Nigeria — North-Central, 
North-West, South-South, and South-West. The dataset includes 936,985 
registered voters and 919,850 total votes cast. The analysis examines voter 
turnout, anomaly distribution, and party performance to surface patterns 
relevant to electoral integrity and civic planning.

## Business Introduction

INEC (Independent National Electoral Commission) oversees the conduct of 
elections across Nigeria's geopolitical zones. Ensuring the integrity of 
polling data — turnout accuracy, vote counts, and anomaly detection — is 
critical to maintaining public trust in electoral outcomes. This analysis 
was carried out as part of the NTTS Internship, Team Gurus | Data Analysis, 
using a dataset of 1,000 polling units collected in June 2026.

## Problem/Overview

While overall voter turnout across the dataset is high (98.03% nationally), 
this figure alone can mask underlying data integrity issues. Out of 1,000 
polling units, 12 (1.2%) recorded anomalies — including 2 cases of Over 
Voting (votes exceeding registered voters), 8 cases of Perfect Turnout, 
1 Suspicious Low turnout, and 1 Zero Turnout. South-West carries the 
highest anomaly burden with 6 flagged units, despite also recording the 
lowest average turnout (96.86%). This raises the question: which anomalies 
represent genuine irregularities that require audit, versus normal 
statistical variation?

## Insights

- **Turnout is high but uneven across zones.** National average is 98.03%. 
  South-South has the highest turnout (98.83%), while South-West has the 
  lowest (96.86%).
- **Anomalies are rare but targeted.** Only 1.2% of polling units show 
  anomalies, but South-West accounts for half of them (6 of 12).
- **Party A leads in every zone** without exception, followed consistently 
  by Party B. Party C trails with under 5% of votes in every zone.
- **A turnout-vs-registration gap exists nationally** — 17,135 votes 
  (1.83%) fewer than registered voters, with South-West showing the 
  largest absolute gap (5,076).
- **South-West is a pattern hotspot** — lowest turnout, highest anomaly 
  count, and largest registration gap all converge in this zone.

## Recommendation

- Audit the 2 Over Voting polling units in North-West and South-South 
  immediately — this is a direct data integrity violation.
- Investigate the 8 Perfect Turnout polling units for possible result 
  manipulation or recording errors before results are finalized.
- Apply an automatic turnout threshold flag (above 95%) in future 
  pipelines for secondary verification.
- Prioritize South-West for deeper investigation given its combination 
  of low turnout and high anomaly count.
- Expand the dataset to include North-East and South-East zones for a 
  complete six-zone national comparison.


