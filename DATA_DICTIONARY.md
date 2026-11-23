# Data Dictionary

This dictionary describes the columns of `applications.csv` and `applications.json`.

| Column                | Type                             | Description                                                                                                 |
| --------------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| string                | string                           | The applied-for string in ASCII (the A-label for an internationalized string), lowercase, without the dot.  |
| u_label               | string or null                   | The internationalized string as written (U-label). Empty for ASCII strings.                                 |
| applicant             | string                           | The applicant, in ICANN's wording.                                                                          |
| applicant_country     | ISO 3166-1 alpha-2 or null       | An ISO code for the applicant's location. Empty when the location could not be placed.                      |
| application_id        | string                           | ICANN's application id.                                                                                     |
| type                  | string or null                   | The application type, in ICANN's wording.                                                                   |
| status                | string or null                   | The application status.                                                                                     |
| contention_set        | string or null                   | The contention set the application belongs to, when ICANN names one.                                        |
| announced_on          | date (YYYY-MM-DD) or null        | The day ICANN first published the application, or the day it entered this dataset when ICANN gives none.    |
| in_word_corpus        | boolean or null                  | Whether the applied-for string is a word in the Unique.domains word catalog.                                |
| word_popularity_band  | low, medium, high, or null       | How widely that word is used. Empty when the string is not a catalog word.                                  |
| comparable_sales_band | none, low, medium, high, or null | How often the same word has sold as a domain name under any extension, as a band. Never a count or a price. |

In `applications.csv`, a value that starts with `=`, `+`, `-`, `@`, a tab or a carriage return carries a leading `'`, so a spreadsheet reads it as text rather than a formula. `applications.json` keeps every value as it is.
