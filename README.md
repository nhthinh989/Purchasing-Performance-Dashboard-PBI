# Procurement-Performance-Dashboard-PBI

## **I.INTRODUCTION**
In this project, a **_strategic dashboard_** was developed using _**Design Thinking**_ approach and _**Power BI**_ tools (**_DAX_**, **_Power Query_**, and **_Visualization_** tools) to analyze **_global sales performance_** over 4 years. The dashboard aimed to assist senior managers in **_understanding business performance by region, product, and sales personnel,_** which led to **_decisions_** in **_Market expansion_**, **_Market optimization_**, and **_Product selection_**.

### **1. BUSINESS QUESTIONS**
Adventure Works Cycles is a bicycle manufacturing company that operates across multiple business functions. Senior management of Adventure Works Cycles requires a detailed understanding of the company’s procurement efficiency to optimize inventory management and cost control in relation to:

- Ensuring sufficient procurement of raw materials and goods to meet sales demand
- Optimizing purchase costs while maintaining quality standards
- Aligning procurement schedules with production and sales timelines
- Identifying potential inefficiencies in the purchasing process

### **2. DATASET**
The dataset (as attachment) contains global sales information of Superstore, including 3 tables:
- Orders: a table storing transaction information
- People: a table containing information about sales representatives in each region
- Returns: a table recording transactions that were returned

## **II.DESIGN THINKING APPROACH**
### Stage 1: Empathize
|5W1H|---|
|---|---|
|Who will be viewing this Dashboard?|	Senior managers (CEO, Sales Manager, Marketing Manager, HR Manager, etc.)|
|If we had to choose only one key Stakeholder, who would it be?| CEO|
|What problem does this Dashboard solve?	| Market expansion strategy<br>Plan for improving the current market<br>Strategic product selection decisions<br>Sales personnel allocation plan|
|Describe the problem in one sentence |	Assist the CEO in understanding the business performance (sales, returns) by region, product, and sales personnel, to support decision-making regarding market expansion, strategic product selection, and personnel allocation.|
|When and where will Stakeholders view this Dashboard?| 1. When working independently, to grasp the business performance to carefully consider strategic decisions.<br>2. During strategy discussions with the team in meetings.|
|Why do stakeholders need this Dashboard?| 1. To quickly understand the business performance of products, markets, and sales personnel.<br>2. To have a basis for selecting strategic products and target markets for expansion.<br>3. To consider the sales personnel allocation plan.<br>4. To determine whether business performance needs improvement in any specific market.|
|How have stakeholders been achieving their goals so far?	| 1. Understand sales, returns, and growth rates across markets <br>--> Identify potential markets <br>--> Determine which markets need improvement <br>--> Plan to investigate causes and propose solutions)<br> 2. Understand sales, returns, and growth rates by product category --> Select strategic products<br>3. Track sales, performance growth, and regions managed by each sales representative --> Allocate personnel accordingly|

|Empathy Map|---|
|---|---|
|**Thinking and feeling**<br>_What does the stakeholder think and feel?_|	The company is performing well, and your focus is on driving further growth with the immediate goal of reaching this year's revenue target. It's great to have that clear objective in mind while exploring strategies to enhance business performance!|
|**Seeing**<br>_What does the stakeholder see?_|	The company is operating successfully on a global scale.<br>This year's revenue target has been set higher than the previous year's.|
|**Saying and doing**<br>_What does the stakeholder say and do?_	|"I believe that expanding into new markets can help the company achieve its revenue goals".<br>"To increase revenue, I should also assess the current markets to identify any areas that require improvement".|
|**Pains**<br>_What are the biggest problems and challenges?_|	1. What are the potential markets for expansion?<br>2. Is there a need to improve the current markets?<br>3. Which products should be prioritized for the new or existing markets?<br>4. Who will be responsible for the new market? Is there a need to adjust personnel allocation?|
|**Gains**<br>_What are the opportunities and benefits?_|	With the analyzed data, the CEO will gain an accurate understanding of the business performance, allowing for the validation of assumptions and informed decision-making.|

### Stage 2: Define Point of View
|Northstar Metric|---|
|---|---|
|What VALUE you want to measure?|Total value generated from customers through sales.|
|WHEN the value DELIVERY SUCCESS?|When an order is completed.|
|Northstar Metric Name|Revenue|
|WHY do you choose this metric?|Reflecting the business's sales performance, higher the revenue better the performance.|

