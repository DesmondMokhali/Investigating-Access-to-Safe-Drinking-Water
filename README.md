# Project Overview 
## Investigating Access to Safe Drinking Water

This project investigates access to safe and affordable drinking water, focusing on inequalities in service levels between different countries and regions. It analyses data from the WHO/UNICEF Joint Monitoring Programme (JMP) to answer questions regarding inequalities in access to safe drinking water (2000 -2020).

![191121-water-crisis-report-main-kh](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/651c76c8-3705-4729-8ec1-883299a201d4)

[Nhung Le](https://www.nbcnews.com/news/latino/when-it-comes-access-clean-water-race-still-strongest-determinant-n1089606)
## Key Points:

- **Data:** WHO/UNICEF JMP data on access to drinking water (2000-2020)
- **Focus:** Inequalities in access to safe drinking water across countries and regions
- **Analysis:**

### Part 1:
- Comparing world population estimates with JMP on the use of water (2020) data to understand the bigger picture.
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

[United Nations SDGs](https://www.globalgoals.org/goals/)

## Target Audience:

- Data scientists
- Public health professionals
- Policymakers
- Anyone interested in global development and water sustainability

 ## Observations:  

+  The analysis provides actionable insights into the water crisis in Sub-Saharan Africa. Despite some progress, the region is projected to achieve full access to water only by approximately **2080** at the current rate of change.
+  This information forms the basis for a compelling narrative about the urgent need for intervention in Sub-Saharan Africa to address the water crisis. Without significant efforts, millions of Africans will continue to face a scarcity of clean water for the next **~60 years**. This narrative underscores the importance of targeted interventions and policy measures to improve water access in the region.


     
  ## Part 1

### 1. Comparing world population estimates with JMP data to understand the bigger picture.    
  
Here, we calculated the total national population using the `pop_n` feature (in thousands) and converted it to billions for comparison with the estimated global population:   
  
**Estimated Global Population (billion)** = `7.821 billion`   
   
**Total Global Population (billion)** = `SUM (pop_n) / 1000000`  
                                  = `SUM ('Estimates on the use of water (2020)’! C2:C214)/1000000`  
                                  = `7.786695108`  
![Tot glob pop](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/9e24e8b0-5692-4d6d-95ae-6a95e0dfb24e)

                                    
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
  +	`wat_bas_x_`: Basic access  
  +	`wat_lim_x_`: Limited access  
  +	`wat_unimp_x_`: Unimproved access  
  +	`wat_sur_x_`: Surface water  

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
  +      NaN becomes 0.  
  +      Low income" becomes 1.  
  +      Lower middle income" becomes 2.  
  +      Upper middle income" becomes 3.  
  +      High income" becomes 4.  

  ![PIVOT](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/72116506-e5f1-479c-99db-6fe4c294f212)

---
### Part 2: Transforming the Data  
  

### 1. Becoming Familiar with the Dataset  
  
   a) To gain further insights, we extended our examination to the **World Health Organization (WHO)/United Nations Children's Fund (UNICEF) Joint Monitoring Programme (JMP) Estimates** on the Use of Water dataset. This dataset spans from the year **2000** to **2020**, broadening the **temporal scope** of our analysis.  
   b) We imported the dataset titled **"Estimates on the Use of Water (2000-2020).csv"** to discern any variations from the dataset used in the preliminary phase of the project.  
   c) Upon reviewing the column names, a notable alteration was identified: the removal of the `income_group` feature and the addition of a `year` feature.  
 
### 2. Investigating Year Representation   

### 1.	Determining the Years Recorded: 
   + To understand the temporal scope of our dataset, we first investigate the years during which data were recorded.  
   +	To observe the representation of years for each country, we employ a meticulous sorting method. This involves freezing the header row to maintain context and using the **Data > Sort range > Advanced range sort** options to sort by `country name` (Column A) and then by `year` (Column B).  

![image](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/725a84df-625b-45d0-8034-ec4e1bf6d478)





### 3.	Identifying Data Collection Frequency:  
  +	A preliminary assessment reveals that data entries were not recorded for every year in each country. To account for this variability when examining temporal trends, we must determine if data were collected only twice per country.  
### 1. Calculating Average Year Difference 
  + In the dataset sheet, a new column named `y_diff` (year difference) is introduced to calculate the difference in years between consecutive entries for each country.    
  + An if statement is implemented to subtract the second year from the first year only if the country name matches between consecutive rows. This ensures that the y_diff is calculated only for entries pertaining to the same country.    

![y_dif_flow](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/762891d7-6ad1-49a4-a783-01611b4b2a80)  ![y_dif_pseudo](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/74457b08-00a8-496b-8aa1-c621774a1a49)




