# Working with filters in LookML views 

```
  dimension: is_sold { 
    type: yesno 
    sql: ${sold_raw} is not null ;; 
  } 
```
```
  measure: sold_count { 
    type: count 
    filters: { 
      field: is_sold 
      value: "Yes" 
    } 
  } 
```
```
  measure: sold_percent { 
    type: number 
    value_format_name: percent_2 
    sql: 1.0 * ${sold_count}/(CASE WHEN ${count} = 0 THEN NULL ELSE ${count} END) ;; 
  }
``` 
```
view: view_name { 
  measure: field_name { 
    filters: [dimension_name: "filter expression", dimension_name: "filter expression", ... ] 
  } 
} 
```