# Procurement-Performance-Dashboard-PBI

## **I.INTRODUCTION**
In this project, a **operation dashboard_** was developed using _**Design Thinking**_ approach and _**Power BI**_ tools (**_DAX_**, **_Power Query_**, and **_Visualization_** tools) to analyze **_global sales performance_** over 4 years. The dashboard aimed to assist senior managers in **_understanding business performance by region, product, and sales personnel,_** which led to **_decisions_** in **_Market expansion_**, **_Market optimization_**, and **_Product selection_**.

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
|Who will be viewing this Dashboard?|	Senior managers (Purchasing Manager; Supply Chain Manager; Operations Manager...)|
|If we had to choose only one key Stakeholder, who would it be?| Purchasing Manager|
|What problem does this Dashboard solve?	| Nắm bắt tình hình tổng quan ở bộ phận thu mua<br>Đánh giá chất lượng của nhà cung cấp |
|Describe the problem in one sentence |	Giúp Purchasing manager nắm bắt tình hình tổng quan trong bộ phận mua sắm. Đồng thời đánh giá lại nhà cung cấp cho phù hợp để phát triển chiến lược hoạt động của công ty hơn nữa.|
|When and where will Stakeholders view this Dashboard?|1. Khi xem xét hiệu suất của phòng ban trong cuộc họp hàng tuần hoặc hàng tháng<br>2. Đánh giá hiệu suất hàng ngày với nhóm, trong cuộc họp nhóm.<br>3. Sử dụng cá nhân khi lập kế hoạch và phân bổ nhiệm vụ cho các thành viên trong nhóm.|
|Why do stakeholders need this Dashboard?| 1. Tối ưu hóa hiệu suất của phòng ban.<br>2. Phát triển kế hoạch mua sắm|
|How have stakeholders been achieving their goals so far?	|1. Hiểu rõ hiệu suất <br>2. Xác định khía cạnh cần tối ưu <br>3. Xây dựng kế hoạch hành động để triển khai tối ưu hóa. <br>-> Managers sẽ theo dõi hiệu suất, gây ra tình trạng ra quyết định chậm trễ và thiếu chính xác.|

|Empathy Map|---|
|---|---|
|**Thinking and feeling**<br>_What does the stakeholder think and feel?_|	Áp lực khi phải đảm bảo đặt hàng đúng số lượng và thời gian.|
|**Seeing**<br>_What does the stakeholder see?_|Bộ phận mua sắm bị phàn nàn về hiệu suất làm việc|
|**Saying and doing**<br>_What does the stakeholder say and do?_	|Các khía cạnh nào cần được làm rõ|
|**Pains**<br>_What are the biggest problems and challenges?_| Hiệu suất chung của bộ phận mua  như thế nào?<br>- Chi phí sản phẩm và giao hàng có được tối ưu hóa không?<br>- Giao hàng có đúng hạn không?<br>- Số lượng sản phẩm đã mua đủ chưa?<br>- Sản phẩm cung cấp có đạt tiêu chuẩn chất lượng không?|
|**Gains**<br>_What are the opportunities and benefits?_|	Tối ưu hóa những vấn đề còn tồn đọng để nâng cao hiệu suất|

### Stage 2: Define Point of View
|Northstar Metric|---|
|---|---|
|What VALUE you want to measure?|Chi phí phải trả|
|WHEN the value DELIVERY SUCCESS?|Khi sản phẩm được nhập hàng thành công|
|Northstar Metric Name||
|WHY do you choose this metric?|Cần phải giám sát chi tiêu cho các công việc mới có thể tối ưu một cách tốt nhất hiệu suất công việc|

Dimension Data Group
|**Group 1** - Location|**Group 2** - Product|**Group 3** - Salesman|**Group 4** - Time|
|:---:|:---:|:---:|:---:|
|_Market<br>Region<br>Country_|	_Product<br>Product Category_	|_Sales person_|_YoY_|

