# Philippine Educational Attainment Analysis

A beginner-friendly data analysis project comparing college-level educational attainment across Philippine regions using data from the **Philippine Statistics Authority (PSA)**.

The project was developed in Google Colab and is presented as both a reproducible notebook and a code-free PDF report.

## Project Overview

National averages can hide important differences between regions. This project organizes the available PSA data into a consistent regional indicator and examines where college-level educational attainment is relatively high or low.

The analysis uses the percentage represented by college and post-baccalaureate categories:

```text
(College + Post-baccalaureate) / Total population extracted from the table x 100
```

## Research Questions

1. Which regions have the highest educational attainment?
2. Which regions have the lowest educational attainment?
3. How does educational attainment vary across regions?
4. Has educational attainment improved over time?
5. Which regions improved the most?

## Key Findings

| Measure | Result |
|---|---|
| Regions analyzed | 17 matched regions |
| Regional mean | 22.23% |
| Regional median | 20.97% |
| Highest value | NCR - 35.52% |
| Lowest value | BARMM - 13.57% |
| Highest-lowest gap | 21.95 percentage points |

### Five Highest Regions

1. NCR - 35.52%
2. CAR - 29.34%
3. Region IV-A - 26.73%
4. Region II - 23.85%
5. Region I - 23.47%

### Five Lowest Regions

1. BARMM - 13.57%
2. Region V - 17.93%
3. MIMAROPA - 18.25%
4. Region XII - 18.84%
5. Region VIII - 19.53%

> **Important limitation:** The available education data contain one comparable snapshot. Questions about improvement over time and the most improved regions cannot be answered responsibly without education data for additional years.

## Project Deliverables

| File | Description |
|---|---|
| [Analysis notebook](outputs/Philippine_Educational_Attainment_Analysis.ipynb) | Complete Google Colab workflow, Python analysis, charts, explanations, and research-question results |
| [PDF report](outputs/Philippine_Educational_Attainment_Analysis.pdf) | Easy-to-read, code-free report with visualizations and plain-language findings |

## Data Source

The project uses PSA Excel workbooks stored in Google Drive:

- `3_HGC and Literacy Statistical Table.xlsx`, worksheet `Table B`
- `Table 1a. CV_2018, 2021 and 2023p Average Annual Family Income, by Per Capita Income Decile Class and by Region, Province and HUCs.xlsx`, worksheet `Table 1a`

The first workbook provides the educational-attainment data. The second is retained as supplementary exploratory material from the original notebook and is **not** used to claim changes in educational attainment.

The source workbooks are not included in this repository. Obtain the appropriate files from the Philippine Statistics Authority and verify the table definitions before reproducing or publishing the analysis.

## Analysis Workflow

1. Connect Google Colab to Google Drive.
2. Locate and load the PSA Excel workbooks.
3. Extract regional education values from `Table B`.
4. Standardize regional names.
5. Inspect missing values, duplicates, ranges, and matching consistency.
6. Calculate descriptive statistics and regional rankings.
7. Visualize the distribution and regional differences.
8. Answer each research question within the limits of the data.
9. Document findings, recommendations, and future work.

## Visualizations

The project includes:

- a complete regional educational-attainment ranking;
- a distribution chart with the mean and median;
- a comparison of each region with the regional mean; and
- clearly labeled purpose, observation, and interpretation notes.

The PDF report is the quickest way to review the charts without reading code.

## Tools Used

- Python
- pandas
- Matplotlib
- Seaborn
- openpyxl
- Google Colab
- Google Drive

No machine-learning model is used. This is a descriptive data analysis project.

## How to Run the Notebook

1. Open the [analysis notebook](outputs/Philippine_Educational_Attainment_Analysis.ipynb) in Google Colab.
2. Add the required PSA workbooks to the root of your Google Drive `MyDrive` folder, or update the paths in the loading cells.
3. Run the notebook cells from top to bottom.
4. Approve the Google Drive connection when Colab requests access.
5. Review the data-quality output before interpreting the results.

The original loading workflow expects these paths:

```text
/content/drive/MyDrive/3_HGC and Literacy Statistical Table.xlsx
/content/drive/MyDrive/Table 1a. CV_2018, 2021 and 2023p Average Annual Family Income, by Per Capita Income Decile Class and by Region, Province and HUCs.xlsx
```

## Repository Structure

```text
.
|-- README.md
`-- outputs/
    |-- Philippine_Educational_Attainment_Analysis.ipynb
    `-- Philippine_Educational_Attainment_Analysis.pdf
```

## Limitations

- The education data represent one time period and cannot establish trends.
- The educational indicator depends on the population universe and categories defined in PSA `Table B`.
- Regional rankings describe differences but do not explain their causes.
- Changes in regional boundaries must be handled before comparing multiple years.
- The supplementary workbook filename contains `CV`; its fields should be checked against the source headers before being interpreted as monetary income.

## Future Work

- Add consistently defined PSA education data for multiple years.
- Compare percentage-point changes after harmonizing regional classifications.
- Explore differences by sex, age group, or urban-rural classification when supported by the source tables.
- Add demographic, access, and socioeconomic indicators for deeper descriptive analysis.
- Include official PSA download links, reference periods, and access dates in a complete data dictionary.

## Final Takeaway

The available data show meaningful regional differences in college-level educational attainment. The strongest next step is to obtain comparable education data across time before attempting to measure improvement.
