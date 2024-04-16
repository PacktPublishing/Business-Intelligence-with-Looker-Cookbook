# Working with Liquid parameters in labels

```
label: "{{ _explore._name}}: Count"
```
```
  dimension: name {
    label: "{% if _user_attributes['company'] == 'Looker' %} Employee Name {% else %} Customer Name {% endif %}"
    sql: ${TABLE}.name ;;
  }
```