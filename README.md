# [Q2 2022] Company Sales and Operations Analysis

<p align="right"> <a 
href="https://stackoverflow.com/users/18680621/sam-taylor" target="_blank"><img alt="StackOverflow" 
src="https://stackoverflow-badge.vercel.app/?userID=18680621" /></a> <a 
href="https://github.com/SamTaylor92" target="_blank"><img alt="Github" 
src="https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=GitHub&logoColor=white" /></a> <a 
href="https://www.linkedin.com/in/samjamest" target="_blank"><img alt="LinkedIn" 
src="https://img.shields.io/badge/LinkedIn-0A66C2.svg?style=for-the-badge&logo=LinkedIn&logoColor=white" /></a> <a 
href="https://signal.group/#CjQKIO50NLkjJmSisbgDD4OhRj5lHG7X-SJTOl-Dn8Fkc4FpEhCYdnCVL1ok4DlVNntY3mGe" target="_blank"><img alt="Signal" src="https://img.shields.io/badge/Signal-3A76F0.svg?style=for-the-badge&logo=Signal&logoColor=white"/></a> <a 
href="mailto:samtaylor92@live.co.uk" target="_blank"><img alt="Email" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>
<p align="right">

## Description
An exploratory data analysis of a dataset. <br><br>

The same analysis was conducted in both `Pandas` and `Google Sheets` and the resulting visualisations were added to a `Google Slides` deck.
  
<p align="center">
  <img src="https://user-images.githubusercontent.com/105542266/172668516-4e004148-c709-4239-803b-862e0a433da6.gif" /> </p>

  
<h2> Tools</h2>
<p>
<a target="_blank"><img alt="Jupyter Notebook" src="https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white"/></a> 
<a target="_blank"><img alt="Python" src="https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white"/></a> 
<a target="_blank"><img alt="Pandas" src="https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white"/></a>
<a target="_blank"><img alt="matplotlib" src="https://img.shields.io/badge/matplotlib-13324B.svg?style=for-the-badge&logo=ChartMogul&logoColor=white"/></a>
<a target="_blank"><img alt="seaborn" src="https://img.shields.io/badge/seaborn-1F8ACB.svg?style=for-the-badge&logo=Codeforces&logoColor=white"/></a>
<a target="_blank"><img alt="scipy" src="https://img.shields.io/badge/SciPy-8CAAE6.svg?style=for-the-badge&logo=SciPy&logoColor=white"/></a>
<a target="_blank"><img alt="Google Sheets" src="https://img.shields.io/badge/Google%20Sheets-34A853.svg?style=for-the-badge&logo=Google-Sheets&logoColor=white"/></a>  
</p>

<details open>
<summary> <h2>Table of contents</h2></summary>	

