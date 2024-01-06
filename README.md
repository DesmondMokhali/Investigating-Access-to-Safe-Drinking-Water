# Project Overview 
## Investigating Access to Safe Drinking Water

This project investigates access to safe and affordable drinking water, focusing on inequalities in service levels between different countries and regions. It analyses data from the WHO/UNICEF Joint Monitoring Programme (JMP) to answer questions regarding inequalities in access to safe drinking water.

![191121-water-crisis-report-main-kh](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/651c76c8-3705-4729-8ec1-883299a201d4)


## Key Points:

- **Data:** WHO/UNICEF JMP data on access to drinking water (2000-2020)
- **Focus:** Inequalities in access to safe drinking water across countries and regions
- **Analysis:**

### Part 1:
- Comparing world population estimates with JMP data to understand the bigger picture.
- Analysing the distribution of urban vs. rural populations.
- Identifying trends and patterns in water access across different regions.
- Comparing access measures across various types of areas.
- Analysing national, urban, and rural access to water based on population size.
- Investigating the impact of population size and urbanization on income and water access.

### Part 2:
- Comparing the imported dataset with JMP data to ensure consistency.
- Identifying the years represented in the data and calculating the average year difference per country.
- Calculating the Annual Rates Change (ARC) for national, rural, and urban areas.
- Analysing changes in access to basic water over time for different areas.
- Comparing ARCs between rural and urban populations and across different regions.
- Investigating how national population size influences the ARC.

## Project Goals:

- Gain insights into global access to safe drinking water.
- Identify inequalities in access between countries and regions.
- Analyse trends and changes in access over time.
- Contribute to achieving the Sustainable Development Goal (SDG) 6: Clean water and sanitation for all.
  
![image](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/7e52eb0b-7469-4d14-8519-07c69bf1d701)

Figure 1: UNITED NATIONS SDGs

## Target Audience:

- Data scientists
- Public health professionals
- Policymakers
- Anyone interested in global development and water sustainability

  Findings
  ## Part 1

### 1 Comparing world population estimates with JMP data to understand the bigger picture.  
Here, we calculated the total national population using the pop_n feature (in thousands) and converted it to billions for comparison with the estimated global population:   
  
**Estimated Global Population (billion)** = `7.821 billion`   
   
**Total Global Population (billion)** = `SUM (pop_n) / 1000000`  
                                  = `SUM ('Estimates on the use of water (2020)’! C2:C214)/1000000`  
                                  = `7.786695108`  

                                    
  This ensures consistent unit representation for accurate analysis.  
    
### 2. Analysing the distribution of urban vs. rural populations.
delved deeper into data and calculated the Total urban population, the Estimated urban share, Total urban share, Difference in the estimated and the Global population, estimated and Urban population,and estimated and Urban share.  
  
![image](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/12029751-288d-45c8-8920-5f460ad2d511)

  Used a line chart to analyse the share of national populations living in urban versus rural areas with a visualization  
  
  ![National population versus urban and rural share 2020](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/886d842d-542f-4554-a5ed-4440dd8c041c)



### 3 Identifying trends and patterns in water access across different regions.
This section delves into analysing national access to different water service levels (basic, limited, etc.) using both descriptive statistics and visualizations.

**Descriptive Statistics:** We calculate various descriptive statistics for each service level percentage:  
  
![Central tendency](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/1081d77f-00c3-4542-8900-b5d2e07c3cd6)

We then created a box and whisker diagrams for each service level percentage, utilizing Google Sheets' candlestick chart functionality to construct 12 box and whisker plots, one for each feature-area combination.

![Access to water](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/e8cb0ad3-3889-42e0-bd72-fd9bea641742)


### National vs. Urban vs. Rural:  
 + Basic water access (`_wat_bas`) is the most prevalent type of access in all three areas, but it is the highest in urban areas (**around 98%**) and lowest in rural areas (**around 72%**).  
 + Limited water access (`_wat_lim`) is most common in rural areas (**around 23%**) and least common in urban areas (**around 1%**).  
 + Unimproved water access (`_wat_unimp`) is highest in rural areas (**around 4%**) and essentially non-existent in urban areas.  
 + Surface water access (`_wat_sur`) is relatively low in all three areas, but it is slightly higher in rural areas (**around 1%**) compared to national and urban areas (**around 0.5%**).    
  

### Distribution of data within each area:
 + The boxes for basic water access in all three areas are relatively narrow, indicating that the data is clustered around the median. This suggests that there is not a lot of variability in basic water access within each area.
 + The boxes for limited water access and unimproved water access are wider, especially in rural areas. This indicates that there is more variability in these levels of access, with some areas having much higher or lower levels than others.
 + There are a few outliers in the plots, particularly for limited water access and unimproved water access in rural areas. These outliers represent areas with significantly higher or lower levels of access than the majority of the population


### 4. Analysing national, urban, and rural access to water based on population size.    
  
  This section explores how national, urban, and rural population sizes influence access to different water service levels through 100% stacked bar charts.  
    
  **Independent Variable:**  
  National population size `pop_n` for national analysis, urban population size `pop_u_val` for urban analysis, and rural population size `pop_r` for rural analysis.  
    
**Dependent Variables:**   
Percentage access levels for each service category:
•	`wat_bas_x_`: Basic access
•	`wat_lim_x_`: Limited access
•	`wat_unimp_x_`: Unimproved access
•	`wat_sur_x_`: Surface water

1.	National Population Size Impact:
   
![National distribution of access to water per service level](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/f2417835-8214-4197-8a73-54f9341c45f0)

2.	Urban Population Size Impact:  

  ![Urban distribution of access to water per service level](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/21eef37e-8a06-49a2-881f-dc0243114c46)

  3.	Rural Population Size Impact:  

   ![Rural distribution of access to water per service level](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/ce59cac0-c955-4520-9690-ff5c62fd5dca)

### 5.  Investigating Access by Income Group
This section delves into exploring the relationship between income groups and access to water services.  

#### a) Summarizing Dataset by Income Group:  
##### 1.	Pivot Table:  
   + Create a pivot table to summarize the data by income group `income_group`.
   + Set rows to `income_group`.   
##### o	Set values to:
  + Sum of population size `pop_n`.
  + Average urban share `pop_u`.
    
•	Average national share of each access level: `wat_bas_n`, `wat_lim_n`, `wat_unimp_n`, and `wat_sur_n`.

##### 2.	Visualization:    
o	**Sorting the X-Axis:** To enhance analysis, convert the text `income_group` column to numerical values:  
 + NaN becomes 0.  
 + "Low income" becomes 1.  
 + "Lower middle income" becomes 2.  
 +	"Upper middle income" becomes 3.  
 +	"High income" becomes 4.  

  ![PIVOT](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/72116506-e5f1-479c-99db-6fe4c294f212)



