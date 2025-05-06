# sakila_pbi


VHS Rental Business Intelligence Dashboard

Contributor: Pavel Nokinov
Project Type: Power BI Dashboard Development

Tools Used: Power BI, DAX, SQL (Sakila Database)

Project Summary
This project presents a comprehensive Power BI solution designed for a VHS rental business using the Sakila database. The objective was to transform operational data into actionable business intelligence through a star-schema model, calculated KPIs, and interactive dashboards. We performed data extraction, transformation, and modeling; created a clean and scalable data warehouse structure; and built two dashboards—one focused on high-level business metrics and another for film-specific insights. This solution supports strategic decision-making in revenue optimization, customer retention, and inventory management.

1. Data Extraction and Modeling
Data was imported directly from the Sakila database using provided credentials. Key tables included: customer, address, city, country, dim_store, film, film_category, category, dim_staff, rental, inventory, payment, and dim_date.
Star Schema Construction
•	fact_rental: Formed by merging rental, inventory, and payment.
•	dim_film: Built by joining film, film_category, and category.
•	dim_customer: Constructed through merges of customer, address, city, and country.
•	Other Dimensions: Included dim_date, dim_store, and dim_staff.

2. Data Transformation
dim_customer Enhancements
•	Formatted text fields (capitalization, concatenation)
•	Created user_name from email addresses
•	Classified income levels: low, medium, high
dim_date Enhancements
•	Filtered date range based on rentals
•	Added an is_weekend flag
fact_rental Enhancements
•	Calculated rental duration (time_rent)
•	Added status flags (Overdue Status, Overdue Days)
•	Generated formatted rental_number values

3. KPI Development
Custom KPIs were developed to track performance across various business areas:
•	Total Revenue: Aggregated rental income
•	Customer Retention Rate: Identified returning vs. new customers
•	Rentals MTD vs Previous Month: Month-over-month comparison
•	Revenue MTD: Current month's revenue progression

4. Dashboards
Main Dashboard
•	Global KPIs with time and category filters
•	Revenue and rental breakdowns by category/title
•	Geographical rental distribution
•	Waterfall chart for revenue trends
Film Dashboard
•	Film-level MTD performance (revenue, rentals)
•	Geo-mapped rental locations
•	Drill-through from the main dashboard for contextual deep dives

Final Results
•	Business Insight: Dashboards enabled stakeholders to monitor performance and drive decisions based on real-time metrics.
•	Model Efficiency: Star schema design supported scalable and accurate time intelligence.
•	UI Design: Visuals were aligned with brand guidelines and included logo integration.

Conclusion
The final Power BI solution meets all business requirements, offering a scalable, maintainable, and insightful dashboard framework. This project exemplifies best practices in data modeling, KPI design, and dashboard usability for operational analytics.
