# Procurement-Performance-Dashboard-PBI

## Table of Contents:
1. [INTRODUCTION](#data)
2. [DESIGN THINKING APPROACH](#d_thinking)
3. [DASHBOARD](#dashboard)
4. [INSIGHTS & RECOMMENDATIONS](#insight)

<div id='data'/>

## **I.INTRODUCTION**
In this project, a _**operation dashboard**_ was developed using _**Design Thinking**_ approach and _**Power BI**_ tools (**_DAX_**, **_Power Query_**, and **_Visualization_** tools) to analyze **_global sales performance_** over 4 years. The dashboard aimed to assist senior managers in **_understanding business performance by region, product, and sales personnel,_** which led to **_decisions_** in **_Market expansion_**, **_Market optimization_**, and **_Product selection_**.

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

<div id='d_thinking'/>
  
## **II.DESIGN THINKING APPROACH**
### Stage 1: Empathize
|5W1H|---|
|---|---|
|Who will be viewing this Dashboard?|	Senior managers (Purchasing Manager; Supply Chain Manager; Operations Manager...)|
|If we had to choose only one key Stakeholder, who would it be?| Purchasing Manager|
|What problem does this Dashboard solve?	| Nắm bắt tình hình tổng quan ở bộ phận thu mua<br>Đánh giá chất lượng của nhà cung cấp |
|Describe the problem in one sentence |	Giúp Purchasing manager nắm bắt tình hình tổng quan trong bộ phận mua sắm. Đồng thời đánh giá lại nhà cung cấp cho phù hợp để phát triển chiến lược hoạt động của công ty hơn nữa.|
|When and where will Stakeholders view this Dashboard?|1. Khi xem xét hiệu suất của phòng ban trong cuộc họp hàng tuần hoặc hàng tháng<br>2. Đánh giá TotalDue|
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

<div id='dashboard'/>
  
## **III. DASHBOARD**
### **Data Modeling**
<img width="451" alt="Image" src="https://github.com/user-attachments/assets/3519aa05-6645-43db-8768-e28d952cbf40" />

### **View 1: Overview**
<img width="652" alt="Image" src="https://github.com/user-attachments/assets/ecaecf5c-cc67-4dec-8d73-2d67f333b14c" />

### **View 2: Vendor Analysis**
<img width="653" alt="Image" src="https://github.com/user-attachments/assets/a365829b-e380-4e2f-9f41-60d84657d300" />

<div id='insight'/>
  
## **IV. INSIGHTS & RECOMMENDATIONS**
## 1. Chi phí sản phẩm và giao hàng có được tối ưu hóa không?

### Chi phí Sản phẩm:
**Insight:**  
- Hầu hết các sản phẩm có giá khi mua cao hơn giá chuẩn, với chênh lệch trung bình khoảng **1.6** → chi phí nhập hàng chưa được tối ưu hóa.  
- Một số sản phẩm có mức chênh lệch đáng kể, đạt tới **10.46** (*All-Purpose Bike* của *Green Lake Bike*) → tăng chi phí vận hành & ảnh hưởng lợi nhuận.  

**Recommendation:**  
- Thương lượng lại với nhà cung cấp để điều chỉnh về giá chuẩn.  
- Theo dõi các trường hợp vượt chuẩn và áp dụng quy trình kiểm tra giá trước khi đặt hàng.  
- Tạo báo cáo cảnh báo cho các sản phẩm có chi phí nhập vượt mức chuẩn.  

### Chi phí Giao hàng:
**Insight:**  
- Chi phí giao hàng lớn nhất đến từ *Cargo Transport 5* (**0.73M**), chiếm phần lớn chi phí vận chuyển so với các công ty khác như:  
  - *ZY - Express*: **0.34M**  
  - *Overnight J-FAST*: **0.27M**  

**Recommendation:**  
- So sánh và đánh giá các nhà cung cấp để tìm ra giải pháp tối ưu hơn về chi phí.  
- Cân nhắc hợp nhất lô hàng hoặc thương lượng giá với *Cargo Transport 5*.  


## 2. Giao hàng có đúng hạn không?  

**Insight:**  
- Tỷ lệ giao hàng đúng hạn trung bình của các nhà cung cấp là **100%**.  

**Recommendation:**  
- Đánh giá toàn bộ danh sách nhà cung cấp để xác định những nhà cung cấp có tỷ lệ giao hàng thấp hơn **100%**.  
- Tạo báo cáo động để giám sát tỷ lệ giao hàng theo thời gian.  

## 3. Số lượng sản phẩm đã mua đủ chưa & đạt tiêu chuẩn chất lượng không?  

**Insight:**  
- Một số sản phẩm như **Metal Sheet 1** (*10.3% rejected*) và **Paint - Black** (*8.7% rejected*) có tỷ lệ bị từ chối cao, cần phải xử lý vấn đề.  
- Các sản phẩm khác như **Flat Washer 1** và **Flat Washer 6** nằm trong nhóm có vấn đề, mặc dù số lượng đặt hàng không lớn nhưng tỷ lệ bị từ chối vẫn đáng chú ý.  
- Tình trạng này có thể làm gián đoạn sản xuất hoặc phát sinh chi phí bổ sung để đặt hàng bổ sung.  

**Recommendation:**  
- Trao đổi và yêu cầu cải thiện chất lượng đối với các sản phẩm có tỷ lệ bị từ chối cao như **Metal Sheet 1** và **Paint - Black** với nhà cung cấp.  
- Áp dụng quy trình kiểm tra chất lượng nghiêm ngặt hơn nhằm hạn chế phát hiện sản phẩm lỗi.  
- Đề xuất thay thế nhà cung cấp nếu vấn đề chất lượng không cải thiện trong thời gian nhất định.  

