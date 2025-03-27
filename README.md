**Cloud-Based Data Analytics Platform for Bikeways – City of Vancouver**

**Objective:**
        
        The aim of this project is to build a scalable, cloud-based Data Analytics Platform (DAP) for analyzing the City 
        of Vancouver’s bikeways infrastructure data. Leveraging the power of Amazon Web Services (AWS), this platform 
        enables ingestion, profiling, transformation, and analysis of bikeway-related datasets to derive actionable 
        insights for urban planning and transportation safety.
        
        Using key AWS services such as Amazon S3, AWS Glue, AWS Glue Studio, Glue DataBrew, AWS Athena, IAM, CloudTrail, 
        CloudWatch, and KMS, the solution covers end-to-end data analytics—from raw ingestion to secure governance 
        and monitoring.
      
        The primary focus of this platform is to:
                  •	Understand bikeway infrastructure distribution, speed limits, and construction trends.
                  •	Automate data cleaning, validation, and transformation workflows.
                  •	Empower decision-makers through real-time querying and analytics.
                  •	Ensure data quality, compliance, and security using best-in-class governance practices.

        The project follows a structured methodology encompassing exploratory, descriptive, and diagnostic analysis, 
        paired with robust data quality control, monitoring, and governance frameworks. Each phase contributes to 
        building a dependable analytical foundation that supports the City of Vancouver in promoting sustainable, 
        cyclist-friendly development.

 **1) Exploratory Data Analysis - Exploring the City of Vancouver Bikeways Dataset Using AWS Cloud Analytics**

        The primary goal of this project is to perform exploratory data analysis (EDA) on the City of Vancouver’s 
        bikeways dataset. This analysis aims to understand the distribution, types, and construction patterns of 
        bikeways across the city. Using AWS services like Athena and Glue, we identified trends in speed limits, 
        bikeway types, and year of construction to support data-driven urban mobility planning.
        
        In the exploratory phase of the bikeways data analytics project, the focus was on understanding the structure, 
        completeness, and quality of the raw dataset before diving into advanced analysis. The dataset was sourced from 
        the City of Vancouver Open Data Portal and primarily included details such as Bikeway Type, Segment Length, 
        Speed Limit, Year of Construction, and Snow Removal information.
         
         To begin, we ingested the raw CSV file into an Amazon S3 bucket, which served as the central storage for 
         the analytics workflow. From there, AWS Glue DataBrew was used to perform data profiling, which allowed us to 
         detect null values, outliers, and inconsistent data formats across different fields.
         
         Using AWS Glue Data Catalog, we created a crawler to automatically classify the schema and register the dataset, 
         making it queryable in Athena. This helped streamline the subsequent stages of transformation and querying.
         This phase also involved renaming columns for clarity, standardizing data types (e.g., converting Speed 
         Limit to numerical format), and dropping unnecessary columns to simplify the structure. 
         These refinements ensured a consistent and clean dataset for downstream analytics.

         The architectural workflow for this stage includes:
                1. Amazon S3 – Raw data storage
                2. AWS Glue DataBrew – Profiling and initial cleaning
                3. AWS Glue Data Catalog – Schema creation and metadata registry
                4. Amazon Athena – Ready for SQL-based querying in the next stages

**Dataset:**

         The dataset used in this project is the “Bikeways Painted Lanes” dataset, sourced from the City of Vancouver Open Data Portal. It includes key attributes such as:
                  •	Bikeway Type
                  •	Route Name
                  •	Speed Limit
                  •	Segment Length
                  •	Year of Construction
                  •	Snow Removal Support
                  •	Segment Geometry
 
**Methodology:**

    • Data Collection: Raw data was ingested from Amazon S3.
    • Data Profiling & Cleaning: AWS Glue and DataBrew were used for profiling and cleansing. Unnecessary columns were removed, and missing values were addressed.
    • Data Cataloging: Metadata was organized using AWS Glue Data Catalog.
    • Analysis: Athena SQL queries were used to identify patterns, such as:

           o Average speed limit by year of construction
           o Total bikeway length by type
           o High-speed segments
           o Correlation between construction year and speed
           o Percentage distribution of bikeway types

**Tools and Technologies:**

      • AWS S3
      • AWS Glue DataBrew
      • AWS Glue (ETL pipeline)
      • AWS Athena
      • AWS IAM (access control)

