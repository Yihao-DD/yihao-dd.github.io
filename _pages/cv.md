---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* M.S. in Applied Data Science, University of Sothern California, 2026(expected)
* B.S. in Computer Science and Technology, Hong Kong Baptist University, 2024

Work experience
======
* **Summer 2024: Intern Backend engineer**
  * **Henan Cdcenter network technology Co., Ltd.**
  * **Duties includes:**
      * **Pipeline Development:** Built and maintained scalable ETL pipelines using Python (pandas, SQLAlchemy) and SQL, handling both structured (PostgreSQL) and semi-structured data (JSON, CSV) from multiple sources to support analytical reporting.
      * **Workflow Orchestration:** Utilized Apache Airflow to schedule and monitor batch processing jobs, improving data pipeline reliability and transparency.
      * **Data Processing:** Processed multi-terabyte datasets using Spark SQL and Hive, optimized query performance, and reduced execution time by 25% through partitioning and caching strategies.
      * **Data Warehousing:** Supported data modeling and table design in Hadoop Hive for business dashboards and KPI tracking. Worked closely with analysts to align schema design with downstream requirements.
      * **Data Quality:** Implemented data validation and automated alerts to ensure pipeline stability; developed unit tests for ETL modules.
      * **Team Coordination:** Documented data assets and collaborated with BI and analytics teams to ensure data usability and traceability.
      * **Access Control:** Assisted in implementing row-level access control policies and data cataloging to align with internal data governance standards.

* **Summer 2023: Intern Data Analyst**
  * **China Life Insurance Co., Ltd.**
  * **Duties included:**
      * **Risk Modeling:** Designed and implemented a user risk profiling model based on insurance policy data and customer interaction history, improving segmentation accuracy by integrating statistical analysis with machine learning approaches (e.g., logistic regression and XGBoost).
      * **LLM Integration:** Participated in experimental integration of large language models (LLMs) for document analysis and customer query understanding, fine-tuning pre-trained transformer models to extract structured information from policy documents and customer communications.
      * **Data Fusion:** Developed data pipelines to merge tabular data (user demographics, claims history) with textual data (consultation transcripts) using vectorization and contrastive learning, enabling richer feature representation for downstream predictive models.
      * **ETL Automation:** Built automated ETL workflows using Python and SQL for data preprocessing and model input preparation, ensuring data readiness for training and deployment phases.
      * **Model Evaluation:** Assisted in designing and conducting offline evaluation experiments and limited-scope A/B testing to compare predictive performance of updated algorithms in risk assessment tasks.
      * **Team Collaboration:** Worked with product and business teams to identify business pain points, define model requirements, and communicate insights from model outputs to inform strategy and customer outreach initiatives.

* Spring 2023: Intern Algorithm engineer
  * China Life Insurance Co., Ltd.
  * Duties included: As membership of advance algorithm develop team, involved in development of multi-modal alignment algorithm. Employed multi-modal encoder to encode multi-modal information (tabular data and textual data), utilized dot-product and negative likehoods to fuse and optimize them. Thie project achieve state-of-arts performance and be employed in real-world business.
 
* **Summer 2022: Intern Software Engineer**
  * **Wonders Information Co., Ltd.**
  * **Duties included:**
      * **Bug Testing:** Assisted in identifying and fixing frontend-backend integration bugs during Social Security Card Platform testing; wrote unit tests to verify core functionality.
      * **Code Implementation:** Supported junior developers by writing and refining Java code for user login, form validation, and data submission modules.
      * **Data Handling:** Helped maintain and populate MySQL databases for user account data; practiced writing basic SELECT/UPDATE queries for data inspection.
      * **Technical Documentation:** Created and updated technical documentation, including function descriptions and user guides, to support team communication and onboarding.
      * **Team Collaboration:** Attended Agile stand-up meetings and sprint planning sessions, gaining experience in software development workflows.
      

    
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
