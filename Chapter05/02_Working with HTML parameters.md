# Working with HTML parameters 

```
  dimension: status { 
    type: string 
    sql: ${TABLE}.status ;; 
    html: {% if value == 'Complete' %} 
    <p style="color: black; background-color: lightblue; font-size:100%; text-align:center">{{ rendered_value }}</p> 
    {% elsif value == 'Shipped' %} 
    <p style="color: black; background-color: lightgreen; font-size:100%; text-align:center">{{ rendered_value }}</p> 
    {% else %} 
    <p style="color: black; background-color: orange; font-size:100%; text-align:center">{{ rendered_value }}</p> 
    {% endif %} 
    ;; 
  }
```
```
html:<p><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Emblem-earth.svg/1024px-Emblem-earth.svg.png" alt="" height="20" width="20">{{ rendered_value }}</p>;;
```