**Deliverables:**

      • Profiled and cleaned dataset
      • Identified initial data trends and inconsistencies
      • Prepared dataset for deeper analysis
 
**Recommendation:** 

      To enhance exploratory analysis, it is recommended to integrate visualization tools like Amazon 
      QuickSight or Python-based libraries to create real-time graphical summaries. This will improve stakeholder 
      understanding of the dataset’s structure and support interactive exploration.

**Conclusion:**

      The exploratory analysis of the City of Vancouver’s bikeways dataset successfully established a foundational 
      understanding of the data’s structure, completeness, and quality. By utilizing AWS Glue DataBrew for profiling 
      and standardization, and AWS Glue Catalog for schema organization, we ensured the dataset was clean, consistent, 
      and analysis-ready. This phase also highlighted key data issues—such as missing speed limit values and 
      inconsistencies in formatting—that were resolved before further processing. Overall, the exploratory phase 
      was critical in preparing the dataset for advanced querying, statistical analysis, and decision-making support.
      
**2) Descriptive Analysis - Understanding Bikeway Infrastructure Patterns in the City of Vancouver**

**Objective:**
 
       The primary objective of this descriptive analysis is to examine key attributes of the City of Vancouver’s 
       bikeways infrastructure. By summarizing the characteristics such as bikeway type, speed limit, 
       year of construction, and segment length, the goal is to identify trends, usage patterns, and 
       infrastructure priorities that support urban mobility and transportation planning.

**Dataset:**

      The analysis is based on the “Bikeways Painted Lanes” dataset sourced from the City of 
      Vancouver Open Data Portal. The dataset includes the following relevant fields:
              • Bikeway Type
              • Bike Route Name
              • Year of Construction
              • Speed Limit
              • Segment Length
              • Snow Removal Status
              • Geographical Information (Coordinates)
              
**Methodology:**

**1. Data Preparation:**

        o Data was ingested from Amazon S3 and profiled using AWS Glue DataBrew to identify 
          missing values and inconsistencies.
        o Cleaned and structured data was cataloged using AWS Glue Data Catalog for easy querying.

**2. Descriptive Queries using Athena:**

       o Average Speed Limit by Year of Construction → To analyze how speed limits have evolved over time.
       o Total Segment Length by Bikeway Type → To determine which types dominate Vancouver’s bikeway network.
       o Identification of High-Speed Segments (above 50 km/h) → To locate segments requiring possible safety reviews.
       o Percentage Distribution of Bikeway Types → To evaluate infrastructure design preferences.
       o Correlation Between Year and Speed Limit → To examine if newer bikeways are associated with 
         slower or faster routes.

**3. Visualization:**

        Results were visualized using figures and dashboards generated from Athena output:
        
          o Distribution trends
        
          o Speed and safety relationships
        
          o Infrastructure coverage insights

**Tools and Technologies:**

    • AWS Athena – For executing SQL-based descriptive queries
    • AWS Glue DataBrew – For data cleaning and profiling
    • AWS S3 – For raw and curated data storage
    • AWS Glue Catalog – For schema management

**Deliverables:**

    • SQL query outputs with summarized statistics
    • Charts and visualizations showing distribution by type, year, and speed
    • Dataset segments tagged by speed thresholds for further review

**Recommendation:** 

     To enhance the descriptive insights, it is recommended to integrate geospatial tools such 
     as AWS Location Service or external platforms like QGIS to visualize the bikeway network 
     across Vancouver’s neighborhoods. This will provide a spatial understanding of infrastructure 
     gaps and usage trends.


**Conclusion:**

     The descriptive analysis provided valuable insights into the patterns and characteristics 
     of bikeways infrastructure across Vancouver. By summarizing trends in bikeway types, 
     segment lengths, speed limits, and year of construction, we uncovered essential findings 
     that support strategic urban planning. Notably, separated and off-street bikeways accounted 
     for a significant portion of infrastructure, and recent constructions demonstrated a trend 
     toward lower speed limits—indicating a growing focus on cyclist safety. These insights will 
     inform policymakers and planners in optimizing the city’s transportation network, ensuring 
     both accessibility and safety for all users.