Dimension Data Group
|**Group 1** - Location|**Group 2** - Product|**Group 3** - Salesman|**Group 4** - Time|
|:---:|:---:|:---:|:---:|
|_Market<br>Region<br>Country_|	_Product<br>Product Category_	|_Sales person_|_YoY_|

Define Point of View
|View	|Description	|	Why	|
|---|:---:|---|
|**View1**| Market Analysis|	Identify potential markets for expansion and weak markets that need improvement.	|			
|**View2**| Product Analysis|	Select strategic products for each market or for all markets.	|		
|**View3**| Sales Person Analysis|	Select personnel responsible for the new market and reallocate personnel for existing markets (if necessary).|

Growth Formula
|Northstar Metric:|Revenue|
|---|---|
|View 1 breakdown	| Revenue by Market, by Time|
|View 2 breakdown	| Revenue by Product, by Time, by Product & Market	|
|View 3 breakdown	| Revenue by Sales Person |


### Stage 3: Ideate
Brainstorming
|Idea Name|Layer 0 dimension| Layer 1 dimension|Layer 2 dimension|
|---|---|---|---|
|View 1: Market| 1. Total Revenue<br>2. Total Profit<br>3. Total Number of Customer|1. Revenue by market<br>2. Profit by market<br>3. Profit Margin by market<br>4. Customer number by market<br>5. Return Rate by market<br>6. YoY Growth Rate of Revenue by market|1. Revenue, profit by market, by category|
|View 2: Product|1. Total Revenue<br>2. Total Profit|1. Revenue by product category<br>2. Profit  by product category<br>3. Product Classification:<br>- High vol, High profit<br>- High vol, Low profit<br>- Low vol, High profit<br>- Low vol, Low profit<br>4. Profit margin by product category<br>5. Return rate by product category<br>6. YoY Growth Rate of Revenue by product category |1. Revenue, profit by category, by year|
|View 3: Sales Person	|1. Total Revenue<br>2. Total Profit|1. Revenue by person<br>2. Profit by person<br>3. Profit margin by person<br>4. YoY Growth Rate of Revenue by person<br>5. Market by person|1. Revenue, profit by person, by category|

Structure idea
|---|	Metric 1 | Metric 2	| Metric 3	| Metric 4 |
|---|---|---|---|---|
|Scorecard	|Revenue	|Number of customers	|Profit	|Profit Margin|

|Idea Name	| Highly important info|	Important info | Detailed info |
|---|---|---|---|
|View 1|1. Revenue by market<br>2. Profit by market<br>3. Profit Margin by market<br>4. Customer number by market<br>5. Return Rate by market<br>6. YoY Growth Rate of Revenue by market|1. Total Revenue<br>2. Total Profit<br>3. Total Number of Customer|1. Revenue, profit by market, by category<br>2. Market details"	|
|View 2|1. Revenue by product category<br>2. Profit  by product category<br>3. Product Classification:<br>- High vol, High profit<br>- High vol, Low profit<br>- Low vol, High profit<br>- Low vol, Low profit<br>4. Profit margin by product category<br>5. Return rate by product category<br>6. YoY Growth Rate of Revenue by product category|1. Total Revenue<br>2. Total Profit |1. Revenue, profit by category, by year|
|View 3	|1. Revenue by person<br>2. Profit by person<br>3. Profit margin by person<br>4. YoY Growth Rate of Revenue by person|1. Total Revenue<br>2. Total Profit|1. Market by person<br>2. Sales person details|	

### Stage 4: Prototype & Review
This is implementation and review stage. Prototype and Review dashboard multiple times to achieve the final dashboard.

## **III. DASHBOARD**
### **Data Modeling**
<img width="950" alt="DataModeling" src="https://github.com/user-attachments/assets/9413c9a9-945c-4ab6-ad49-932c0e682b86">

### **View 1: Market Analysis**
<img width="952" alt="Market" src="https://github.com/user-attachments/assets/90292d44-c85a-434d-b1cc-f3f4404f414e">

