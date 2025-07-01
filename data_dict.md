# Patent Litigation Data Dictionary

This document provides definitions for each field in the patent litigation dataset.

## Fields

| Field Name | Description | Data Type |
|------------|-------------|-----------|
| flag | Jurisdiction or database identifier | String |
| case_no | Unique case identifier in court dockets | String |
| filed_date | Date when the case was filed | Date (MM/DD/YY) |
| filing_year | Year when the case was filed | Integer |
| status | Current status of the litigation (e.g., Closed) | String |
| court | Court where the case was filed | String |
| plaintiff | Party that initiated the lawsuit | String (Multiple parties may be pipe-delimited) |
| parent_company | Parent company of the plaintiff, if applicable | String (Multiple entities may be pipe-delimited) |
| 3rd_funded | Indicates if the case was funded by a third party | Boolean/String |
| defendant | Party being sued in the lawsuit | String (Multiple parties may be pipe-delimited) |
| patents | Patent numbers involved in the lawsuit | String (Multiple patents may be pipe-delimited) |
| number_patents | Number of patents involved in the lawsuit | Integer |
| cause_of_action | Legal cause for the lawsuit | String |
| primary_cause_action | Primary legal cause for the lawsuit | String |
| entity_type | Type of entity filing the lawsuit | String (e.g., "Operating Company", "NPE (Individual)") |
| sme_annotation | Classification of company size | String |
| industry | Industry sector of the litigation | String |
| judge | Name of the presiding judge | String |
| closed_date | Date when the case was closed | Date (MM/DD/YY) |
| day | Number of days the case was active | Integer |
| label | Size classification of the case | String (e.g., "low", "medium", "large") |

## Notes

- Fields containing multiple values are typically pipe-delimited (e.g., "Entity1|Entity2|Entity3")
- NPE stands for Non-Practicing Entity
- SME stands for Small and Medium-sized Enterprise