**3) Diagnostic Analysis - Investigating the Influencing Factors Behind Bikeway Infrastructure Trends in the City of Vancouver**


      The primary goal of this diagnostic analysis is to uncover the underlying factors affecting 
      the development and variation of bikeways in the City of Vancouver. Through the use of statistical 
      methods and relational analysis, this section aims to explain trends related to speed limits, 
      bikeway types, and construction periods. The insights derived will help the city’s planning 
      teams understand infrastructure performance and inform future policy decisions.

**Background:**
 
     While the City of Vancouver has made significant investments in improving urban mobility 
     through bikeways, differences in speed regulations, construction years, and bikeway types 
     suggest varying design choices and priorities. A diagnostic analysis is necessary to investigate 
     whether certain conditions—such as year of construction—are influencing speed limits or 
     infrastructure decisions. Understanding these patterns will support better alignment of 
     policy with the city’s safety and mobility goals.

**Dataset:**
    
      This analysis utilizes a curated version of the “Bikeways Painted Lanes” dataset that includes:
             • Bikeway Type
             • Segment Length
             • Speed Limit
             • Year of Construction
             • Snow Removal Status
             • Route Name

**Methodology:**
 
      1. Data Preparation:
            o Cleaned and structured data was prepared using AWS Glue DataBrew and stored in Amazon S3.
            o The data was cataloged using AWS Glue Crawlers and queried via Amazon Athena.
      2. Trend Analysis:
            o Assessed how average speed limits varied by year of construction to identify 
              regulatory or design changes over time.
      3. Correlation Analysis:
            o Used SQL functions in Athena (e.g., CORR) to identify correlation between 
              year of construction and speed limits.
            o Examined whether newer bikeways tend to have lower speed limits, 
              suggesting improved safety practices.
      4. Outlier Detection:
            o Queried and isolated bikeway segments with speed limits 
              above 50 km/h to determine potential safety risks.
            o Cross-referenced these segments by bikeway type 
              and snow removal support.
      5. Infrastructure Segmentation:
            o Grouped bikeways by type and analyzed their total segment 
              length and average speed to understand design intent and usage context.
      6. Synthesis of Findings:
            o Integrated the results of statistical queries to determine which infrastructure 
              types or historical periods are associated with higher or lower speed limits and broader  infrastructure growth.

**Tools and Technologies:**

       • Amazon Athena: SQL querying and statistical calculations
       • AWS Glue Data Catalog: Metadata management
       • Amazon S3: Data storage
       • Glue DataBrew: Pre-cleaning and transformation

**Deliverables:**
 
       • A detailed diagnostic report summarizing key patterns and correlations
       • Identification of outlier bikeway segments and their contextual insights
       • Recommendations for speed regulation and infrastructure planning based 
         on data-driven findings
       • Visualizations to support analytical narratives (charts, histograms, maps)

**Timeline:**
   
       • Completion estimated within 2 weeks post-cleaning phase
       • Iterative discussions with project stakeholders to refine insights

**Conclusion:**
 
     This diagnostic analysis contributes to the City of Vancouver’s urban mobility 
     goals by identifying patterns in bikeway infrastructure development. By correlating design 
     features with speed and usage trends, this study equips planners with actionable 
     knowledge to design safer, more effective bikeway systems in the future.

**4) Data Quality Control - Implementation of Data Quality Control Measures for Bikeways Data – City of Vancouver**

        The primary objective of this initiative is to implement a structured Data 
        Quality Control (DQC) process for the bikeways dataset used by the City of Vancouver. 
        This ensures that the data used for analysis is accurate, complete, consistent, and 
        reliable, ultimately supporting better planning, operational decision-making, and 
        public infrastructure investment.
        
       During the initial data profiling and exploratory analysis phases, the bikeways dataset 
       revealed issues such as missing speed limits, inconsistent formatting, and unused or 
       redundant columns. To maintain high data quality standards throughout the analytics pipeline, 
       a dedicated quality control framework was required. By automating validation and 
       cleaning processes within AWS Glue, the City of Vancouver can avoid flawed insights 
       and build a dependable foundation for its urban planning efforts.

       The DQC process focused on the following areas:
        
          •	Data Profiling: Identifying issues like null values and inconsistent formats using AWS Glue DataBrew.
          •	Data Cleaning: Dropping unused columns, converting data types, and resolving missing or incorrect values.
          •	Validation Rules: Applying filters and logic to ensure that only consistent and complete records move forward.
          •	Segregation of Passed and Failed Records: Using conditional routing to separate records for further review.
          •	Automation & Monitoring: Creating an automated AWS Glue visual ETL pipeline to ensure consistent, ongoing quality checks.
          
