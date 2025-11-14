# DAX Measures Used in Power BI

Below are all the DAX measures created for the Task 2 dashboard.

---

## Total Metrics

### Total Impressions
```DAX
Total Impressions = SUM('cleaned-data-facebook'[impressions])
```
### Total CLicks
```DAX
Total Clicks = SUM('cleaned-data-facebook'[clicks])
```
### Total Spend
```DAX
Total Spend = SUM('cleaned-data-facebook'[spent])
```
### Total Conversations
```DAX
Total Conversions = SUM('cleaned-data-facebook'[approved_conversion])
```

## Performance KPIs

### CTR (%)
```DAX
CTR (%) =
DIVIDE(
    [Total Clicks],
    [Total Impressions],
    0
)
```
### CPC (Cost Per Click)
```DAX
CPC =
DIVIDE(
    [Total Spend],
    [Total Clicks],
    0
)
```

### CPA (Cost Per Acquisition)
```DAX
CPA =
DIVIDE(
    [Total Spend],
    [Total Conversions],
    0
)
```

### CPM (Cost Per 1000 Impressions)
```DAX
CPM =
DIVIDE(
    [Total Spend],
    [Total Impressions],
    0
) * 1000
```
