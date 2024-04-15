# Creating measures in views 

```
  measure: total_latitude { 
    type: sum 
    sql: ${latitude} ;; 
  } 

  measure: average_latitude { 
    type: average 
    sql: ${latitude} ;;  
  }
``` 
```
  measure: total_num_of_item { 
    type: sum 
    sql: ${num_of_item} ;;
  } 
```
```
  dimension: delivery_time { 
    type: number 
    sql: DATE_DIFF(${delivered_date}, ${created_date}, day) ;; 
  } 
```
```
  measure: average_days_to_process { 
    type: average 
    value_format_name: decimal_1 
    sql: ${delivery_time} ;; 
  } 
```
```
  dimension: gross_margin { 
    type: number 
    value_format_name: usd 
    sql: ${sale_price} - ${inventory_items.cost} ;; 
  } 
```
```
  measure: total_gross_margin { 
    type: sum 
    value_format_name: usd 
    sql: ${gross_margin} ;; 
    drill_fields: [detail*] 
  } 
```
```
  measure: total_gross_margin_percentage { 
    type: number 
    value_format_name: percent_2 
    sql: 1.0 * ${total_gross_margin}/ nullif(${total_sale_price},0) ;; 
  }
``` 