**Methodology:**

     1. Assessment of Raw Data:
     
            o Uploaded raw CSV bikeways dataset to Amazon S3.
            o Evaluated issues in fields such as speed limit, year of construction, and segment length.
        
     2. Data Profiling with AWS Glue DataBrew:
     
            o Performed column-level analysis to detect nulls, invalid formats, and inconsistent values.
            o Generated profiling reports to assess completeness, consistency, and accuracy.
        
     3. ETL Pipeline Creation:
     
            o Designed a visual ETL pipeline named bikeways-QC-dee in AWS Glue Studio.
            o Used conditional routers to evaluate row-level outcomes of records based on predefined quality rules.
        
     4. Segregation Strategy:
     
            o Records that passed all validation checks were transformed and loaded into a curated “Passed” S3 bucket.
            o Failed records were redirected into a “Failed” path, maintaining transparency for auditing or correction.
        
     5. Data Schema Alignment:
     
           o Used the “Change Schema” transform to standardize field names and formats before final load.
        
     6. Monitoring Setup:
     
           o Established real-time job monitoring using AWS CloudWatch metrics tied to Glue job performance.
           o Ensured alerts and logs were configured to flag failed or incomplete runs.
        
**Tools and Technologies:**

     • Amazon S3: Raw and curated dataset storage
     • AWS Glue Studio: ETL pipeline development for automated data validation
     • AWS Glue DataBrew: Data profiling and quality issue detection
     • Amazon CloudWatch: Real-time job monitoring and alerting

**Deliverables:**

    • A fully automated ETL pipeline with data quality checks built-in
    • Passed and failed datasets segregated in S3 buckets
    • Data profiling summary reports and validation logic documentation
    • Cleaned and standardized dataset ready for advanced analysis
    • Glue job logs and monitoring dashboards via CloudWatch

**Timeline:**

    • Week 1–2: Raw data ingestion and profiling
    • Week 3–4: ETL pipeline design and conditional routing
    • Week 5: Schema transformation and testing
    • Week 6: Monitoring integration and validation
    • Week 7–8: Documentation and handoff for future use

**Conclusion:**

     By integrating data quality control early in the bikeways data pipeline, 
     the City of Vancouver ensures that all subsequent analysis is built on clean, 
     accurate, and trustworthy data. This process supports ongoing governance and 
     allows for sustainable, automated data processing as new bikeways data is collected over time.

**5) Monitoring - Real-Time Monitoring and Logging for Bikeways Data Analytics Platform – City of Vancouver**

    The objective of this component is to establish a robust monitoring system for 
    the Bikeways Data Analytics Platform (DAP) to ensure high system availability, 
    data pipeline reliability, and full visibility into user interactions. Monitoring 
    allows for proactive detection of failures, performance degradation, and unauthorized 
    data access, enabling timely intervention and operational efficiency.

    As the bikeways dataset flows through various AWS services such as Glue ETL jobs, 
    Athena queries, and S3 storage layers, it is crucial to track system health and user activity. 
    Without proper monitoring, data processing failures, query delays, or unapproved access 
    may go unnoticed. This monitoring initiative supports transparency, security, 
    and compliance while enabling real-time oversight of platform operations.

    This monitoring setup includes:
    
       • Tracking Glue job performance and failure rates.
       • Monitoring query performance and resource usage.
       • Logging all API activity and user interactions.
       • Creating dashboards and alarms for continuous visibility and operational response.
       
**Methodology:**
      
      1.	CloudTrail Logging:

           o Created a trail named bikeways-trail-dee using AWS CloudTrail.
           o Enabled logging of user and API-level activity across all services used (S3, Athena, Glue).
           o Configured logs to be delivered to a dedicated S3 bucket for audit purposes.
      
      2.	CloudWatch Integration:
           
           o Set up a CloudWatch dashboard named bikeways-MCR-dee to track key metrics such as:
                  Glue job success/failure
                  Query durations and failures in Athena
                  Resource utilization
           o Deployed CloudWatch Alarms to notify admins of pipeline job failures or anomalies.
     
      3.	Log Storage and Analysis:
           
           o Stored all CloudTrail and CloudWatch logs in a versioned, secure S3 bucket.
           o Used log groups and filters to extract patterns or recurring issues.

      4.	Audit and Alert Configuration:
           
           o Configured alert emails and SNS notifications to instantly notify teams of 
             system failures or suspicious access attempts.

