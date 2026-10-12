# New gTLD applications, 2026 round (1,614)

Every application ICANN published for the 2026 round of new generic top-level domains, in CSV and JSON, with three coarse bands from Unique Domains. Updated when ICANN publishes status changes.

**Announced on:** 2026-10-07
**Last updated:** 2026-10-12
**Applications:** 1,614 · **Distinct strings:** 986 · **In contention:** 891 applications in 263 contention sets

Source: ICANN, New gTLD Program application listings. The applied-for strings, applicants, application ids, types, statuses and contention sets are republished as ICANN publishes them; the applicant's country is an ISO code derived from ICANN's listing, and the date is ICANN's, or the day of the import when ICANN's file carries none. The three band columns are Unique Domains data.

Rows are sorted by string, then application id. The file does not rank applications.

## Files

- `applications.csv`, every application (1,614 rows)
- `applications.json`, the same rows as JSON
- `DATA_DICTIONARY.md`, the columns
- `LICENSE`, terms for the ICANN columns and the Unique Domains columns
- `CITATION.cff`, citation metadata

## Columns

| Column                | Source         | Description                                                                                                        |
| --------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------ |
| string                | ICANN          | The applied-for string in ASCII (the A-label for an internationalized string), lowercase, without the dot.         |
| u_label               | ICANN          | The internationalized string as written (U-label). Empty for ASCII strings.                                        |
| applicant             | ICANN          | The applicant as ICANN publishes it.                                                                               |
| applicant_country     | ICANN          | An ISO code derived from the applicant's location in ICANN's listing. Empty when the location could not be placed. |
| application_id        | ICANN          | ICANN's application id.                                                                                            |
| type                  | ICANN          | The application type as ICANN publishes it.                                                                        |
| status                | ICANN          | The application status at the last update of this dataset.                                                         |
| contention_set        | ICANN          | The contention set the application belongs to, when ICANN names one.                                               |
| announced_on          | ICANN          | The day ICANN first published the application, or the day of the import when ICANN's file carries no date.         |
| in_word_corpus        | Unique Domains | Whether the applied-for string is a word in the Unique Domains word catalog.                                       |
| word_popularity_band  | Unique Domains | How widely that word is used. Empty when the string is not a catalog word.                                         |
| comparable_sales_band | Unique Domains | How often the same word has sold as a domain name under any extension, as a band. Never a count or a price.        |

## Quick start

```python
import pandas as pd

df = pd.read_csv("https://raw.githubusercontent.com/UniqueDomains/new-gtld-applications-2026/main/applications.csv")
print(df.groupby("status").size())
```

## See also

- [Every application, with the bands, on Unique Domains](https://unique.domains/tld/applications?utm_source=github&utm_medium=referral&utm_campaign=repo_new_gtld_applications_2026&utm_content=related_tld_applications)
- [The TLDs Unique Domains tracks](https://unique.domains/tld?utm_source=github&utm_medium=referral&utm_campaign=repo_new_gtld_applications_2026&utm_content=related_tld_hub)

## Contact

Questions or corrections: `kai@unique.domains`
