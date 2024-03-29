# Working with dynamic SQL

```
view: view_name {
  parameter: parameter_name { ... }
}
```
```
  parameter: break_down_by_date {
    type: unquoted
    allowed_value: {
      label: "Break down by Day"
      value: "day"
    }
    allowed_value: {
      label: "Break down by Month"
      value: "month"
    }
    allowed_value: {
      label: "Break down by Year"
      value: "year"
    }
  }
```
```
  dimension: date {
    sql:
      {% if break_down_by_date._parameter_value == 'day' %}
        ${created_date}
      {% elsif break_down_by_date._parameter_value == 'month' %}
        ${created_month}
      {% elsif break_down_by_date._parameter_value == 'year' %}
        ${created_year}
      {% else %}
        ${created_date}
      {% endif %};;
  }
```
```
  dimension: salary {
    type: number
    hidden: yes
    sql: ${TABLE}.user_id ;;
  }

  dimension: salary_display {
    sql:
      {% if _user_attributes['HR'] == 'yes' %}
        ${salary}
      {% else %}
        "Salary Hidden"
      {% endif %} ;;
  }
```