**Tools and Technologies:**

      • AWS CloudTrail – Tracks all user and API activity
      • Amazon CloudWatch – Monitors ETL jobs and system performance metrics
      • Amazon SNS – Alert delivery for alarms
      • Amazon S3 – Storage for logs and monitoring history

**Deliverables:**

       • CloudTrail logs in S3 for secure audit trails
       • Live CloudWatch dashboard for Glue jobs and query performance
       • Alarm policies for pipeline monitoring
       • System health report and anomaly detection configurations
       • Alerting mechanism for system interruptions and access issues

**Timeline:**

       • Week 1: CloudTrail trail creation and log delivery setup
       • Week 2: CloudWatch dashboard and Glue job metrics integration
       • Week 3: Alarm policies and SNS alerting
       • Week 4: Final validation and monitoring SOP documentation

**Conclusion:**
      
       By integrating a proactive monitoring framework using AWS native tools, the City 
       of Vancouver’s Bikeways Data Analytics Platform gains real-time visibility into 
       operations, improving responsiveness, auditability, and overall reliability. 
       This ensures continuity of data processing and reinforces trust in the 
       analytics outcomes delivered to planners and stakeholders.

**Architecture Diagrams**

**Data Profiling & Cataloging**

<img width="468" alt="image" src="https://github.com/user-attachments/assets/cd796d41-a25d-4830-8b73-6920ce4b0793" />

             
**Quality Check & Monitoring**