If Statement   
Y_diff    
+          `= IF(A3=A2,B3-B2,"")`  
  
### 3.	Detecting Duplicate Rows:
   
•	By checking for instances where `y_diff` equals 0, we can identify and subsequently remove duplicate rows from the dataset.  
  
### Reasoning Behind y_diff = 0:  
•	The assumption is that if `y_diff` equals 0, it signifies duplicate rows as it implies the same year for consecutive entries of the same country.  
    
### 4.	Summary Sheet Analysis:  
On the newly created summary sheet, the **average**, **minimum**, and **maximum** `year differences` are calculated, rounded to two decimal places.  
  
Average Year Difference:    
  +             = ROUND (AVERAGE (y_diff), 2)
          
 Minimum Year Difference:  
  +              = ROUND (MIN (y_diff), 2)
            
 Maximum Year Difference:  
  +              = ROUND (MAX (y_diff), 2)   
             
The average year difference is found to be **4.8**, the minimum is **1**, and the maximum is **5**.  
  
### 5.	Histogram Creation:  
•	In the same sheet, a histogram of the year column is generated to visualize the distribution of years in the dataset.  
•	 Under customize settings, set max for horizontal axis to **2021**  
![Year distribution](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/58bc5339-67e7-4dbf-8cde-c000886812ea)

### Summary of Findings:
The analysis indicates that the dataset exhibits a variability in data recording years, with an average difference of 4.8 years between consecutive entries. The histogram visualization further illustrates the distribution of years in the dataset

  
### 3. Investigating Annual Rates of Change (ARC)  

### 1.	Understanding the Concept of ARC:  
Annual Rates of Change (ARC) are employed to assess whether the proportion of access to drinking water is experiencing a decline or improvement. ARC is calculated as the average yearly change rate of a variable over a specified time period.  
  
**The formula for ARC is expressed as follows:**  
 ARC_x  
+      = (wat_bas_x(n+1) - wat_bas_x(n)) / (year(n+1) - year(n))
  
Here, `x` represents the different areas, with `ARC_n` for national, `ARC_r` for rural, and `ARC_u` for urban areas.  


### 2.	Creating ARC Columns:
Three new columns, namely `ARC_n`, `ARC_r`, and `ARC_u`, are added to the dataset sheet to represent the Annual Rates of Change for **national**, **rural**, and **urban** populations.  
  
### 3.	Calculating ARC for Each Area:  
ARC values are computed for each area by applying the formula only when the country name in the next row is the same as the country name in the current row.  


![arc_flow](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/4e45860d-6eef-479c-b3ab-70adcc42e274)


![arc_pseudo](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/2bdc2767-8e94-4886-b454-11b15a2d3609)


**Pseudocode for the IF Statement:**
  
+       = IF($A2=$A3,($E3-$E2)/($B3-$B2),""),"null"

    
Similar formulas are applied for `ARC_r` and `ARC_u`, considering the corresponding columns.
  
### 4.	Handling Errors:
The IFERROR function is integrated into the IF statements for `ARC_n`, `ARC_r`, and `ARC_u` to replace error values with **"null"**.  
    
### Observing #VALUE! Errors:
The errors are observed in rows where one or both of the `wat_bas_x` rows are `"null."` The IFERROR function is added to mitigate these errors.  
  
**Conditional Statement for Error Handling:**
+     = IFERROR(IF($A2=$A3,($E3-$E2)/($B3-$B2),""),"null") 

  
### 5.	Calculating Averages, Minimums, and Maximums:
On the summary sheet, the average, minimum, and maximum values for ARC_n, ARC_r, and ARC_u are calculated. 
  
**Average ARC_n:**   
   +     = ROUND (AVERAGE (ARC_n),2)

  
 **Average ARC_r:** 
   +     = ROUND (AVERAGE (ARC_r),2)
       
**Average ARC_u:**    
   +      = ROUND (AVERAGE (ARC_u),2)
       
The **average ARC** values are found to be **0.28**, **0.48**, and **0.15** for national, rural, and urban populations, respectively.

  
### 4. Investigating Access by Area  
#### A.	What does the change in access to basic water look like for different areas?  
#### B.	How does the ARC differ between rural and urban populations?  
  
***A.	Analyzing Change in Access to Basic Water***
  
### 1.	Counting Null Values:  
In the summary sheet, calculate the number of countries with missing ARC values for national `ARC_n`, rural `ARC_r`, and urban `ARC_u` areas.  
   
**Null Values**   
  
ARC_x:  
+           = COUNTIF (arc_x, "null")
  
 ARC_n:  
