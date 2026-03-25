# Austin Housing Market Analytics: Power BI, Power Query, Data Modelling and Dashboard Reporting Project

## Executive Summary

This project analyses 15,171 residential property records from the Austin housing market and transforms raw housing data into a structured, interactive Power BI reporting dashboard. The dashboard suite was built to help users quickly understand market size, pricing patterns, property characteristics, and the main factors associated with higher-value homes.
The final solution includes two interactive dashboard pages:
   A market overview dashboard summarising property count, home prices, lot size, living area, home types, ZIP code distribution,   
   build year trends, and key property features.
   A features and price analysis dashboard focused on identifying the main drivers of listing price using feature comparisons, trend 
   analysis, keyword analysis, and Key Influencers in Power BI.
This project demonstrates practical skills in Power Query, data modelling, DAX, KPI reporting, dashboard design, and business insight generation.

## Business Problem


The project addressed two main challenges in the raw housing dataset:

### Data preparation challenges

      1. The raw dataset contained too many columns for efficient analysis.
      2. Repeated attribute combinations created unnecessary redundancy.
      3. Some field values and formatting were inconsistent.
      4. Binary fields were not business-friendly for reporting.
      5. Text-heavy description fields increased model size and complexity.
      6. The data required cleaning, standardisation, deduplication, and restructuring before analysis

### Reporting and analysis challenges

      1. It was difficult to identify overall market patterns from the raw data.
      2. Property segments were not easy to compare in a clear reporting format.
      3. Key drivers of listing price were not immediately visible.
      4. The dataset did not support fast, interactive business analysis in its original form.

### Project objective

Transform the raw housing dataset into a clean, structured, and business-friendly dashboard that supports interactive analysis and clearer market insights.


## Methodology

This project was completed in Power BI using Power Query, dimensional data modelling, DAX measures, and interactive dashboard design.

### Data Cleaning and Transformation
   
      1. Loaded the raw housing dataset into Power Query for preparation and transformation.
      2. Cleaned and transformed 15,172 property records to improve reporting readiness.
      3. Standardised text fields and improved consistency across selected columns.
      4. Converted binary True/False fields into more business-friendly Yes/No values.
      5. Removed duplicate attribute combinations to reduce redundancy in the dataset.
      6. Applied transformation and formatting rules to improve data quality and usability.
      7. Reduced the main housing table from 47 columns to 21 columns before modelling.
      
### Data Modelling

1. Rebuilt the raw dataset into a relational star-style model centred on the
      housing_fact table.
   
2. Created supporting dimension tables, including:

      location
      house
      schools
      features
      description
      
3. Created analytical support tables including:

      features_pivot for feature-based comparison analysis
      word_summary_pqe for optimised word-frequency analysis
      
4. Built relationship keys such as house_key, school_key, feature_key, and zpid to connect fact and supporting tables.

5. Organised the model to reduce redundancy, improve maintainability, and support more efficient analysis.

   <img width="529" height="390" alt="image" src="https://github.com/user-attachments/assets/95409284-431e-4f88-b15f-7b2259d54d3b" />

### Text and Feature Analysis Preparation
Separated property description content into a dedicated text-analysis structure.
Created a summary word table to support dynamic word ranking across price groups.
Used a Power Query–based summary approach to improve performance compared with a heavier DAX-driven structure.
Prepared feature attributes in a pivoted format to analyse how housing features related to listing price.


### 3. Analysis and Dashboard Reporting

 Built structured POWER BI, KPIs and charts

 Analysed 15,171 property listings

 Created summary views by:

        city
        
        home type
        
        bedroom count
        
        school rating band

Designed a dashboard to present key pricing and market insights

You can view the dashboard output here:


<img width="1525" height="853" alt="image" src="https://github.com/user-attachments/assets/c1e6fb5f-0884-424f-94ba-2d966e778a13" />


<img width="1503" height="853" alt="image" src="https://github.com/user-attachments/assets/953b3bf3-8071-4f4e-b89b-1aea9cbca51a" />



## Skills

        POWER BI
        Power Query
        Data Cleaning
        Data Transformation
        Relational Data Modelling
        KPI Reporting
        Dashboard Design
        Duplicate Removal


  ##  Results & Business Recommendation

  ### Key Results

        Cleaned and transformed 15,172 records
        Reduced the main table from 47 columns to 21 columns
        Built a relational model with 6 linked tables
        Analysed 15,171 listings

  ### City Summary

    Austin dominates the dataset with 15,020 properties, an average price of $514,785, and an average living area of 2,210 sq ft.         Smaller locations such as West Lake Hills and Dripping Springs show much higher average prices and larger homes, although their       property counts are very low.

    #### Recommendation:
    Focus reporting on both high-volume markets and premium niche suburbs. High-volume areas help identify overall market behaviour,      while smaller high-value suburbs may indicate premium pricing segments.

<img width="367" height="170" alt="Screenshot 2026-03-16 150031" src="https://github.com/user-attachments/assets/aaa9b3f1-f43c-4f13-acd0-fda32562dcd1" />

  ### Home Type Summary

        Single Family properties account for 14,241 listings, making them the dominant segment in the dataset, with an average price         of $516,388. Vacant Land and MultiFamily properties show higher average prices, but they represent much smaller volumes.
        
        #### Recommendation:
        For reporting and business analysis, treat Single Family homes as the core market segment, while using smaller categories             such as Vacant Land and MultiFamily to identify specialised or premium opportunities.


<img width="370" height="196" alt="Screenshot 2026-03-16 150052" src="https://github.com/user-attachments/assets/5949a385-1f35-4f76-8e26-3b1dabf6d1c4" />


### Achievements

    Reduced report size by ~40%
    Improved refresh and query speed
    Built scalable dimensional architecture
    Enabled keyword-level text analysis
    Enhanced model maintainability

### Business Recommendations

    Apply dimensional modeling early in BI projects
    Separate unstructured text from fact tables
    Normalize repetitive attributes
    Optimize data types and precision
    Design for scalability from the beginning

These practices improve system reliability and reduce long-term maintenance costs.

## Next Steps

Future improvements include:

    Integrating Python-based NLP for deeper text analysis
    Building predictive pricing models
    Automating refresh pipelines
    Deploying reports to Power BI Service
    Implementing monitoring and alert systems

These enhancements would further increase analytical value and
