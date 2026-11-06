# Stack Overflow Developer Survey

A Pandas analysis of work experience, remote work, programming languages and compensation in a Stack Overflow survey extract.

[Open the notebook](Stack_Overflow_Analysis_Project.ipynb)

## Questions I explored

How much work experience do respondents report? How many work remotely or use Python? How does compensation vary by country, and which industries appear most often among higher-paid remote respondents?

I used filtering, missing-value checks, grouped aggregations and percentiles. Questions with multiple answers are stored as semicolon-separated text.

## Results from the saved run

| Measure | Result |
| --- | ---: |
| Unique respondents | 49,191 |
| Mean reported work experience | 13.4 years |
| Median reported work experience | 10 years |
| Respondents marked as remote | 10,931 |
| Python users as a share of all respondents | 37.54% |

Software Development has the largest count in the higher-paid remote segment, with **1,186 respondents**. That segment uses the compensation threshold at the 75th percentile of all non-missing compensation responses, then filters for remote work.

## Reading the results

The Python percentage uses all unique respondents as its denominator; missing language answers count as no Python mention. The work-experience and compensation calculations skip missing numeric values.

The notebook's complete-response check returns zero. Survey branching and optional questions mean this should not be read as a claim that every response is unusable.

Reported compensation includes extreme values. The top-five compensation table is exploratory and should not be used as evidence that a particular qualification causes higher earnings. This is a self-selected survey sample, not a representative salary benchmark.

## Run it

Download the matching public survey CSV and schema from [Stack Overflow's survey data](https://survey.stackoverflow.co/) and place these files beside the notebook:

- `survey_results_public.csv`
- `survey_results_schema.csv`

The original CSV files are not included, and the notebook does not record their release year. Match the schema and row count before comparing a new run with the saved results.

```bash
pip install -r requirements.txt
jupyter notebook Stack_Overflow_Analysis_Project.ipynb
```

The notebook also opens in Google Colab after uploading the two CSV files.

Educational project completed during GoIT Data Analytics training.
