# EDA_Capstone_Project_Hotel_Booking-Sumit-
EDA_Capstone_Project_Hotel_Booking(Sumit)
Here’s a detailed summary of what was performed in the analysis, along with key insights and findings:

---

## **1. Know Your Data**
### **Summary:**
- **Dataset Overview:**  
  - **Shape:** 119,390 rows × 32 columns.  
  - Columns like `hotel`, `is_canceled`, `lead_time`, `arrival_date_*`, and others provide insights into booking trends, cancellations, and customer behavior.  

- **Missing Values:**  
  - Key columns with missing values: `children` (4 entries), `country` (488 entries), `agent` (13.68%), `company` (94.31%).  
  - High null percentage in the `company` column suggests it may be dropped for effective analysis.

- **Duplicates:**  
  - **Duplicate Rows:** 31,994 duplicate rows were found.  

- **Unique Customer Types:**  
  - `customer_type` has 4 unique values:  
    - **Transient (75%)**  
    - **Transient-Party (21%)**  
    - **Contract (3.4%)**  
    - **Group (<1%)**  

---

## **2. Understanding Your Variables**
### **Observations:**
- **High Cardinality in `adr`:** 3,162 unique values for the `adr` (Average Daily Rate) column.  
- **Top Distributions:**  
  - Most bookings are for transient customers.  
  - Market segments like `Online TA` and `Groups` dominate.  

- **Insights on Cancellation:**  
  - Over 30% of the bookings were canceled.

---

## **3. Data Wrangling**
### **Actions Taken:**
1. **Column Drops:**  
   - Dropped the `company` column due to over 94% missing values.
2. **EDA Preparedness:**  
   - Grouped data by `market_segment`, `deposit_type`, `hotel`, and cancellation status.  
   - Distribution plots like histograms and bar charts were plotted to understand `adr`, booking patterns, and cancellation rates.

---

## **4. Data Visualization and Storytelling**
### **Key Charts & Insights:**

#### **Chart 1: Booking Cancellation Status (Pie Chart)**  
- **Insights:**  
  - ~37% cancellations.  
  - Suggests a high cancellation rate that could be analyzed by factors like `deposit_type` and `lead_time`.

#### **Chart 2: Month-Wise Bookings (Bar Chart)**  
- **Insights:**  
  - Bookings peak in summer months (May–August).  
  - Low in winter, especially December.

#### **Chart 3: Reservations by Market Segment and Cancellation Status**  
- **Insights:**  
  - **Online TA and Groups** show higher cancellation rates.  
  - Contract-based bookings rarely cancel.

#### **Chart 4: Bookings and Cancellations by Customer Type**  
- **Insights:**  
  - **Transient customers** have the highest cancellations, likely due to more flexibility.  
  - Contracts have minimal cancellations.

#### **Chart 5: Distribution of Bookings by Market Segment (Pie Chart)**  
- **Insights:**  
  - Online Travel Agents dominate (~50%).  
  - Corporate and Groups follow.

#### **Chart 6: Hotel Type and Cancellation vs. Booking Ratio**  
- **Insights:**  
  - Resort hotels show a higher booking ratio compared to city hotels.  
  - Cancellations are more frequent for city hotels.

#### **Chart 7: Monthly Bookings by Market Segment**  
- **Insights:**  
  - **Online TA bookings dominate year-round.**  
  - Groups contribute more in holiday seasons.

#### **Chart 8: Hotel Types and Special Requests Comparison**  
- **Insights:**  
  - Customers in resort hotels tend to make more special requests.  
  - City hotels see fewer requests, potentially linked to shorter stays.

#### **Chart 9: Arrival Year-wise Bookings and Cancellations**  
- **Insights:**  
  - Booking trends are stable, but cancellation rates slightly increase over years.

---

## **Key Insights from the Analysis:**
1. **Customer Trends:**  
   - Transient customers form the majority but cancel frequently.  
   - Online TA is the most common distribution channel but sees high cancellations.

2. **Seasonality:**  
   - Summer months show a booking surge.  
   - Winter months show lower demand.

3. **Cancellations by Deposit Type:**  
   - `No Deposit` bookings have the highest cancellations.  
   - Ensuring deposits can reduce cancellations.

4. **Hotel Insights:**  
   - City hotels face higher cancellations.  
   - Resort hotels cater to customers who often make special requests.

5. **Pricing (ADR):**  
   - Higher ADR values often correlate with lower cancellation rates.  

---

### **Next Steps for Deeper Analysis:**
1. Analyze the relationship between `lead_time` and cancellations.
2. Study geographical trends by visualizing `country` distribution.
3. Model predictions for cancellations using machine learning.  

Would you like detailed insights on any specific chart or deeper analysis?
