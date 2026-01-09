# Exploratory Data Analysis (EDA) Report :   
## Amazon Sales Dataset

## 1. Project Objective

The primary mission of this analysis is to transform raw transaction logs into a **Strategic Growth Roadmap**. By moving beyond basic data cleaning, we have identified high-velocity categories and geographic **power centers**. This report serves as the foundation for **Revenue and Sales Optimization**, focusing on where the business can achieve the highest return on investment.

## 2. Data Overview & Integrity

Our analysis is built on a robust dataset of **128,975 transactions**. To ensure the integrity and reliability of insights, the following data hygiene steps were performed:

- **Standardizing Geographic Data:**  
  Merged duplicate city entries caused by case-sensitivity and typos.

- **Financial Engineering:**  
  Created the `Total_Revenue` metric to reflect true cash flow beyond simple unit counts.

- **Cleaning:**  
  Removed redundant system-generated columns to maintain a lean, high-performance data model.

## 3. Statistical Summary & Core Insights

- **The "Standard" Purchase Pattern:**  
  Since both the 50th and 75th percentiles for `Qty` are exactly **1**, the vast majority of customers are purchasing single items. This highlights a strong opportunity to deploy **"Frequently Bought Together"** or bundle-based recommendations to increase the average quantity per order toward **2**.

- **Stable Pricing Sweet Spot:**  
  The close alignment between the **Mean (₹589)** and **Median (₹568)** order values indicates a highly stable pricing environment. Customers consistently demonstrate comfort within the **₹400–₹800** spending range, clearly defining the platform’s core price-sensitive market segment.

- **Whale Orders (B2B Potential):**  
  Although the typical order size is small, extreme outliers—**Max Revenue of ₹44,672** and **Max Quantity of 15**—signal the presence of high-value **"whale" customers**. These transactions are likely driven by B2B buyers or boutique owners. Proactively identifying and nurturing these accounts presents a high-impact growth lever with **minimal customer acquisition cost**.

## 4. Revenue Trends: The Pulse of the Business

Revenue behavior is dynamic rather than linear.

- **Everyday Trends:**  
  Daily revenue trends exhibit multiple spikes, indicating strong responsiveness to short-term triggers such as promotions and weekends.

- **The Pricing Lever:**  
  A strong **0.84 correlation** between `Unit_Price` and `Total_Revenue` reveals a critical truth:  
  **Growth is driven by value(price), not volume(quatity).**

  To double revenue, it is more efficient to move a customer from a low-value *"Top"* to a high-value *"Set"* than to acquire two separate customers for *"Tops"*.

## 5. Category Trends: 

- **The Volume Engine:**  
  *Kurtas* are the major sold clothes, driving the highest unit sales and ensuring consistent brand visibility.

- **The Revenue Engine:**  
  *Sets* and *Western Dresses* are financial heavyweights. Despite lower unit volumes, their higher price points contribute disproportionately to total revenue.

- **Strategic Play:**  
  Kurtas should be positioned as the **entry product**, strategically funneling customers toward higher-margin *Sets*.

## 6. City Trends: Mapping the Volume Powerhouses

Our geographic sales are concentrated in a dominant **Top 5 city tier**, which consumes the majority of logistical capacity:

- **Bengaluru:** 11,038 units (undisputed volume leader)  
- **Hyderabad:** 8,284 units  
- **Mumbai:** 6,576 units  

**Concentration Insight:**  
The fact that the top 10 cities—ranging from Bengaluru to Noida—account for a substantial share of total quantity **(42.2%)** suggests a major opportunity to reduce shipping costs through focused, city-centric inventory placement.

## 7. Business Model Trend: The B2B Growth Lever

The most compelling insight emerges from the contrast between B2C and B2B performance.

### Efficiency Comparison

- **B2C (The Foundation):**  
  Drives **99.3% of order volume** with an AOV of **₹588.72**.

- **B2B (The Multiplier):**  
  Represents **<1% of orders** but operates at an AOV of **₹708.59**—nearly **20% higher value per shipment**.

### City-Specific B2B "Personalities"

Distinct B2B behaviors emerge across key hubs:

- **New Delhi – The Premium Market:**  
  Highest B2B AOV (**₹814**), with a clear preference for high-end *Sets* over basic Kurtas.

- **Noida – The Wholesale Hub:**  
  B2B revenue leader (**₹63,306**), moving the highest number of units and acting as the core bulk ethnic-wear channel.

- **Mumbai – The Trend Setter:**  
  Dominates B2B *Western Wear*, signaling a more modern and fashion-forward retail partner ecosystem in the West.

## 8. Conclusion & Strategic Roadmap

The data communicates a clear strategic direction: **5 cities and 2 categories define the backbone of the business.**

- **Double Down on B2B:**  
  Sustainable growth does not require millions of new customers. It requires deeper B2B penetration in high-volume hubs like Noida.

- **Product–City Alignment:**  
  Move away from generic catalogs.  
  - Western-focused assortments for **Mumbai**  
  - Set-focused assortments for **Delhi NCR**

- **Logistical Focus:**  
  With **Bengaluru** and **Hyderabad** handling the highest shipment volumes, ensuring faster fulfillment in these hubs is critical to protecting volume leadership.


