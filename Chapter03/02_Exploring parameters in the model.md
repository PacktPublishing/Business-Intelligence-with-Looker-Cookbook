# Exploring parameters in the model 

```
explore: orders_and_users {
  view_name: orders
  sql_always_where: ${orders.created_year}>2021 ;;
  join: users {
    type: left_outer
    sql_on: ${orders.user_id} = ${users.id} ;;
    relationship: many_to_one
  }
}
```
```
explore: orders_and_users {
  view_name: orders
  sql_always_where: ${orders.created_year}>2021 ;;
  sql_always_having: ${orders.count}>3 ;;
  join: users {
    type: left_outer
    sql_on: ${orders.user_id} = ${users.id} ;;
    relationship: many_to_one
  }
}
```
```
  always_filter: {
    filters: [
      users.country: "United States"
    ]
  }
```
```
  conditionally_filter: {
    filters: [orders.created_month: "1 month"]
    unless: [users.id]
  }
```