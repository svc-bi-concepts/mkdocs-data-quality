# Data Governance for Shared Databases

## DBT
- Data Quality Tests: Implement [DQ tests for shared databases](data-quality-tests-shared-databases.md) using [generic DBT tests](data-quality-tests-DBT.md)
- Data Contracts: Enforce contracts all DM models (enforce in project file for DM folder)

## Snowflake Only
- Data Quality Tests: Implement [DQ tests for shared databases](data-quality-tests-shared-databases.md):
    - Not nulls implement as table constraints
    - Other tests implement as [DMF DQ Tests](data-quality-tests-snowflake-only.md) 
- Data Contracts: Currently not directly supported in Snowflake

## Data Quality Tools 
If using dedicated  Data Quality or Governance tools such as Soda or Great Expectations;

- Data Quality Tests: Implement  [DQ tests for shared databases](data-quality-tests-shared-databases.md) using the relevent propiertary method

- Data Contracts can be enforced with a combination of Schema enforcement (column names, types, nullability) and Data Quality Rules (valid ranges, uniqueness, freshness) e.g. [Soda example yaml checks](soda-example-yaml.md)

