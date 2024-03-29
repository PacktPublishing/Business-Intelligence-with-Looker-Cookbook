# Working with geodata in lookml 

```
view: users_france { 
  derived_table: { 
    sql: 
    SELECT * 
    FROM users 
    WHERE country = "France" 
    ;; 
  } 
```
```
explore: users_france {} 
```
```
map_layer: communes {
  file: "/communes.topojson" 
  format: topojson 
} 
```
```
  dimension: city { 
    type: string
    sql: ${TABLE}.city ;; 
    map_layer_name: communes 
  } 
```
```
  dimension: dc_location { 
    type: location 
    sql_latitude: ${TABLE}.latitude ;; 
    sql_longitude: ${TABLE}.longitude ;; 
  } 
```
```
  dimension: users_location { 
    type: location 
    sql_latitude: ${TABLE}.latitude ;; 
    sql_longitude: ${TABLE}.longitude ;; 
  } 
```
```
  dimension: distance_to_DCs { 
    type: distance 
    start_location_field: distribution_centers.dc_location 
    end_location_field: users_location 
    units: kilometers 
  } 
```