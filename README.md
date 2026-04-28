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


## Instructions for reproducing results
# To run the exploratory data analysis script:

1. Download SOTU_data_final.csv from the DATA folder and project_1_eda.py from the SCRIPTS folder to a known location on your computer.
2. Run project_1_eda.py. Ensure that the file directory in your IDE is set to the location of SOTU_data_final.csv.
3. Plots will be generated showing crisis vs. non-crisis speech counts, average word count by crisis flag, crisis years by type, and frequency of crises mentioned in SOTU addresses.

# To run the sentiment analysis script:

1. Download SOTU_data_final.csv from the DATA folder and sentiment_model.py from the SCRIPTS folder to a known location on your computer.
2. Run sentiment_model.py. Ensure that the file directory in your IDE is set to the location of SOTU_data_final.csv.
3. A sentiment_analysis_results.csv file will be generated in the OUTPUTS folder containing sentiment scores for each speech.

# To run the statistical analysis script:

1. Download sentiment_analysis_results.csv from the OUTPUTS folder and stat_analysis.py from the SCRIPTS folder.
2. Run stat_analysis.py. Ensure that the file directory in your IDE is set to the location of sentiment_analysis_results.csv.
3. Six visualizations and a summary report will be generated in the OUTPUTS folder.

# Once all scripts have been run, these are the outputs you should be able to obtain:

1. sentiment_analysis_results.csv — sentiment scores for all speeches
2. analysis_summary.txt — statistical test results summary
3. boxplot_positive_sentiment.png — box plot comparing crisis vs. non-crisis sentiment
4. histogram_positive_sentiment.png — histogram of sentiment distribution
5. pie_crisis_sentiment.png — pie chart for crisis speeches
6. pie_noncrisis_sentiment.png — pie chart for non-crisis speeches
7. boxplot_ratio.png — box plot of positive/negative ratios
8. timeseries_sentiment.png — time series showing sentiment trends over time
