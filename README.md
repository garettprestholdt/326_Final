# Twin Cities Water Quality & Property Value Analysis

**Objective:** Analyze the correlation between residential property pricing and local water quality in the Twin Cities using a **~10GB dataset** of 1.5 million records.

**Built With:** Python, **Polars (LazyFrames)**, Parquet Partitioning, Scikit-Learn (CART, Random Forest).

### Data Sources
* **MetroGIS Tax Parcels:** 1.5M records (2002–2015) including valuation and dwelling type.
* **Met Council Lake Data:** Historical quality metrics (Secchi depth, Phosphorus) for 332 lakes.
* **Spatial Cross-Reference:** Distance calculations between parcels and monitoring stations.

### Workflow
* **Lab 1: Ingestion:** Handled raw ingestion of 13 years of tax data and spatial files.
* **Lab 2: Integration:** Designed logic to join tax records with water monitoring stations using spatial keys.
* **Lab 3: Optimization:** Converted CSVs to **partitioned Parquet files**, enabling efficient lazy querying on large-scale data.
* **Lab 4: Processing:** Aggregated granular water quality metrics (e.g., Seasonal Grade) for modeling.
* **Lab 5: Feature Engineering:** Selected predictors from property attributes (ownership, dwelling type) and lake proximity.
* **Lab 6: Modeling:** Trained and validated **CART** and **Random Forest** models to predict property value impacts.

