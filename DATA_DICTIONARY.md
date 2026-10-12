# Data Dictionary

This dictionary describes the columns of `applications.csv` and `applications.json`.

| Column                | Type                             | Source         | Description                                                                                                        |
| --------------------- | -------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------ |
| string                | string                           | ICANN          | The applied-for string in ASCII (the A-label for an internationalized string), lowercase, without the dot.         |
| u_label               | string or null                   | ICANN          | The internationalized string as written (U-label). Empty for ASCII strings.                                        |
| applicant             | string                           | ICANN          | The applicant as ICANN publishes it.                                                                               |
| applicant_country     | ISO 3166-1 alpha-2 or null       | ICANN          | An ISO code derived from the applicant's location in ICANN's listing. Empty when the location could not be placed. |
| application_id        | string                           | ICANN          | ICANN's application id.                                                                                            |
| type                  | string or null                   | ICANN          | The application type as ICANN publishes it.                                                                        |
| status                | string or null                   | ICANN          | The application status at the last update of this dataset.                                                         |
| contention_set        | string or null                   | ICANN          | The contention set the application belongs to, when ICANN names one.                                               |
| announced_on          | date (YYYY-MM-DD) or null        | ICANN          | The day ICANN first published the application, or the day of the import when ICANN's file carries no date.         |
| in_word_corpus        | boolean or null                  | Unique Domains | Whether the applied-for string is a word in the Unique Domains word catalog.                                       |
| word_popularity_band  | low, medium, high, or null       | Unique Domains | How widely that word is used. Empty when the string is not a catalog word.                                         |
| comparable_sales_band | none, low, medium, high, or null | Unique Domains | How often the same word has sold as a domain name under any extension, as a band. Never a count or a price.        |

In `applications.csv`, a value that starts with `=`, `+`, `-`, `@`, a tab or a carriage return carries a leading `'`, so a spreadsheet reads it as text rather than a formula. `applications.json` keeps every value as it is.
