# Purchasing-Performance-Dashboard-PBI

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

### **2. DATASET**
AdventureWorks database supports standard online transaction processing scenarios for Adventure Works Cycles. Scenarios include Manufacturing, Sales, Purchasing, Product Management, Contact Management, and Human Resources.

Dataset: adventureworks2019 (public Google BigQuery dataset)

Dataset dictionary: https://drive.google.com/file/d/1bwwsS3cRJYOg1cvNppc1K_8dQLELN16T/view

<div id='d_thinking'/>
  
## **II.DESIGN THINKING APPROACH**
### Stage 1: Empathize
![Image](https://github.com/user-attachments/assets/90789b12-1a54-4c3b-bc51-fe8e8692db68)
![Image](https://github.com/user-attachments/assets/dcdfa52b-43e9-4f37-9c45-efb81eeff9c2)

### Stage 2: Define Point of View
![Image](https://github.com/user-attachments/assets/8f2c30fe-9a4d-4059-a7b2-5cf7a698d8c2)
![Image](https://github.com/user-attachments/assets/61ec22da-a5d8-48c0-b0d4-272184a97b45)
![image](https://github.com/user-attachments/assets/c07b1b4b-cdc8-4100-8c81-8d8b6accc9d6)


### Stage 3: Ideate
Brainstorming
![Image](https://github.com/user-attachments/assets/9b67405c-4bb5-4554-b48d-243b07069622)
Structure idea
![image](https://github.com/user-attachments/assets/46152ba2-b8eb-4485-86bc-f479e9c8d899)

### Stage 4: Prototype & Review
This is implementation and review stage. Prototype and Review dashboard multiple times to achieve the final dashboard.

<div id='dashboard'/>
  
## **III. DASHBOARD**
### **Data Modeling**
<img width="451" alt="Image" src="https://github.com/user-attachments/assets/3519aa05-6645-43db-8768-e28d952cbf40" />

### **View 1: Overview**
![Image](https://github.com/user-attachments/assets/7e71961a-e4ca-4fa4-87c6-2974906de653)

### **View 2: Vendor Analysis**
![Image](https://github.com/user-attachments/assets/af6f1b5e-52af-426b-ba59-0b46915f5c05)

<div id='insight'/>
  
## **IV. INSIGHTS & RECOMMENDATIONS**

**1. Insights**

**1.1 Overall Purchasing Performance**

- **Average order processing time is 19.45 days**, which is relatively long and may affect supply chain efficiency.
- **On-time delivery rate is 100%**, indicating an effective purchasing process in terms of delivery timeliness.
- **Total shipping cost is $1.58M**, accounting for **2.25% of the total invoice value ($70.48M)**. Specifically:
    - **Cargo Transport 5** has the highest shipping cost **($0.73M)**, nearly double that of **ZY-Express ($0.34M)** and three times that of **Overnight J-Fast ($0.27M)**.
    - There are significant cost differences among shipping providers, which may impact overall purchasing expenses.

**1.2 Order Analysis by Year**

- **Total purchasing spending increased significantly from 2011 to 2014**, peaking in 2014.
- **The fastest growth occurred between 2012 and 2013**, reflecting an expanding purchasing demand.
- **A decline in spending was observed at the end of 2014**, potentially due to strategic or market changes.

**1.3 Product Rejection Rate Analysis**

- **Average rejection rate: 3.1%** across a total of **2.32 million units received**.
- Some products have **high rejection rates**:
    - **Metal Sheet 1 (10.3%)**, **Paint - Black (8.7%)**, **Flat Washer 1 (8.5%)**.
    - These products may have quality issues from suppliers or errors in inbound inspections.
- High-volume items like **ML Crankarm (43,784 units received)** also show significant rejections **(2,805 units)**, which could impact production.

**1.4 Vendor Analysis**

- **Total vendors: 104**, with **100 active** and **4 inactive**.
- **93 vendors are preferred**, but **11 vendors are not**, suggesting potential optimization opportunities.
- **Superior Bicycles** is the largest vendor by purchase value **($4.55M)**, followed by **Professional Athletic Consultants ($3.06M)**.
- Some vendors have higher rejection rates, which may be linked to price or product quality issues.

**1.5 Standard Price vs. Last Purchase Price Analysis**

- **A 5% discrepancy** exists between standard and actual purchase prices.
- Some products have higher purchase costs than standard prices, potentially increasing overall expenses if not managed properly.

---

**2. Recommendations**

**2.1 Optimize Purchasing Process & Order Processing Time**

✅ **Reduce order processing time (19.45 days) to ~15 days** by:

- Implementing **long-term contracts** with reliable suppliers to reduce negotiation time.
- Using **purchase automation** to speed up approval and order processing.
- Integrating **inventory management systems** to forecast demand and enable proactive ordering.

**2.2 Control Shipping Costs**

✅ **Review Cargo Transport 5’s contract ($0.73M) and consider alternatives**:

- Compare costs among shipping providers and explore **lower-cost alternatives**.
- **Negotiate discounts** with Cargo Transport 5 if their shipping volume remains high.

**2.3 Reduce Product Rejection Rates**

✅ **Improve quality control for incoming goods**:

- **Enhance inspection** for high-rejection products like **Metal Sheet 1 (10.3%)** and **Paint - Black (8.7%)**.
- Collaborate with suppliers to **improve manufacturing processes** and minimize defects.
- **Develop a reliable supplier list**, eliminating vendors with consistently high rejection rates.

**2.4 Optimize Vendor Portfolio**

✅ **Remove inefficient vendors**:

- Phase out or reduce reliance on **non-preferred vendors (11 vendors)**, focusing on suppliers with better quality and pricing.
- **Negotiate long-term contracts** with vendors achieving **100% on-time delivery**.

**2.5 Manage Purchase Price Volatility**

✅ **Minimize price fluctuations (5% variance)**:

- Establish **price ceilings** for each product based on historical data.
- **Negotiate stable long-term pricing** with suppliers.
- Regularly monitor the difference between standard and actual purchase prices to **prevent unnecessary cost increases**.

#### **2.5 Manage Purchase Price Volatility**  
✅ **Minimize price fluctuations (5% variance)**:  
- Establish **price ceilings** for each product based on historical data.  
- **Negotiate stable long-term pricing** with suppliers.  
- Regularly monitor the difference between standard and actual purchase prices to **prevent unnecessary cost increases**.

