# Soda Example YAML Checks

```yaml
checks for dim_customers:
  # Schema Contract
  - schema:
      name: Enforce contract schema
      warn:
        when required column missing: [customer_id, name, email]
        when wrong column type:
          customer_id: integer
          email: varchar
  # Data Quality Contract
  - missing_count(email) = 0:
      name: Emails must never be null
  - invalid_percent(email) < 1%:
      name: Emails must be valid (regex)
      valid regex: '^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'
  - freshness(updated_at) < 1d:
      name: Data must be updated daily
```

