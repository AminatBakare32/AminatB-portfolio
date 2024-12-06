# AminatB-portfolio
# AWS Data Analytics Platform (DAP) for the City of Vancouver

## **Project Title**
AWS Data Analytics Platform for the City of Vancouver

## **Project Description**
This project involves designing and implementing a scalable AWS-based Data Analytics Platform (DAP) for the City of Vancouver. It aims to analyze trends in construction, renovation, and development projects using data from the Issued Building Permits dataset. The project provides descriptive and exploratory analytics while ensuring robust data governance, security, and cost optimization.

## **Objective**
- Establish an efficient and scalable AWS DAP for processing and analyzing urban data.
- Support descriptive and exploratory analytics for data-driven decision-making.
- Implement data protection, governance, and cost estimation.

## **Dataset**
- **Source:** Issued Building Permits dataset from [City of Vancouver Open Data Portal](https://opendata.vancouver.ca).
- **Timeframe:** March 15, 2024, to November 20, 2024.
- **Key Fields:**
  - `permit_num`
  - `type_of_work`
  - `project_value`
  - `permit_elapsed_days`
  - `ValueCategory`
  - `issueyear`

## **Methodology**
### **Part 1**
1. **Data Ingestion**:
   - Raw data ingested into AWS S3 (`cv-raw-ami` bucket).
   - Profiled using AWS Glue DataBrew to identify quality issues.
2. **Data Profiling**:
   - Insights derived, such as missing data rates and correlations between fields.
3. **Data Cleaning**:
   - Null and invalid values corrected; saved to `cv-trf-ami` bucket.
4. **Pipeline Design**:
   - Automated ETL processes using AWS Glue.

### **Part 2**
1. **Data Governance**:
   - Defined quality checks for completeness, uniqueness, and freshness using AWS Glue Data Quality.
2. **Data Protection**:
   - Enabled bucket encryption using AWS KMS.
3. **Data Enrichment**:
   - Enhanced datasets by Creating a DataCatalog and running queries on Amazon Athena using my crawler files.
4. **Observability**:
   - Monitored pipelines via CloudWatch and logged anomalies.

## **Tools and Technologies**
- **AWS Services**: Glue, Amazon Athena, S3, Cloudwacth, AWS Databrew Glue, KMS.
- **Programming**: SQL
- **Visualization**: Dashboards and logs.

## **Deliverables**
1. **Descriptive Analysis**:
   - Insights on average processing times for each `type_of_work`.
   - Example: "New Building" projects take the longest (857 days).
2. **Exploratory Analysis**:
   - Correlation of processing times with project values and permit volumes.
3. **Data Governance and Protection**:
   - Data quality and privacy checks.
   - Encrypted buckets (`cv-trf-ami` and `cv-cur-ami`).
4. **Cost Analysis/Dashboard**:
   - Monthly AWS operational costs estimated between $2.47 and $29.64.
