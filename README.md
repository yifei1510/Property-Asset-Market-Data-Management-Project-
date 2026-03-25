# Austin Housing Market Analytics: Power BI, Power Query, Data Modelling and Dashboard Reporting Project

## Executive Summary

Built an interactive Power BI dashboard solution to analyse 15,171 residential property records and turn raw housing data into clear market insights. The dataset was cleaned, standardised, deduplicated, and remodelled from 47 columns to 21 columns, then restructured into a relational model to improve reporting efficiency and usability.

The final solution highlighted key metrics including a median home price of $405,000, median living area of 1,975 sq ft, and median lot area of 8,276 sq ft, while also analysing price differences across home type, ZIP code, build year, structural attributes, premium features, and listing descriptions. Model optimisation further reduced the Power BI file size from 5,318 KB to 2,973 KB.

Live Dashboards:

[Summary Insight](https://app.powerbi.com/groups/me/reports/3fa174c1-7367-4134-9264-b3257dd45974/a268de0cf7222dc8033d?experience=power-bi)

[Price Analysis](https://app.powerbi.com/groups/me/reports/3fa174c1-7367-4134-9264-b3257dd45974/4e38970ef0bd2d8ffbb9?experience=power-bi)

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


## Skills

      Power BI
      Power Query
      Data Cleaning and Transformation
      Data Standardisation and Deduplication
      Relational Data Modelling
      DAX and KPI Reporting
      Interactive Dashboard Design
      Data Visualisation


  ##  Results & Business Recommendation

  The final Power BI solution transformed 15,171 residential property records into a structured analytics dashboard, making it easier   to evaluate market conditions, compare property segments, and identify key drivers of listing price. After cleaning and 
  restructuring the dataset, the main table was reduced from 47 columns to 21 columns, then rebuilt into a relational model to
  improve reporting efficiency and support interactive analysis.

 ### Overview Dashboard

This dashboard provides a high-level market view across pricing, property type, location, build year, and feature availability.

<img width="698" height="393" alt="image" src="https://github.com/user-attachments/assets/befb5486-b729-4349-a045-cdaca4dab68a" />


      1. The dashboard summarised 15,171 properties, with a median home price of $405,000, median living area of 1,975 sq ft, and              median lot area of 8,276 sq ft.
      2. The market was heavily dominated by Single Family homes (14,241 listings), far exceeding other property types such as condos          and townhouses.
      3. Average home price ($512,768) was noticeably higher than median home price, showing that listing prices were influenced by   
         high-value outliers.
      4. Property distribution by build year showed stronger listing concentration in more recent decades, helping highlight where   
         current market supply is clustered.
      5. Feature availability analysis showed that cooling (98.19%) and heating (99.02%) were almost universal, while premium 
         features such as spa (7.90%) and view (22.77%) were less common.

### Feature and Price Analysis Dashboard

<img width="664" height="386" alt="image" src="https://github.com/user-attachments/assets/5961649f-cf51-46fe-8c60-e501d26387b7" />


This dashboard explores how property features, structural attributes, and listing descriptions relate to higher listing prices.

Feature comparison showed that homes with spa, view, heating, and garage access generally had higher median listing prices than those without these features.

Key Influencers analysis identified strong price drivers such as:

      Living area above 4,263 sq ft
      More than 4.5 bathrooms
      Lot size above 25,700 sq ft
      2–3 stories
      Newer build years

### Key Result

Text analysis across 7 custom price bands showed clear differences in listing language. Lower-priced homes more often used practical terms such as kitchen, bedrooms, and family, while higher-priced homes more often included premium terms such as pool, private, lake, and views.

The project also improved model performance by redesigning the text-analysis structure from approximately 738,000 rows to around 29,285 rows, making dynamic ranking visuals more responsive.

### Business Recommendation

      Use median-based KPIs instead of averages when reporting housing prices, as median values better represent the market in the  
      presence of extreme listings.
      
      Prioritise segmentation by home type, location, build year, living area, lot size, and premium features, as these variables 
      showed stronger relationships with listing price.
      
      Use feature-level insights to support pricing and positioning decisions, especially for homes with premium attributes such as 
      spa and view.
      
      Apply text-based listing analysis to improve marketing strategy, since language patterns differ across price segments and can 
      help align descriptions with target buyers.
      
      Maintain a structured relational model for future reporting, as the redesign improved both analytical flexibility and 
      performance.


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
