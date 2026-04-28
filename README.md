# DS4002 Final Project CS3 Read Me

## Software and Platform 

**Software:** Python 3.8 or higher

**Required Packages:**
- `transformers` (>=4.30.0) - For sentiment analysis model
- `torch` (>=2.0.0) - Backend for transformers
- `pandas` (>=1.3.0) - Data manipulation and analysis
- `numpy` (>=1.21.0) - Numerical computing
- `matplotlib` (>=3.5.0) - Data visualization
- `seaborn` (>=0.12.0) - Statistical data visualization
- `scipy` (>=1.7.0) - Statistical tests (two-sample t-test)

**Installation:**
Can be installed with 
pip install -r requirements.txt

## A Map of Documentation 

**DATA**
- SOTU_data_final.csv - Dataset containing all SOTU speeches (1850-2025); Columns: President, Year, Title, Text, is_crisis, crisis_name
- state_of_the_union_texts.csv - Raw original dataset

**SCRIPTS**
- sentiment_model.py - Main script: Analyzes sentiment of all speeches
- stat_analysis.py - Secondary script: Performs statistical analysis on results and creates visualizations
- project_1_eda.py - Initial exploratory data analysis

**OUTPUTS**
- sentiment_analysis_results.csv - Results from sentiment analysis 
- analysis_summary.txt - Statistical test results summary 
- boxplot_positive_sentiment.png - Box plot comparing crisis vs non-crisis 
- histogram_positive_sentiment.png - Histogram of sentiment distribution 
- pie_crisis_sentiment.png - Pie chart for crisis speeches 
- pie_noncrisis_sentiment.png - Pie chart for non-crisis speeches 
- boxplot_ratio.png - Box plot of positive/negative ratios 
- timeseries_sentiment.png - Time series showing sentiment trends


# Instructions for reproducing results

## Step 1: Set Up Environment

1. Clone or download this repository to your local machine
2. Open a terminal or command prompt and navigate to the project directory:
```bash
   cd DS4002.CS3_SOTU_Case_Study
```
3. Install required Python packages:
```bash
   pip install -r requirements.txt
```
## Step 2: Verify Data Files

1. Ensure the `DATA` folder contains `SOTU_data_final.csv`
2. This file should contain 231 rows (one per speech) with the following columns:
   - President: Name of the president
   - Year: Year of the speech (1850-2025)
   - Title: Full title of the speech
   - Text: Complete speech text (stored as a list of sentences)
   - is_crisis: Binary indicator (1 = crisis, 0 = non-crisis)
   - crisis_name: Name of the crisis (if applicable)

**Optional**: If you disagree with any of the crisis classifications in the dataset, you may update the is_crisis or crisis_name columns in SOTU_data_final.csv before running the scripts. Rerunning the analysis with your own classifications is a great way to explore how definitional choices affect results.

## Step 3: To run the exploratory data analysis script:

1. Download SOTU_data_final.csv from the DATA folder and project_1_eda.py from the SCRIPTS folder to a known location on your computer.
2. Run project_1_eda.py. Ensure that the file directory in your IDE is set to the location of SOTU_data_final.csv.
3. Plots will be generated showing crisis vs. non-crisis speech counts, average word count by crisis flag, crisis years by type, and frequency of crises mentioned in SOTU addresses.

## Step 4: To run the sentiment analysis script:

1. Download SOTU_data_final.csv from the DATA folder and sentiment_model.py from the SCRIPTS folder to a known location on your computer.
2. Run sentiment_model.py. Ensure that the file directory in your IDE is set to the location of SOTU_data_final.csv.
3. A sentiment_analysis_results.csv file will be generated in the OUTPUTS folder containing sentiment scores for each speech.
4. Verify the output file was created in the OUTPUTS folder

## Step 5: To run the statistical analysis script:

1. Download sentiment_analysis_results.csv from the OUTPUTS folder and stat_analysis.py from the SCRIPTS folder.
2. Run stat_analysis.py. Ensure that the file directory in your IDE is set to the location of sentiment_analysis_results.csv.
3. Six visualizations and a summary report will be generated in the OUTPUTS folder.

## Step 6: Once all scripts have been run, these are the outputs you should be able to obtain:

1. crisis_vs_noncrisis_count.png — bar chart of SOTU speeches by crisis status
2. avg_wordcount_by_crisis.png — average word count by crisis flag
3. crisis_years_by_type.png — bar chart of crisis years by type (military vs. economic)
4. crisis_frequency_chart.png — frequency of crises mentioned in SOTU addresses
5. sentiment_analysis_results.csv — sentiment scores for all speeches
6. analysis_summary.txt — statistical test results summary
7. boxplot_positive_sentiment.png — box plot comparing crisis vs. non-crisis sentiment
8. histogram_positive_sentiment.png — histogram of sentiment distribution
9. pie_crisis_sentiment.png — pie chart for crisis speeches
10. pie_noncrisis_sentiment.png — pie chart for non-crisis speeches
11. boxplot_ratio.png — box plot of positive/negative ratios
12. timeseries_sentiment.png — time series showing sentiment trends over time