➡️ Insights:
- The company has its **_presence in all major markets_** around the world.
  - **_LATAM_**: Contributes **_highest revenue and profit_**, average rate of goods returned.
  - **_APAC_**: **_Highest YoY growth rate & customers count_**, ranks **_second in revenue_**, but exhibits **_low profit margins_**.
  - **_US Market_**: Ranks **_second in profit_**, this market has **_surprisingly high profit margin_**, an average number of customers, but **_low revenue_**.
  - **_Africa_** and **_EMEA_**: Has **_high customer numbers_** but **_negative profit_**.
  - **_Canada_**: Having **_strong YoY growth rate_** but **_few customers, low revenue_**

### **View 2: Product Analysis**
<img width="950" alt="Product" src="https://github.com/user-attachments/assets/4c8edaa8-0132-456e-b769-1225b51686ae">
<img width="950" alt="Product-Market" src="https://github.com/user-attachments/assets/0256876b-f3a2-4de8-ac04-98691dc09b53">

➡️ Insights:
-	**_Copiers_** are the company’s **_best-selling product overall_**, except for **_US market_**, where **_phones_** and **_chairs_** out-perform copiers.
-	**_Tables_** has poor performance with **_negative profit margins_** over the past four years, resulting in losses.
-	The **_return rate for binders_** has reached **_25%_**, which is **_highest among all_**.

### **View 3: Sales Agent Analysis**
<img width="950" alt="Salesman" src="https://github.com/user-attachments/assets/a638370e-018d-45e6-84e4-2e130cb034ff">

➡️ Insights:
-	**_Sales Agent of APAC-South East Asia market_**: performance is not very well with **_negative profit_** and a **_profit margin_** of only **_4%_**, although the he is **_selling key products_** such as copiers, phones, and bookcases in his market-in-charge.

## **IV. INSIGHTS & RECOMMENDATIONS**
### 1. Market Expansion
- ***Market Overview***:
  - The company has established presence in all major global markets. Rather than entering a completely new market, it is recommended to **_expand within the existing market_**. **_Canada_** market is **_recommended_**.
  - Despite Canada's strong Year-over-Year (YoY) growth rate and profit margin, its customer base remains limited, resulting in lower revenue. <br>--> It is proposed to develop a **_strategy to reach a broader customer segment_** in **_Canada_**.

- ***Sales Agent***:
  - **_Nicole Hansen_** is currently **_responsible for the Canadian market_**. The revenue, profit margin, and YoY growth rate indicators are **_performing well_**. <br>--> It is advisable to **_continue_** his/her oversight of this market.

- ***Product Strategy***:
  - Copiers are the company’s best-selling product overall. <br>--> It is suggested that **_copiers_** be positioned as a **_strategic product for the company_**.

### 2. Current Market Optimization
- ***LATAM Market***: **_Maintain the current strategy_** for this market as this market has been the best performer overall.

- ***APAC Market***:
  - This market is growing rapidly, has the highest number of customers, and ranks second in revenue, though it exhibits low profit margins. <br>--> It is recommended to **_investigate the reasons_** for the **_low profit margins_** and to develop **_strategies_** to **_enhance profitability from existing customer base_** by either increasing sales or improving profit margins.

- ***US Market***:
  - Ranked second in profit, this market has an unexpectedly high profit margin, an average number of customers, but low revenue. <br>--> It is proposed to develop **_strategies_** to drive **_more customer purchases_**, potentially considering a lower profit margin to stimulate higher sales volumes. **_Strategic products_** for this market should include **_phones_** and **_chairs_**.

- ***Ineffective Markets***:
  - **_Africa and EMEA are underperforming_**, with high customer numbers but negative total profits. <br>--> It is recommended to **_investigate the causes_** behind these issues to develop appropriate **_strategies_** for **_either improvement or withdrawal_** from these markets.

- ***Product Performance***: 
  - **_Tables_** have shown **_poor performance_** with negative profit margins over the past four years, resulting in losses with each sale <br>--> **_Discontinue_** this product or **_adjust its pricing_**.
  - The return rate for binders has reached 25% <br>--> **_Investigate the causes_** behind this high return rate and **_implement corrective measures_**.

- ***APAC-South East Asia Sales Agent***: It is proposed to issue a **_warning to the sales agent_** in this region due to negative profit and a profit margin of only 4%, despite the market's strong performance in key products like copiers, phones, and bookcases. The sales agent should reassess and **_adjust their sales plan_** accordingly.
