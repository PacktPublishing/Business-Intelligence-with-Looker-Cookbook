# Reusing the lookml code

```
include: "users.view" 

view: users_statistics { 
  extends: [users] 

  measure: count_percent_of_total { 
    label: "Count (Percent of Total)" 
    type: percent_of_total 
    sql: ${count} ;; 
    drill_fields: [detail*] 
  } 

  measure: average_age { 
    type: average 
    value_format_name: decimal_2 
    sql: ${age} ;; 
    drill_fields: [detail*] 
  } 
} 
```
```
view: +distribution_centers { 
  dimension: latitude { 
    hidden: yes 
  } 
} 
```
 