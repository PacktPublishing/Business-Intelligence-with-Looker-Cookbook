# Adding advanced model parameters 

```
label: "Our Company Ecommerce Data Model"
```
```
week_start_day: monday
```
```
named_value_format: percent_with_no_decimals { 
  value_format: "0\%"  
}
```
```
  measure: sold_percent { 
    type: number 
    value_format_name: percent_with_no_decimals 
    sql: 1.0 * ${sold_count}/(CASE WHEN ${count} = 0 THEN NULL ELSE ${count} END) ;; 
  }
```