+           = COUNTIF ('Estimates of the use of water (2000-2020)'!$R2:$R463, "null")
            = 2
          
 ARC_r:  
 +          = COUNTIF ('Estimates of the use of water (2000-2020)'!$S2:$S463, "null")
            = 64
           
 ARC_u:  
 +            = COUNTIF ('Estimates of the use of water (2000-2020)'!$T4:$T465, "null")
              = 50

  
### 2.	Counting Full Access:
Three new columns, namely `wat_bas_n (rounded)`, `wat_bas_r (rounded)`, and `wat_bas_u (rounded)`, are created in the original dataset sheet by rounding the original access to basic water services columns to the nearest whole number. The IFERROR function is employed to handle potential errors during this rounding process, returning the rounded value if successful or the string `null` if an error occurs.  
  
wat_bas_x (rounded):
+         = IFERROR(ROUND(wat_bas_x, 0), "null")
    
wat_bas_n (rounded):
+        = IFERROR(ROUND(E2, 0), "null")  
            
 wat_bas_r (rounded):
 +        = IFERROR(ROUND(I2, 0), "null")
             
wat_bas_u (rounded): 
  +       = IFERROR(ROUND(M2, 0), "null")
             
 
**Additionally**, columns `ARC_n_full`, `ARC_r_full`, and `ARC_u_full` are created to determine "full access" based on conditions.
IF the country names are the same AND that both `wat_bas_n (rounded)` features for that country are **> 99%** for both years. Return “full access” if it is true.

+      START
       If name(n) == name(n+1) AND wat_bas_n (rounded)(n) == 100 AND wat_bas_n (rounded)(n+1) == 100
       then
       ARC_n_full = “full access”
       End if
       END
  
ARC_n_full:   
+            =IF(AND($A3 = $A2,W2 = 100,W3 =100),"full access","")
    
 ARC_r_full:
 +           =IF(AND($A3 = $A2,V2 = 100,V3 =100),"full access","")
     
 ARC_u_full:
 +            =IF(AND($A3 = $A2,W2 = 100,W3 =100),"full access","")
  
The number of countries with full access per population is then calculated in the summary sheet.
  
Full Access ARC_n:
+            =COUNTIF($X2:$X463, "full access") 
             = 62
           
Full Access ARC_r: 
+            =COUNTIF($Y2:$Y463, "full access") 
             = 29
           
Full Access ARC_u:
+            =COUNTIF($Z2:$Z463, "full access") 
             = 55
  
### 3.	Counting Zero, Negative, and Positive ARCs:  
The number of countries with ARC values equal to zero, less than zero, and greater than zero is calculated for national, rural, and urban populations.  
  
National  
+           =COUNTIFS($R2:$R463, "= 0", $X2:$X463,"<>full access")
            = 16
 Rural  
