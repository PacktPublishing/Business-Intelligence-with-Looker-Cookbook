# Connecting to data in Looker

```
SELECT 
PARSE_DATE("%Y%m%d",event_date) as Session_Date, 
device.category AS Device_category, 
COUNT(*) AS Nb_of_sessions 
FROM `bigquery-public-data.ga4_obfuscated_sample_ecommerce.events_202101*` 
WHERE event_name = 'session_start' 
GROUP BY 1,2 
ORDER BY 1,2 ASC; 
```