# Prepare Phase — Data Source Documentation

## Dataset Name  
Divvy / Cyclistic Bike-Share Trip Data

## Data Provider  
Motivate International Inc. (Divvy Bikes)

## Description  
This dataset contains historical trip-level records from Cyclistic, a bike-share program operating in Chicago. Each record represents a single bike trip and includes ride duration, start and end station details, and rider classification (member or casual).

## Time Period Covered  
January 2019 – December 2019

## File Format  
CSV (.csv)

## Data Files Used  
- Divvy_Trips_2019_Q1.csv  
- Divvy_Trips_2019_Q2.csv  
- Divvy_Trips_2019_Q3.csv  
- Divvy_Trips_2019_Q4.csv  

## Data Organization  
The data was provided in quarterly CSV files. Each file contains structured trip-level records with consistent column formats, allowing for consolidation into a full-year dataset.

---

## ROCCC Data Quality Assessment

The dataset was evaluated using the ROCCC framework to assess its credibility and suitability for analysis.

### Reliable
✅ Generated directly by Divvy’s operational bike-share system and collected automatically through system infrastructure.

### Original
✅ Sourced directly from the primary provider (Motivate International Inc.) without third-party modification.

### Comprehensive
⚠️ Includes detailed trip-level data sufficient for behavioral analysis. However, personal and financial information is excluded due to privacy constraints.

### Current
⚠️ Covers the 2019 calendar year. While historical, it is appropriate for identifying usage trends and rider behavior patterns.

### Cited
✅ Publicly available dataset with documented source and licensing terms.

---

## Data License & Privacy

### License Information
The Divvy bike-share dataset is publicly available and distributed under a public data license provided by Motivate International Inc.

### Usage Rights
- Data is available for public, educational, and non-commercial use.
- Analysis and visualization are permitted with proper attribution.

### Privacy Considerations
- Personally identifiable information (PII) is not included.
- No rider names, contact details, or payment information are provided.
- The dataset complies with privacy and data protection standards.

### Attribution
Source: Divvy Bike Share Trip Data  
Provider: Motivate International Inc.

---

## Data Storage Strategy  

- **Local Project:** Raw CSV files stored in a dedicated raw data directory for full-scale analysis using Excel and Power Query.
- **GitHub Portfolio Version:** Raw files excluded due to size limitations. Only cleaned, aggregated, and summarized outputs are included.