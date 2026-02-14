# URL Threat Detection & Security Analysis

Python-based security analysis tool that processes honeypot logs to identify and classify malicious URL-based attacks.

## Overview

This project analyzes over 720,000 URLs from honeypot log data to detect and classify various types of web-based attacks. The system uses optimized pattern matching and parallel processing to identify security threats including SQL injection, XSS, path traversal, and other common attack vectors.

## Features

- **Multi-Pattern Attack Detection**: Identifies 15+ attack types including:
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - Path Traversal
  - Command Injection
  - XML External Entity (XXE)
  - Server-Side Request Forgery (SSRF)
  - And more...

- **Performance Optimization**:
  - Parallel processing for large datasets
  - Vectorized operations for efficiency
  - Handles 720,000+ URLs efficiently

- **Comprehensive Analysis**:
  - Temporal attack patterns (time-based distribution)
  - Geographical source analysis
  - Attack severity classification
  - Top attacking IPs and countries

- **Automated Reporting**:
  - Executive summary generation
  - HTML security reports
  - Visualization exports (PNG)
  - JSON structured output

## Data

**Note:** The honeypot dataset (log_file_2.csv, 1.6GB) is not included in this repository due to size constraints. All analysis outputs and visualizations are embedded in the notebook.

The dataset contained:
- 720,281 URLs analyzed
- Honeypot traffic logs with timestamps, source IPs, and request data
- Geographic information for attacking sources
- User agent and protocol information

## Results

Analysis results are saved to the `Reports/` directory:
- `attack_distribution_[timestamp].png` - Attack type distribution chart
- `country_distribution_[timestamp].png` - Geographic attack sources
- `severity_distribution_[timestamp].png` - Attack severity analysis  
- `temporal_analysis_[timestamp].png` - Time-based attack patterns
- `security_report_[timestamp].html` - Comprehensive HTML report
- `executive_summary_[timestamp].txt` - Executive-level findings
- `summary_[timestamp].json` - Structured data output

## Key Findings

The analysis identified:
- Distribution of attack types across the dataset
- Peak attack times and temporal patterns
- Top attacking countries and IP addresses
- Security recommendations based on attack patterns

## Technologies Used

- **Python 3.x**
- **Pandas** - Data processing and analysis
- **NumPy** - Numerical operations
- **Matplotlib** - Visualization
- **Regex** - Pattern matching for threat detection
- **Parallel Processing** - Multi-threaded analysis for performance

## Security Patterns

The system detects attacks using carefully crafted regex patterns for:
- Database attack vectors (SQL injection, NoSQL injection)
- Script injection (XSS, template injection)
- File system attacks (path traversal, LFI/RFI)
- Infrastructure attacks (SSRF, XXE)
- Command execution attempts
- Authentication/authorization bypasses

## Performance

- **Dataset Size**: 720,281 URLs
- **Processing**: Multi-threaded with 4+ cores
- **Memory**: Optimized for large datasets
- **Output**: Comprehensive reports with visualizations

## Running the Analysis

**Note:** To run this analysis, you would need access to honeypot log data in the expected format (tab-separated CSV with columns: timestamp, source_ip, request_url, etc.).

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```

2. Prepare data:
   - Place honeypot logs as `log_file_2.csv` in the project directory
   - Ensure data format matches expected schema

3. Run the notebook:
   - Open `URL_Threat_Detection_Analysis.ipynb`
   - Run all cells (processing time varies with dataset size)

## Author

**Kyle Purves**
