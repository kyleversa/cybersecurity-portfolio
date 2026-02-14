# Cyber Threat Sentiment Analysis

Advanced sentiment and bias analysis of cybersecurity threat intelligence reports using Natural Language Processing.

## Overview

This project analyzes cybersecurity threat intelligence reports to identify sentiment patterns and cognitive biases in threat reporting. The analysis provides insights into how threat actors, technologies, and incidents are portrayed across different reports.

## Features

- **Sentiment Analysis**: Evaluates positive, negative, and neutral sentiment across threat reports
- **Bias Detection**: Identifies four types of bias:
  - Geographical bias (regional focus)
  - Attribution bias (threat actor characterization)
  - Technical bias (technology-specific language)
  - Temporal bias (timeframe emphasis)
- **Automated Reporting**: Generates comprehensive analysis reports with visualizations
- **Multi-Document Analysis**: Processes multiple PDF reports simultaneously

## Data

The `Project 3 Files/` directory contains 20 cybersecurity threat intelligence reports in PDF format (35MB total). These reports cover various threat actors, attack campaigns, and security incidents.

**Note:** This project is fully runnable - all required data files are included in the repository.

## Results

Analysis results are saved to the `Output/` directory:
- `sentiment_bias_analysis_results.csv` - Detailed analysis data
- `sentiment_bias_analysis_visualizations.png` - 7-panel visualization chart
- `analysis_summary.txt` - Statistical summary
- `bias_impact_summary.txt` - Key findings and bias impact analysis

## Running the Analysis

1. Ensure all dependencies are installed:
   ```bash
   pip install pandas numpy matplotlib nltk pypdf2
   ```

2. Download NLTK data (first time only):
   ```python
   import nltk
   nltk.download('vader_lexicon')
   nltk.download('punkt')
   ```

3. Run the notebook:
   - Open `Cyber_Threat_Sentiment_Analysis.ipynb`
   - Run all cells (processing takes approximately 4 minutes)

## Key Findings

The analysis reveals:
- Sentiment patterns across different threat types
- Common biases in threat intelligence reporting
- Geographical focus areas in threat reporting
- Attribution language and characterization patterns

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NLTK** - Natural language processing and sentiment analysis
- **Matplotlib** - Data visualization
- **PyPDF2** - PDF text extraction

## Visualizations

The project generates a comprehensive 7-panel visualization showing:
1. Sentiment distribution across reports
2. Bias type prevalence
3. Geographical focus analysis
4. Attribution patterns
5. Technical bias indicators
6. Temporal bias trends
7. Overall bias impact summary

## Author

**Kyle Purves**
