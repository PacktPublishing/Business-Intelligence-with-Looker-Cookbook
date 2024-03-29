# Joining tables in models 

```
explore: distribution_centers { 
  label: "DC" 
} 
```
```
explore: products { 
  join: distribution_centers { 
    type: left_outer  
    sql_on: ${products.distribution_center_id} = ${distribution_centers.id} ;; 
    relationship: many_to_one 
  } 
} 
```