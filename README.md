 PhonePe Transaction Insights Dashboard

 Overview

The PhonePe Transaction Insights Dashboard is an interactive web-based analytics platform built with Streamlit and PostgreSQL. It provides detailed visualizations and insights based on PhonePe transaction, user, and insurance data. The dashboard supports multiple business case studies with SQL query integration and dynamic visualizations.



 Features

The dashboard includes analysis for five business cases:

1. User Registration Analysis

    Tracks user registration growth trends.
    Identifies states with highest and lowest registrations.
    Analyzes registration share by region.
    Provides time-based registration trends.
    Displays geographic registration distribution.

2. User Engagement & Growth Strategy

    Analyzes active user patterns.
    Examines engagement by state.
    Identifies potential growth regions.
    Measures retention trends.
    Compares user activity across time periods.

3. Decoding Transaction Dynamics

    Analyzes total transaction volumes and amounts.
    Identifies top-performing states by transaction value.
    Shows seasonal transaction patterns.
    Compares year-on-year transaction growth.
    Highlights state-level transaction rankings.

4. Device Dominance and User Engagement

    Tracks usage by device type.
    Identifies device preferences across regions.
    Compares engagement between device categories.
    Analyzes correlation between device usage and transaction activity.
    Monitors device trend changes over time.

5. Insurance Penetration & Growth Potential

    Measures insurance penetration by state.
    Identifies states with highest insurance adoption.
    Analyzes insurance transaction volumes.
    Shows insurance growth trends.
    Highlights under-penetrated markets.



 Technology Stack

 Programming Language: Python
 Framework: Streamlit
 Database: PostgreSQL
 ORM: SQLAlchemy
 Visualization: Plotly
 Data Source: Processed PhonePe transaction, user, and insurance datasets stored in PostgreSQL.



 Installation

1. Clone the Repository


   git clone <repository_url>
   cd <repository_name>


2. Create and Activate Virtual Environment


   python -m venv env
   env\Scripts\activate    On Windows
   source env/bin/activate  On Mac/Linux


3. Install Dependencies


   pip install -r requirements.txt


4. Set Up PostgreSQL Database

    Create a PostgreSQL database.
    Import the provided dataset tables (`agg_user_data`, `agg_transaction_data`, `agg_insurance_data`, `map_us_df`, `map_trans_df`, `map_insurance_data`, `map_inscountry_df`, `top_user_df`, `top_transaction_df`, `top_insurance_data`).
    Update the connection string in `app.py`:

  python
     engine = create_engine("postgresql+psycopg2://<username>:<password>@localhost/<database_name>")
  

5. Run the Streamlit Application


   streamlit run app.py




 Folder Structure


project_root/
│
├── app.py                 Main Streamlit application
├── requirements.txt       Python dependencies
├── data/                  (Optional) Raw/processed datasets
└── README.md              Project documentation




 Solution Approach

 Data is pre-processed and stored in PostgreSQL.
 SQLAlchemy is used for database interaction.
 Each business case contains five predefined SQL queries.
 Query results are visualized using Plotly charts.
 Streamlit provides dropdown-based selection for business cases.
 Each visualization includes:

   Chart output
   Expandable raw data table
 Layout is optimized for two-column display with a consistent style.



 Author

Name: Sudharsan Udhayakumar
Role: Data Scientist| Data Analyst | Streamlit Dashboard Developer
email:ssudhar525@gmail.com
