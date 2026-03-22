# Austin Housing Market Analytics: Excel, Power Query, Data Modelling and Dashboard Reporting Project

## Executive Summary

This project analyses 15,171 residential property records from the Austin housing market and transforms raw housing data into a structured, interactive Power BI reporting solution. The dashboard suite was built to help users quickly understand market size, pricing patterns, property characteristics, and the main factors associated with higher-value homes.
The final solution includes two interactive dashboard pages:
   A market overview dashboard summarising property count, home prices, lot size, living area, home types, ZIP code distribution,   
   build year trends, and key property features.
   A features and price analysis dashboard focused on identifying the main drivers of listing price using feature comparisons, trend 
   analysis, keyword analysis, and Key Influencers in Power BI.
This project demonstrates practical skills in Power Query, data modelling, DAX, KPI reporting, dashboard design, and business insight generation.

## Business Problem

Residential property data often contains many variables such as home type, build year, living area, lot size, ZIP code, and property features. Without a structured reporting solution, it is difficult to identify:
    overall market conditions and pricing levels
    which property types dominate the market
    how property features relate to listing price
    what characteristics are associated with premium homes
    how listing descriptions differ across price segments
The goal of this project was to convert a large raw housing dataset into a clear, business-friendly dashboard that supports fast insight generation and interactive exploration.


## Methodology

The project was completed in Excel using Power Query, data modelling logic, Pivot Tables and charts.

### 1. Data Cleaning and Transformation

    Loaded the raw housing dataset into Power Query

    Cleaned and transformed 15,172 records
    
    Standardised text fields and improved field consistency
    
    Removed duplicate attribute combinations
    
    Applied transformation rules to improve reporting readiness
    
    Reduced the main table from 47 columns to 21 columns

### Data Modeling

  Rebuilt the dataset into a relational model with 6 linked tables

  Created:

        housing_fact
        
        location
        
        house
        
        schools
        
        features
        
        description

Created relationship keys to connect fact and supporting tables

Organised data to reduce redundancy and improve analysis efficiency

<img width="622" height="416" alt="Screenshot 2026-03-09 204208" src="https://github.com/user-attachments/assets/db7f5a7f-6248-4321-bbf7-3fe5feebcfca" />


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
