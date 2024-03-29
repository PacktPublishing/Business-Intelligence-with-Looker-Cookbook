# Working with links

```
link: { 
  label: "Google Search" 
  url: "http://www.google.com/search?q={{ value }}" 
  icon_url: "http://google.com/favicon.ico" 
} 
```
```
  always_filter: { 
    filters: [ 
      users.country: "United States" 
    ] 
  } 

  conditionally_filter: { 
    filters: [orders.created_month: "1 month"] 
    unless: [users.id]
  }
```
```
  link: { 
    label: "{{value}} Analytics Dashboard" 
    #url: "/dashboards/1925?Country={{ _filters['users.country'] | url_encode }}" 
    url: "/dashboards/1925?Country={{ value | encode_uri }}" 
  }
```
```
  link: {
    label: "{{value}} Analytics Dashboard"
    url: "/dashboards/1925?Country={{_filters['users.country'] | url_encode }}"
  }
```
