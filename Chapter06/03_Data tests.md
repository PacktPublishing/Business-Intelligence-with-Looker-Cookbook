# Data tests 

```
test: order_id_is_unique {
  explore_source: orders {
    column: order_id {}
    column: count {}
    sorts: [orders.count: desc]
    limit: 1
  }
  assert: order_id_is_unique {
    expression: ${orders.count} = 1 ;;
  }
}
```
```
include: "/data_tests.lkml"
```