Define Point of View
|View	|Description	|	Why	|
|---|:---:|---|
|**View1**| Overview|	Đánh giá hiệu suất của Bộ phận mua sắm|			
|**View2**| Vendor Analysis|	Đánh giá chất lượng nhà cung cấp để tối ưu hóa giá sản phẩm, thời gian giao hàng.|		

Growth Formula
|Northstar Metric:|Revenue|
|---|---|
|View 1 breakdown	| Total Due & Breakdown, Shipping Cost và On-time delivery Overall|
|View 2 breakdown	| Total Due by Vendor|


### Stage 3: Ideate
Brainstorming
|Idea Name|Layer 0 dimension| Layer 1 dimension|Layer 2 dimension|
|---|---|---|---|
|View 1: Market| 1. Total Due<br>2. Average Lead time<br>3.On-time delivery<br>4. Total Shipping Cost<br>5.Total Order<br>6.Total Tax|1. Shipping cost by vendor<br>2. Breakdown of TotalDue<br>|1. TotalDue by time (Year/Quater/Month/Day)<br>Rejection by Product|
|View 2: Product|1. Total Vendor<br>- Active and not<br>- Prefer and not<br>2. Rating Vendor|1. Subtotal by Vendor<br>2. Standard price and Last Receipt Cost of each Vendor produc |Rejection Rate vs Standard Price & Subtotal|

Structure idea
|---|	Metric 1 | Metric 2	| Metric 3	| Metric 4 |
|---|---|---|---|---|
|Scorecard	|TotalDue	|On-time delivery |AverageLeadTime	|ShippingCost|

|Idea Name	| Highly important info|	Important info | Detailed info |
|---|---|---|---|
|View 1|1. Breakdown of TotalDue<br>2. AverageLeadTime<br>3.On-time delivery|1. TotalShippingCost<br>2. Total Order|1. TotalDue by time<br>2. Rejection Analysis	|
|View 2|1. Total vendor<br>2. Total active, prefer & not by vendors<br>3. CreditRating by vendor|1. Subtotal by Vendor<br> |1. Rejection Rate vs Standard Price & Subtotal<br>2. Standard price and Last Receipt Cost of every Vendor product|

### Stage 4: Prototype & Review
This is implementation and review stage. Prototype and Review dashboard multiple times to achieve the final dashboard.

## **III. DASHBOARD**
### **Data Modeling**
<img width="451" alt="Image" src="https://github.com/user-attachments/assets/3519aa05-6645-43db-8768-e28d952cbf40" />

### **View 1: Overview**
<img width="652" alt="Image" src="https://github.com/user-attachments/assets/ecaecf5c-cc67-4dec-8d73-2d67f333b14c" />

➡️ Insights:
- The company has its **_presence in all major markets_** around the world.
  - **_LATAM_**: Contributes **_highest revenue and profit_**, average rate of goods returned.
  - **_APAC_**: **_Highest YoY growth rate & customers count_**, ranks **_second in revenue_**, but exhibits **_low profit margins_**.
  - **_US Market_**: Ranks **_second in profit_**, this market has **_surprisingly high profit margin_**, an average number of customers, but **_low revenue_**.
  - **_Africa_** and **_EMEA_**: Has **_high customer numbers_** but **_negative profit_**.
  - **_Canada_**: Having **_strong YoY growth rate_** but **_few customers, low revenue_**

### **View 2: VendorVendor Analysis**
<img width="653" alt="Image" src="https://github.com/user-attachments/assets/a365829b-e380-4e2f-9f41-60d84657d300" />

➡️ Insights:
-	**_Copiers_** are the company’s **_best-selling product overall_**, except for **_US market_**, where **_phones_** and **_chairs_** out-perform copiers.
-	**_Tables_** has poor performance with **_negative profit margins_** over the past four years, resulting in losses.
-	The **_return rate for binders_** has reached **_25%_**, which is **_highest among all_**.


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
