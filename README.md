# Business Intelligence with Looker Cookbook

<a href="https://www.packtpub.com/product/business-intelligence-with-looker-cookbook/9781800560956?_gl=1*1evex2w*_gcl_au*NzkyOTIxOTY1LjE3MTI3MjM0MTE.*_ga*MTI3MTI1MDc3LjE3MDQ4NzY0MzU.*_ga_Q4R8G7SJDK*MTcxMzc2MzM1My4zNS4xLjE3MTM3NjMzNjMuNTAuMC4w"><img src="https://content.packt.com/_/image/original/B16393/cover_image_large.jpg" alt="no-image" height="256px" align="right"></a>

This is the code repository for [Business Intelligence with Looker Cookbook](https://www.packtpub.com/product/business-intelligence-with-looker-cookbook/9781800560956?_gl=1*1evex2w*_gcl_au*NzkyOTIxOTY1LjE3MTI3MjM0MTE.*_ga*MTI3MTI1MDc3LjE3MDQ4NzY0MzU.*_ga_Q4R8G7SJDK*MTcxMzc2MzM1My4zNS4xLjE3MTM3NjMzNjMuNTAuMC4w), published by Packt.

**Create BI solutions and data applications to explore and share insights in real time**

## What is this book about?
This book will show you how to develop models and create dynamic dashboards using LookML. You’ll explore advanced features to gain deeper insights and make informed decisions.

This book covers the following exciting features:
* Understand Looker's key components, including LookML, data models, and dashboards.
* Explore Looker's functionality, including custom fields, calculations, and visualizations.
* Work with Looker dashboards using dynamic elements like links and actions.
* Use different types of filters for dimensions to create dashboards
* Develop Looker applications using essential tools and frameworks
* Explore additional applications for the Looker organization
* Integrate Looker with other tools using APIs, connectors, and data pipelines

If you feel this book is for you, get your [copy](https://www.amazon.com/Business-Intelligence-Looker-Cookbook-applications/dp/1800560958/ref=sr_1_1?crid=3U5TWY9FRN6Z0&dib=eyJ2IjoiMSJ9.2tSCjxDy7Qj49z44v5BTjpTwYqrO9KbP9xNndAwH67s6C0IfrJ61J1pkjoI9kHOq2K1ltXFZafRQQGRvx4wcTK3Pew1T4laTHxuvQskEqvk.EjAgnue0G8Fj1BQ02kv0xLSqAUYUYnA2xGvsF-g8loY&dib_tag=se&keywords=Business+Intelligence+with+Looker+Cookbook&qid=1713763503&sprefix=business+intelligence+with+looker+cookbook%2Caps%2C347&sr=8-1) today!
<a href="https://www.packtpub.com/?utm_source=github&utm_medium=banner&utm_campaign=GitHubBanner"><img src="https://raw.githubusercontent.com/PacktPublishing/GitHub/master/GitHub.png" 
alt="https://www.packtpub.com/" border="5" /></a>
## Instructions and Navigations
All of the code is organized into folders. For example, Chapter02.

The code will look like the following:
```
  dimension: age_group {
    type: tier
    tiers: [18, 25, 35, 45, 55, 65, 75, 90]
    sql: ${age} ;;
    style: classic
  }
```

**Following is what you need for this book:**
If you’re a business analyst, data analyst, or BI developer who wants to get well-versed with the features of Looker, this book is for you. Basic knowledge of business intelligence is required to get started.

Here's everything you need to run all the steps and code files in the book (Chapter 1-10).
## Software and Hardware List
| Chapter | Software required | OS required |
| -------- | ------------------------------------ | ----------------------------------- |
| 1-10 | Google Cloud Account| Any OS with a modern web browser |
| 1-10 | Looker | Any OS with a modern web browser  |

You’ll need a Google account to access Google Cloud and request a Looker trial instance. We’ll guide you through the setup process in Chapter 1. To access Looker, you don’t need to install anything; a web browser is enough.

## Related products
* Database Design and Modeling with Google Cloud [[Packt]](https://www.packtpub.com/product/database-design-and-modeling-with-google-cloud/9781804611456?_gl=1*1r2n5l5*_gcl_au*NzkyOTIxOTY1LjE3MTI3MjM0MTE.*_ga*MTI3MTI1MDc3LjE3MDQ4NzY0MzU.*_ga_Q4R8G7SJDK*MTcxMzc2MzM1My4zNS4xLjE3MTM3NjM5MTcuNTYuMC4w) [[Amazon]](https://www.amazon.com/Database-Design-Modeling-Google-Cloud/dp/180461145X/ref=sr_1_2_sspa?crid=1O8HYVYK1EQHY&dib=eyJ2IjoiMSJ9.dkvid_RArjLhIOhdSOQtE2yglJ8Gz74kmbTTGs4KXxTfB6_gKjqTal92gKvdM5R9KgvLRU03HehzxNwIHPNhLJncC34G9QKcf4AYcBXrDwIurUTIIlXup0LKtxiKY9k6Rnq1Ew5zEF1ZxhdPY0MbqWxbxhv2zYUrSKAS3pZzb4tRLSjLbKV68RmI2HtsJzqiHh_P-pokbQfHij6wZYlX6qrs4HPfWX9Ke5-0nV768zQ.cf3NKiRuquxqy69axc5hkC8H1ygBCPPUPms4xbsGxj8&dib_tag=se&keywords=Database+Design+and+Modeling+with+Google+Cloud&qid=1713763921&sprefix=database+design+and+modeling+with+google+cloud%2Caps%2C576&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)

* Data Engineering with Google Cloud Platform [[Packt]](https://www.packtpub.com/product/data-engineering-with-google-cloud-platform/9781800561328?_gl=1*1hp45go*_gcl_au*NzkyOTIxOTY1LjE3MTI3MjM0MTE.*_ga*MTI3MTI1MDc3LjE3MDQ4NzY0MzU.*_ga_Q4R8G7SJDK*MTcxMzc2MzM1My4zNS4xLjE3MTM3NjM5OTguNTcuMC4w) [[Amazon]](https://www.amazon.com/Data-Engineering-Google-Cloud-Platform/dp/1800561326/ref=sr_1_1?crid=2S4POSTVKNLKN&dib=eyJ2IjoiMSJ9.QeSNIxV0ltAKZVJSFikBFZD55LL-k3XIKieXkX1KWsm5OWt6EPR7QQ_1UN22ruBTGfvIkYUO-um6X38Dhf5Pk2Ga1Csu01eAqq78HdUzuDUSGif01U9hT3X6m4HIHhtkg8bOSVjU4ufD2muEIS6KVpK2sxEwe1vIlG5eHpmtKGxG-Nq4O97EO2qLK67XffC7p-tSLPwDSdQ3k_fXOYhmaT_PlnUDfwUQM4QoiiDDVZs.RS2VrsA0h2bbjXli1wMUrvXn76aPBtF9LvpcgQ1-Nko&dib_tag=se&keywords=Data+Engineering+with+Google+Cloud+Platform&qid=1713763989&sprefix=data+engineering+with+google+cloud+platform%2Caps%2C327&sr=8-1)

* Data Storytelling with Google Looker Studio [[Packt]](https://www.packtpub.com/product/data-storytelling-with-google-looker-studio/9781800568761?_gl=1*clls9x*_gcl_au*NzkyOTIxOTY1LjE3MTI3MjM0MTE.*_ga*MTI3MTI1MDc3LjE3MDQ4NzY0MzU.*_ga_Q4R8G7SJDK*MTcxMzc2MzM1My4zNS4xLjE3MTM3NjQwNjcuNTcuMC4w) [[Amazon]](https://www.amazon.com/Storytelling-Google-Looker-Studio-hands/dp/1800568762/ref=sr_1_1?crid=3S7NMQ7GD5SBB&dib=eyJ2IjoiMSJ9.FACTluHI3PnF3Ucf2ol0WExoF3kVScZB6ex925Eynh1k40EKonq9f-YWgXikSyXj3qxE7yjygxF2dKzvXftmO5rw4V_NT-RaEvoZc2hnrUEqZ3WQZmSOX4vB0CPUQhp9cEFQ3jJgU7rfrbsvJ5ewKXn2ZjbMVnp8NE75HKGED9mGdJrwk2v_Fvvou5LdJntYTv9KakbIUyOovu43k1Sd2a6RjIsXLnRaspCTx1NwYGw.gl7yRV6jTKlIqKRNNCQeuy6vCk4msmCu3-mgych8_VU&dib_tag=se&keywords=Data+Storytelling+with+Google+Looker+Studio&qid=1713764071&sprefix=data+storytelling+with+google+looker+studio%2Caps%2C310&sr=8-1)

## Get to Know the Author
**Khrystyna**
 is a data analyst and Looker expert with over a decade of experience in the field. With a passion for empowering businesses through data-driven decisions, Khrystyna transitioned from her early career in digital marketing to specialize in data analysis. Graduating from Lumiere University Lyon 2 with a Master's degree in Business Intelligence, she honed her skills by working with various companies, leveraging data to tackle real-world challenges and drive strategic growth. Recognized as a thought leader in the industry, Khrystyna is a sought-after speaker at industry events and has authored numerous articles on data analytics and Looker. Beyond her professional endeavours, she dedicates her time to mentoring and coaching aspiring data professionals, sharing her expertise and insights to foster growth and innovation in the field.