+           =COUNTIFS('$S2:$S463, "=0", $Y2:$Y463,"<>full access")
            = 5
Urban  
+           =COUNTIFS($T2:$T463, "= 0", $Z2:$Z463,"<>full access")
            = 7
          
Number of countries where ARC < 0 and doesn’t have full access for each of the population types: national, rural, and urban  
  
National  
+           =COUNTIFS($R2:$R463, "< 0", $X2:$X463,"<>full access")
            = 16
          
 Rural    
+           =COUNTIFS($S2:$S463, "<0", $Y2:$Y463,"<>full access")
            = 17
          
Urban  
+           =COUNTIFS($T2:$T463, "< 0", $Z2:$Z463,"<>full access")
            = 26
  
Calculate the number of countries where ARC > 0 and doesn’t have full access for each of the population types.  
  
National  
+           =COUNTIFS($R2:$R463, "> 0", '$X2:$X463,"<>full access")
            = 135
          
 Rural  
+           =COUNTIFS($S2:$S463, "> 0", $Y2:$Y463,"<>full access")
            = 116
          
Urban     
+           =COUNTIFS($T2:$T463, "> 0", $Z2:$Z463,"<>full access")
            = 93


  ![pivot2](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/99fb30c1-38b9-4f7c-84b9-6391bd7bbd8f)
  
We can check for full access by using the not equal operator **(<>)** in our **COUNTIFS()** formula on the “full access” string in the `ARC_n_full`, `ARC_r_full`, and `ARC_u_full` columns.  
  
We can check that we’ve considered all countries for the conditions:  
no value, full access, ARC = 0, ARC < 0, and ARC > 0, by summing the number of countries for each and comparing it to the total number of countries.  
  

  
***B. Analyzing Differences in ARC between Rural and Urban Populations***  
  
### 1.	Calculating ARC Differences:   
A new feature called `ARC_diff` is created in the dataset sheet to calculate the difference between rural ARC `ARC_r` and urban ARC `ARC_u` for every second row.  

ARC_diff:  
+            = IF (AND (ARC_r <>"“, ARC_u<>""),ARC_r-ARC_u,"")
             = IF (AND (S2 <>"“, T2<>""),S2-T2,"")

  
### 2.	Handling Errors:  
The formula is adjusted to account for #VALUE! errors.  
  
ARC_diff 
+            = IFERROR (IF (AND (ARC_r <>””, ARC_u<>""), ARC_r- ARC_u,""), "null")
    
### 3.	Histogram Creation:  
Select the data: Highlight both the "ARC_diff" column (containing the differences in annual rates of change) and the "Arc_n_full" column (containing the corresponding national full annual rates of change).  
1)	Insert the histogram  
2)	Configure the axes, ensure that `Arc_diff` is assigned as the "Series" (values for the bars) and `Arc_n_full` is assigned as the "Horizontal (Category) Axis Labels."  





![Distribution of Differences in Annual Rates of Change (Rural vs  Urban)](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/278a8719-9e79-4892-b712-41a37a05c408)






IMAGE: Histogram
### Summary of Findings:
1.	This histogram reveals how yearly change rates for two variables differ. Years with small change gaps in both are most common, though some years exhibit much larger discrepancies.
2.	While the specific direction of change remains unclear (both variables could increase/decrease), the range of possibilities spans from -2.50 to 2.50 percentage points.
3.	Overall, the data suggests diversity in year-on-year change patterns between these two variables.



### 5. Investigating Access to Basic Water Services by Region   
  
### 1. Understanding Regional Differences  
The United Nations categorizes countries into regions to track progress towards Sustainable Development Goals (SDGs). We aim to analyse whether access to basic water services varies across these regions and identify areas needing targeted efforts.  
  
***A. Access and Region: Data Preparation***  
  
Our initial dataset lacks regional information. To bridge this gap,Import and Add a new sheet containing regional data **(Regions.csv)**.
  
**Merge:** Create a new column in the original dataset named `region`. Use a **LOOKUP** function to assign each country its corresponding region based on its country name.
  
Region  
+            =VLOOKUP (lookup_value, table_array, col_index_num, [range_lookup])
             =VLOOKUP (name, Regions!region, 2, FALSE)
             =VLOOKUP (A2, Regions! $A$1: $B$233,2, FALSE)
           

### Summarize:     
**In the summary sheet, the following summary statistics are calculated in a pivot table for each region:**    
a. The number of countries per region.  
b. The average Annual Rates of Change on a national level per region.  
c. The average Annual Rates of Change in rural areas per region.  
d. The average Annual Rates of Change in urban areas per region.  

![pivot](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/fc26aecd-d015-48ff-b43c-60e4c880ce28)



***B.	Visualizing Access by Region:***  
To analyse the connection between national and rural Annual Rates of Change (ARCs) and their correlation with population size across different regions, we generate a visualization that illustrates access by region.    
The visual representation focuses on comparing the national ARC to the rural ARC, and simultaneously depict the relationship between region-specific population sizes and the national population.   



![Access to Water_ Rural vs  National Change by Region (Population Size)](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/aa9bf995-30fb-4265-aff4-1623a6c0e8ac)




### Observations:  
This bubble chart depicts the connection between access to basic water service, measured by annual rates of change (ARCs), across different regions.  
  
**Each bubble represents a region, with its position determined by two factors:**    
	**X-axis:** `ARC_n` (National Annual Rate of Change) - This indicates the overall change in access for the entire country.  
	**Y-axis:** `ARC_r` (Rural Annual Rate of Change) - This shows the specific change in access within rural areas of the region.  
  
**The size of the bubble represents another important factor:**  
**Pop_n (National Population):** The larger the bubble, the more significant the population of the region it represents.
  




### C.Weaving ARCs into a Story
 

![image](https://github.com/DesmondMokhali/Investigating-Access-to-Safe-Drinking-Water/assets/121891418/ab8111a9-b813-4ee8-98e1-a045310d68c6)




+  The analysis provides actionable insights into the water crisis in Sub-Saharan Africa. Despite some progress, the region is projected to achieve full access to water only by approximately 2080 at the current rate of change.
+  This information forms the basis for a compelling narrative about the urgent need for intervention in Sub-Saharan Africa to address the water crisis. Without significant efforts, millions of Africans will continue to face a scarcity of clean water for the next ~60 years. This narrative underscores the importance of targeted interventions and policy measures to improve water access in the region.




