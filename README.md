# VoltRelay Energy

VoltRelay Energy is a data-analysis project focused on understanding and improving the performance of an electric battery swap network. The notebook analyzes swap operations, station health, rider behavior, and support issues to identify operational bottlenecks, clean anomalies, and quantify service quality.

## Project Goals

- Clean and normalize raw operational data from swap events and station telemetry
- Correct known data issues such as timezone drift and inconsistent city naming
- Remove duplicate retry records and test-station artifacts
- Analyze performance trends across time, stations, and user segments
- Measure service failures, wait times, and contribution margin to support operational decisions

## What’s Included

This repository contains:

- `VoltRelay.ipynb` — end-to-end notebook covering data cleaning, anomaly handling, and analytical investigations
- `README.md` — project overview and usage notes

## Data Domains Covered

The analysis uses several operational datasets, including:

- swap events
- rider profiles
- battery inventory and station metadata
- station hourly status telemetry
- support tickets
- city-level daily context
- fleet partner information

## Notebook Workflow

The notebook is organized into key phases:

1. Data Cleaning & Anomaly Handling
   - Firmware timezone correction for `v3.2.0`
   - Geography standardization for city names
   - Offline retry deduplication
   - Numeric coercion for telemetry fields
   - Outlier capping and removal of internal test stations

2. Core Analytical Investigations
   - Network performance over time
   - Service failures and customer experience
   - Queue wait times and failure-rate analysis by hour, station type, and vehicle class
   - Monthly revenue, completion trends, and contribution margin estimation

## Requirements

To run the notebook locally or in Google Colab, install:

- Python 3
- pandas
- numpy
- matplotlib
- seaborn

Example:

```bash
pip install pandas numpy matplotlib seaborn
```

## Running the Notebook

Open `VoltRelay.ipynb` in Jupyter Notebook, VS Code, or Google Colab. Upload or mount the required CSV datasets, then run the cells in order.

## Typical Use Cases

- Assess network reliability and station performance
- Identify operational pain points during peak hours or in specific cities
- Measure the effect of data-quality issues on business KPIs
- Support strategic decisions around maintenance, expansion, and service policy

## Notes

This project is designed for operational analytics and business intelligence use. Some later-stage calculations, such as contribution margin modeling, are simplified placeholders that can be refined with more detailed cost and battery degradation inputs.

## License

This project does not currently include a license file. If you plan to share or distribute it publicly, consider adding an appropriate open-source license.
