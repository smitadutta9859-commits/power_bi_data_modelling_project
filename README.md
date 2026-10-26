## Data Model Architecture

The project uses a multi-table analytical data model in Power BI to support sales reporting, customer analysis, product performance, inventory tracking, campaign analysis, and order-process monitoring.

### Fact Tables

The model includes the following fact or transactional tables:

- `fact_sales` — sales transactions and line-level sales values.
- `fact_sales_targets` — sales revenue targets by date.
- `fact_inventory` — product inventory quantities by month.
- `fact_campaign_spend` — campaign spending, clicks, and impressions.
- `fact_promotion_campaign` — campaign and product associations.
- `fact_order_process` — order-processing dates and order-related information.

### Dimension and Supporting Tables

- `dim_customer` — customer attributes and regional information.
- `dim_product` — product details, categories, brands, suppliers, and prices.
- `dim_date` — date dimension for time-based analysis.
- `dim_loc` — geographic attributes such as city and region.
- `dim_campaign` — campaign details, channels, budgets, and dates.
- `dim_order_flags` — order-channel and order-priority attributes.
- `security` — user email and region mappings for row-level access control.
- `_measures` — dedicated table for organizing DAX measures.

### Modelling Features

- Relationships between sales transactions and descriptive tables.
- Date-based analysis and sales-target comparisons.
- Product, customer, location, inventory, and campaign analysis.
- DAX measures organized in a dedicated measures table.
- Region-based Row-Level Security using user identity and security mappings.

**Model diagram:** See `data-model.

*Note: The `security` and `_measures` tables are supporting tables rather than conventional business dimensions.*