- [Description](#description)
- [Brief](#-brief-)
- [Questions to answer](#-questions-to-answer-)
- [Methodology](#-methodology-)
  - [Data cleaning](#-data-cleaning-)
  - [Data analysis](#-data-analysis-)
- [Results](#-results-)
- [Summary](#-summary-)
- [Recommendations](#-recommendations-)
- [Reference material](#reference-material)
  
</details>

<details open>
  
<summary> <h2> [Brief] </h2> </summary>
You're an Analyst for a new company called Marañón (similar to Amazon), and you've been asked to prepare a presentation for both Sales & Operations that summarizes sales and operations thus far. The summary should include (and the very least) an overview of the company's current state, current customer satisfaction, and proposal for 2-3 areas where the company can improve.<br><br>

__Here are some additional facts:__

- Pretend it is currently Sep-18, so you can ignore all data after this date.
- The company was founded in Jan-17, so you can ignore all data prior to this.
- The company is based in the USA, but it was founded in Brazil.
- You can presume that all orders have been delivered - so ignore the order state field.
- All available data can be downloaded from this link: 
    - https://drive.google.com/drive/folders/16JuqYZIfYKyWCkahQtX9lWtSVji820th?usp=sharing

__Your presentation should:__
- Include no more than 10 slides
- Last no longer than 20 minutes<br>

__Tip:__ Create a structure for answering the questions. If you're not sure what questions to ask, make some up for yourself. It dramatically simplifies the task of digging for data.
<p align='right'><a href="#-tools" target="_blank">⬆</a></p>	

</details>
  
<details open>   
<summary> <h2> [Questions to answer] </h2> </summary> 

To make the analysis more focused, I focused on the following questions:

- Where are the company's customers located?
- How are the company's sales?
- Which products sell best?
- What is the relationship between units sold and delivery cost?
- What percentage of a product's expenses is transportation costs?
- How satisfied are customers?
- Why is there a dip in customer satisfaction (CSAT) in Q4 2017 & Q1 2018?
- What other factors contribute to the negative CSAT?
<p align='right'><a href="#-tools" target="_blank">⬆</a></p>
</details>

</details>
  
<details open>   
<summary> <h2> [Methodology] </h2> </summary> 

<details open>   
<summary> <h3> [Data cleaning] </h3> </summary>  
  
![clean_data](https://user-images.githubusercontent.com/105542266/172595953-fbeeb212-f28b-4bfd-b562-6efbf7206568.gif)

The following was done with the data, so that it was ready to be analysed:
- Joined datasets together
- Renamed columns
- Removed white space
- Changed data types to more appropriate ones
- Dropped columns that were not relevant
- Removed specific rows with several NaN values
- Removed any data that didn't fall between 2017 and 2018
  
  
<p align='right'><a href="#-tools" target="_blank">⬆</a></p>
  
</details>

<details open>   
<summary> <h3> [Data analysis] </h3> </summary>    
  
![analysis](https://user-images.githubusercontent.com/105542266/172583412-9aa30df7-b62f-48ae-bf19-871c3a5240a9.gif)

After cleaning the data, I:
- Combined columns to create relevant metrics/key performance indicators relevant to the dataset:
  - `quarter` from the __[order_purchase_timestamp]__
  - `month` from the __[order_purchase_timestamp]__
  - `percent of NR`: __[payment_value]__ / __[payment_value]__.sum() *100
  - `CSAT`: [__review_score__ > 3, True(100), False(0)]
  - `days_until_delivered`: __[order_delivered_customer_date]__ - __[order_purchase_timestamp]__
  - `actual_delivery_date_minus_estimated_delivery_date`: __[order_delivered_customer_date]__ - __[order_estimated_delivery_date]__
  - `delivery SLA`:  np.where(`actual_delivery_date_minus_estimated_delivery_date` >0, 0,1)
- Correlated data to look for interesting patterns in the data
- Statistically analysed significance of relationships
- Split data into relevant slices, to begin to analyse the questions outlined above
- Visualised the data
  
<p align='right'><a href="#-tools" target="_blank">⬆</a></p>
  
</details>
</details>

<details open>   
<summary> <h2> [Results] </h2> </summary> 

<details open>   
<summary> <h3> [Summary] </h3> </summary>  

- __Company was facing increased demands of sales from 2017, quarter on quarter__
  - (__Source__: Product sales data)

- __The increased demands led to decrease of SLA for on-time deliveries (KPI)__
  - (__Source__: Delivery times)

- __The company outsourced deliveries to cope with demands, reducing overall customer satisfaction (KPI)__
  - (__Source__: Delivery times | CSAT data | Customer review comments)

- __With more logistical overheads, the company worked to improve delivery SLAs (KPI), which raised CSAT (KPI)__
  - (__Source__: Product sales data vs. delivery costs | Delivery % of total sales)

- __Company HQ (USA) ≠ customer base (Brazil) - resulting in higher than industry average delivery costs__
  - (__Source__: Customer map & Product price components)

- __Product range very diverse: issues with delivery and quality of product__
  - (__Source__: CSAT data | Customer review comments)  
  
<p align='right'><a href="#-tools" target="_blank">⬆</a></p>

</details>  
  
<details open>   
<summary> <h3> [Recommendations] </h3> </summary>  

- __Set & maintain SLA for on-time deliveries (suggestion: ~95%)__
  - QTD: (Q3 2018): 92.52%
  - Increase FTEs needed to hit the target
  - Example initiative to improve:
  - A/B test to measure if extending the ‘expected delivery’ by X days increases CSAT and delivery SLA.

- __Set target for CSAT (suggestion: ~85%)__
  - QTD (Q3 2018): 81.51
  - Quality control on ~5% of orders leaving warehouse
    - To reduce ~32% product DSAT driver
  - Work with QAs to categorise negative review comments & work to reduce the main drivers
    - Product issues
    - Logistical issues
    - Etc.

- __Open a warehouse in Brazil (São Paulo)__
  - 100% of customer base in Brazil
  - 42% of customer base in São Paulo
    - Aim: to reduce delivery costs (% of overall order price)

- __Cut products that are not selling & focus on product quality__

- __Investigate the relationship between categories of product, delivery costs, return on investment.__

<p align='right'><a href="#-tools" target="_blank">⬆</a></p>  
  
</details>

<details open>
<summary> <h3>📚[Reference material]</h3> </summary>
  
- [x] [Stack Overflow](https://stackoverflow.com/)

<p align='right'><a href="#-tools" target="_blank">⬆</a></p>	
  
</details>

</details>

