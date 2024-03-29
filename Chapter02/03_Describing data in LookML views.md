# Describing data in LookML views 

```
  measure: total_gross_margin_percentage {
    label: "Gross Margin %"
    group_label: "Revenue section"
    description: "A KPI that shows the percentage of the gross margin"
    type: number
    value_format_name: percent_2
    sql: 1.0 * ${total_gross_margin}/ nullif(${total_sale_price},0) ;;
    tags: ["sales", "orders", "revenue"]
  }
```
```
  measure: average_sale_price {
    group_label: "Revenue section"
    order_by_field: total_gross_margin_percentage
    # group_item_label: "Price"
    type: average
    value_format:"$#.0;($#.0)"
    sql: ${sale_price} ;;
  }
```