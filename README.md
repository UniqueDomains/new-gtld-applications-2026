# New gTLD applications, 2026 round (1,766)

Every application ICANN published for the 2026 round of new generic top-level domains, as one CSV and one JSON file: 1,766 applications for 1,138 strings, with applicants, types, statuses and contention sets. Here the round is one file you can load, sort and join. Updated from time to time, not on a schedule. Unique.domains adds three columns: whether the string is a word in its catalog, and two coarse bands. The same applications are a page you can browse: [unique.domains/tld/applications](https://unique.domains/tld/applications).

**Announced on:** 2026-10-07
**Applications:** 1,766 · **Distinct strings:** 1,138 · **In contention:** 705 applications in 226 contention sets

Rows are sorted by string, then application id. The file does not rank applications.

## Files

- `applications.csv`, every application (1,766 rows)
- `applications.json`, the same rows as JSON
- `DATA_DICTIONARY.md`, the columns
- `LICENSE`, the terms of each column
- `CITATION.cff`, citation metadata

## Columns

| Column                | Description                                                                                                 |
| --------------------- | ----------------------------------------------------------------------------------------------------------- |
| string                | The applied-for string in ASCII (the A-label for an internationalized string), lowercase, without the dot.  |
| u_label               | The internationalized string as written (U-label). Empty for ASCII strings.                                 |
| applicant             | The applicant, in ICANN's wording.                                                                          |
| applicant_country     | An ISO code for the applicant's location. Empty when the location could not be placed.                      |
| application_id        | ICANN's application id.                                                                                     |
| type                  | The application type, in ICANN's wording.                                                                   |
| status                | The application status.                                                                                     |
| contention_set        | The contention set the application belongs to, when ICANN names one.                                        |
| announced_on          | The day ICANN first published the application, or the day it entered this dataset when ICANN gives none.    |
| in_word_corpus        | Whether the applied-for string is a word in the Unique.domains word catalog.                                |
| word_popularity_band  | How widely that word is used. Empty when the string is not a catalog word.                                  |
| comparable_sales_band | How often the same word has sold as a domain name under any extension, as a band. Never a count or a price. |

## Quick start

```python
import pandas as pd

df = pd.read_csv("https://raw.githubusercontent.com/UniqueDomains/new-gtld-applications-2026/main/applications.csv")
print(df.groupby("status").size())
```

## See also

- [Every application, with the bands, on Unique.domains](https://unique.domains/tld/applications?utm_source=github&utm_medium=referral&utm_campaign=repo_new_gtld_applications_2026&utm_content=related_tld_applications)
- [The TLDs Unique.domains tracks](https://unique.domains/tld?utm_source=github&utm_medium=referral&utm_campaign=repo_new_gtld_applications_2026&utm_content=related_tld_hub)

From code: the [Node.js SDK and CLI](https://github.com/UniqueDomains/nodejs) (`npm install @uniquedomains/sdk`), the [Python client](https://github.com/UniqueDomains/python) (`pip install uniquedomains`) and the [MCP server](https://github.com/UniqueDomains/mcp-server) for AI assistants, hosted at `https://mcp.unique.domains/mcp`.

## Contact

Questions or corrections: `kai@unique.domains`
