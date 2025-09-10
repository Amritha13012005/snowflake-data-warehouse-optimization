Snowflake Data Warehouse Optimization

Overview
Hands-on mini-project using Snowflake Cloud Data Platform. The goal was to create a dataset, build an aggregated table, optimize queries using clustering, create a materialized view, and demonstrate basic RBAC concepts.

Project Structure
- Project.sql — contains all SQL scripts for warehouse, database/schema, table creation, clustering, and materialized view..
- README.md — project description and instructions.
- screenshots/ — optional folder for query and output screenshots.

Steps Performed
1. Warehouse Setup
   Created a small compute warehouse (WH_XS) with auto-suspend/resume.

2. Database & Schema
   Created database DEMO_DB and used PUBLIC schema.

3. Synthetic Data Table
   Created table EVENTS_RAW with 100,000 rows.
   Columns: id, event_time, user_id, event_type, value, country.

4. Baseline Query
   Ran daily counts by country to check performance.

5. Aggregated Table
   Created EVENTS_DAILY with event_date, country, event_type, cnt, and avg_value for faster analytics.

6. Clustering Optimization
   Applied CLUSTER BY(event_time) on EVENTS_RAW to reduce bytes scanned.

7. Materialized View
   Created MV_EVENTS_DAILY for faster repeated aggregation queries.

8. RBAC Concepts
   Demonstrated role-based access using default Snowflake roles (SYSADMIN, PUBLIC).

Outcome
- Optimized queries for large datasets.
- Learned Snowflake data modeling, clustering, materialized views, and access control basics.
- Entire project completed on Snowflake Trial Account.
