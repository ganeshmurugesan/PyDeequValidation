# Healthcare Data Quality Validation with PyDeequ

This repository demonstrates how to use PyDeequ, the Python wrapper for AWS Deequ, to validate and ensure the quality of healthcare datasets. AWS Deequ is an open-source library built on Apache Spark for data quality validation at scale.

## Overview

The project analyzes three interconnected healthcare datasets (patients, encounters, and procedures) to demonstrate how to implement data quality checks, profiling, and validation in a healthcare analytics context.

## Data Source

The healthcare data used in this project was sourced from [Maven Analytics Data Playground](https://mavenanalytics.io/data-playground?accessType=open&dataStructure=Multiple%20tables&order=date_added%2Cdesc) - specifically the "Hospital Patient Records" dataset. This synthetic dataset simulates real-world hospital patient data and includes:

- **Patients**: Demographic information about patients
- **Encounters**: Records of patient visits and encounters
- **Procedures**: Medical procedures performed during encounters

## Repository Contents

- **Jupyter Notebook**: Complete implementation of PyDeequ for healthcare data validation
- **CSV Files**: 
  - `patients.csv`: Patient demographic information
  - `encounters.csv`: Patient encounter records
  - `procedures.csv`: Medical procedure records
- **Python Modules**:
  - Data loading and preprocessing
  - Data profiling and analysis
  - Data quality verification
  - Results visualization and reporting

## Key Features

This implementation demonstrates:

1. **Environment Setup**: Configuring Java, Spark, and PyDeequ dependencies
2. **Data Profiling**: Analyzing key statistics of healthcare datasets
3. **Data Quality Checks**:
   - Completeness validation for critical fields
   - Format validation for demographic information
   - Value range checks for financial data
   - Consistency checks across related datasets
4. **Results Reporting**: Formatted output of validation results

## Requirements

- Python 3.7+
- Java 11
- Apache Spark 3.5.x
- PyDeequ
- PySpark
- Pandas
- SQLite (for storage)

## Usage

### Google Colab

The notebook is designed to run in Google Colab. It includes all the necessary setup steps to install and configure the required dependencies.

### Local Installation

If running locally:

1. Install Java 11 and set JAVA_HOME
2. Install Apache Spark 3.5.x and set SPARK_HOME
3. Install Python dependencies:
   ```
   pip install pyspark==3.5.0 pydeequ pandas faker tabulate
   ```
4. Download the required JAR files:
   - SQLite JDBC driver
   - Deequ 2.0.7 JAR for Spark 3.5

## Key Findings

The analysis revealed:

- High completeness (100%) for most critical healthcare fields
- Consistent pricing patterns for encounters
- Wide variability in procedure costs ($100 to $289,531)
- Partial completion for optional fields like reason codes
- Balanced gender distribution (49.28% female, 50.72% male)

## Learning Resources

To learn more about AWS Deequ and data quality:

- [AWS Deequ GitHub Repository](https://github.com/awslabs/deequ)
- [PyDeequ Documentation](https://pydeequ.readthedocs.io/)
- [Data Quality Fundamentals (AWS Blog)](https://aws.amazon.com/blogs/big-data/validate-data-quality-with-aws-deequ/)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Maven Analytics for providing the healthcare dataset
- AWS for developing the Deequ library
- The open-source community for PyDeequ
