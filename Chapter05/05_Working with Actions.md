# Working with Actions  

```
  dimension: actions { 
    group_label: "Actions" 
    description: "Various actions you can take on anomalies" 
    sql: "Actions..." ;; 
    action: { 
      label: "Email Data Quality Team" 
      url: "https://hooks.zapier.com/hooks/catch/(replace_by_your_code)/(replace_by_your_code)/" #add you webhook URL here 
      icon_url: "http://www.google.com/s2/favicons?domain=www.gmail.com" 

      form_param: { 
        name: "Message" 
        type: textarea 
        default: "Hey, Could you check out this data anomaly. It occurred for the Order {{ order_id._rendered_value}}." 
      } 

      form_param: { 
        name: "Recipient" 
        type: select 
        default: "James" 
        option: { 
          name: "james" 
          label: "James" 
        } 
        option: { 
          name: "bob" 
          label: "Bob" 
        } 
      } 
    } 
  }