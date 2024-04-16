# Creating dimensions in views
```
  dimension: age {
    type: number
    sql: ${TABLE}.age ;;
    drill_fields: [id]
  }
```
```
  dimension: last_name {
    type: string
    sql: ${TABLE}.last_name ;;
    hidden: yes
  }
```
```
  dimension: full_name { 
    type: string 
    sql: ${first_name} || ' , ' || ${last_name};; 
  }
``` 
```
  dimension: age_group { 
    type: tier 
    tiers: [18, 25, 35, 45, 55, 65, 75, 90] 
    sql: ${age} ;; 
    style: classic 
  }
``` 
```
  dimension: delivery_time { 
    type: number 
    sql: DATE_DIFF(${delivered_date}, ${created_date}, day) ;; 
  } 
```
```
  dimension: reporting_period { 
    sql:  
    CASE  
      WHEN EXTRACT(YEAR from ${created_raw}) = EXTRACT(YEAR from CURRENT_TIMESTAMP()) AND ${created_raw} < CURRENT_TIMESTAMP() 
      THEN 'This Year to Date' 
      WHEN EXTRACT(YEAR from ${created_raw}) + 1 = EXTRACT(YEAR from CURRENT_TIMESTAMP()) AND CAST(FORMAT_TIMESTAMP('%j', ${created_raw}) AS INT64) <= CAST(FORMAT_TIMESTAMP('%j', CURRENT_TIMESTAMP()) AS INT64) 
      THEN 'Last Year to Date' 
      END;;
  } 
```