![image](https://github.com/user-attachments/assets/b156e647-24b8-49ea-9ef7-05ed309f4283)

**ETL Pipeline - Summarization**

![image](https://github.com/user-attachments/assets/aea71837-b397-4e5b-901f-4e4e841e4e54)


  The Cov-bpl-lst-Summarization ETL pipeline is designed to process and summarize bikeways 
  data from the City of Vancouver. It begins by extracting the dataset from the AWS Glue Data Catalog,
  ensuring it is schema-aware and ready for transformation. A schema transformation step is applied first 
  to standardize field names and data types, followed by a filter stage that removes unwanted or invalid 
  records—such as those with null values or out-of-scope bikeway information. Once filtered, the data proceeds 
  to an aggregation stage where key metrics are summarized, such as total bikeway lengths by type or year of construction.
  To enable tracking and versioning, the current run timestamp is dynamically added to each record and then converted into
  the local time zone format for regional consistency. Before export, the schema is adjusted again to ensure it matches 
  the target structure, and the output is split into two branches: one that loads the clean, summarized data into 
  a system-facing S3 bucket for integration, and another that formats and exports the dataset into a user-facing S3 bucket 
  for reporting or public access. This dual-output design ensures that both internal systems and end users receive reliable 
  and ready-to-use data. The ETL pipeline provides a robust, automated way to transform raw bikeways data into summarized 
  insights that support informed urban planning and analysis.

**ETL Pipeline - Quality Check**

![image](https://github.com/user-attachments/assets/a66e4447-54d3-4e71-a76b-474093b6bac7)

    
     The pipeline starts with "Load Submission" as its initial node that enables the direct 
     Amazon S3 bucket data ingestion. After loading the data into the workflow system it 
     proceeds to the "Data Quality Check" transformation to assess each record against 
     predefined quality rules before advancement.
     
     After data quality assessment the system stores individual record outputs through 
     the "rowLevelOutcomes" node. Each result moves to a "Conditional Router" allowing it to 
     determine the following processing stage for records based on their quality meets requirements. 
     Further processing happens at the correct branch dependent on the assessment results.
     
     A Conditional Router divides data distribution into separate streams which depend on 
     the results of the quality evaluation process. The Quality_passed branch processes records 
     which meet every established quality criterion. A change schema transformation processes 
     valid records before they join the target structure process. The S3 bucket for clean data 
     receives processed data after adjustment through the "Prepare Load" step. Records which fail 
     the quality check are piped to “default_group” on the right-hand branch for subsequent processing. 
     These entries experience schema transformation parallel to passed records during 
     the “Prepare to Load in Failed Path” step. The system stores all failed records in 
     a dedicated Load – Failed Records S3 bucket which enables later review and 
     correction or reprocessing operations.

      The S3 transform bucket cov-trf-dee now contains a QualityCheck folder 
      that splits into two subfolders: Passed and Failed. Records that comply with all quality benchmarks are 
      kept in the Passed section of the Stores bikeway database. The Failed subfolder contains data files 
      that present at least one quality fault through missing speed limits and incorrect 
      construction years and invalid coordinates. The configuration enables the partitioning of good quality records 
      from problematic ones so pure data reaches analysis and decision-making. This setup enables proactive 
      data monitoring and retains the analytic integrity of the bikeways system through its pipeline operations.
       
       The S3 transform bucket cov-trf-dee now contains a QualityCheck folder that splits into two subfolders: Passed and Failed. 

            o The Failed subfolder contains data files that present at least one quality fault through 
            missing speed limits and incorrect construction years and invalid coordinates.
            o Records that comply with all quality benchmarks are kept in the Passed section of the Stores bikeway database. 
            
      The configuration enables the partitioning of good quality records from problematic ones 
      so pure data reaches analysis and decision-making. This setup enables proactive data monitoring 
      and retains the analytic integrity of the bikeways system through its pipeline operations.

**Gap Analysis – Bikeways Cloud Data Analytics Platform**
        
        The implementation of the Bikeways Data Analytics Platform for the 
        City of Vancouver was guided by core AWS Well-Architected Framework principles. 
        While several best practices were applied across the project lifecycle, 
        there remain areas where enhancements could further optimize system performance, efficiency, and reliability.

**1. Reliability**

**What Was Done Well:**

    Implemented data replication using Amazon S3 rules to ensure dataset availability in case of failure.
    Enabled bucket versioning to track and recover previous data states.
    Created CloudWatch alarms and Glue job monitoring to detect and respond to operational failures.
    Designed a visual ETL pipeline with a fallback route for failed records, ensuring uninterrupted data processing.

**What Can Be Improved:**

    Introduce multi-region data backup to further strengthen disaster recovery.
    Incorporate retry and failover mechanisms in Glue workflows to handle transient errors without manual intervention.
    Define Recovery Time Objective (RTO) and Recovery Point Objective (RPO) for the analytics platform.

**2. Operational Excellence**

**What Was Done Well:**

    Used AWS Glue Studio to implement repeatable ETL pipelines, reducing manual steps.
    Employed CloudTrail for complete tracking of user and API activity for governance and audits.
    Conducted data quality checks to segregate clean and invalid records and avoid downstream errors.

**What Can Be Improved:**

    Infrastructure was created manually; introducing Infrastructure as Code (IaC) 
    tools like AWS CloudFormation or Terraform would improve repeatability and minimize human error.
    Standard Operating Procedures (SOPs) for job reruns, error handling, 
    and pipeline updates should be documented and version-controlled.
    Adopt code repositories (e.g., CodeCommit) for tracking pipeline and transformation logic changes.

**3. Performance Efficiency**

**What Was Done Well:**
  
    Leveraged Amazon Athena to run SQL queries directly over S3, 
    avoiding unnecessary data movement and compute resource provisioning.
    Dropped unused columns and optimized data types early in the pipeline to reduce processing overhead.

**What Can Be Improved:**
       
    Consider partitioning data in S3 (e.g., by year or bikeway type) 
    to improve query efficiency and reduce scan costs.
    Enable Athena query result caching for faster repeated query execution.
    Use QuickSight or BI tools for lightweight visualization, reducing reliance on heavyweight querying.

**Conclusion:**

    The Bikeways Data Analytics Platform successfully implemented core 
    cloud-native principles, enabling secure, scalable, and insightful analytics. 
    By addressing current gaps—especially in automation, failover design, and infrastructure 
    codification—the platform can evolve into a more resilient and high-performing solution. 
    Continuous refinement will allow the City of Vancouver to maximize value from its 
    bikeway data and support forward-thinking, data-driven urban development.

![image](https://github.com/user-attachments/assets/0fca0302-9136-47da-a4ca-1111dc795f3e)
