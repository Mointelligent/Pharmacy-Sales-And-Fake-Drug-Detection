# Pharmacy Sales & Fake Drug Detection Analysis 💊📊

This project focuses on analyzing pharmacy sales patterns in Nigeria to detect potential counterfeit and substandard drugs in the pharmaceutical supply chain. The analysis encompasses data cleaning, SQL analysis, Power BI visualizations, and identification of anomalies that could indicate fake drug distribution.

## Project Overview

The primary goal of this project was to detect anomalies in pharmacy sales that may signal the presence of fake drugs, and to provide actionable insights for stakeholders. This involved:

* **Data Cleaning and Initial Analysis (Excel):** 🧹 Preparing raw pharmacy sales data, handling errors, duplicates, and inconsistencies for further analysis.
* **Anomaly Detection & Deeper Analysis (SQL / Excel):** 🔬 Assigning risk scores for price, quantity, and expiry to identify high-risk transactions and suspicious patterns among pharmacies, brands, and suppliers.
* **Data Visualization (Power BI):** 📈 Creating interactive dashboards to summarize high-risk transactions and trends across urban and rural areas.
* **Interactive Dashboard (Power BI):** 🖥️ Developing a dashboard for stakeholders to monitor pharmacy sales anomalies and potential fake drugs.

## Project Structure

* `data/`: Contains raw and cleaned pharmacy sales datasets (Excel files).  
* `notebooks/`: SQL queries, Excel calculations, and analysis documentation.  
* `powerbi/`: Power BI project files (.pbix) and related assets.  
* `images/`: Screenshots or exports of the Power BI dashboard.  
* `README.md`: This file.

## Analysis and Methodologies

### 1. Data Cleaning (Excel)

* **Original dataset:** 10,057 rows × 12 columns  
* **Cleaned dataset:** 10,001 rows × 22 columns  
* **Cleaning steps:**  
  - Removed 5 rows with errors  
  - Deleted 51 duplicate rows  
  - Corrected spelling inconsistencies  
  - Verified no missing values  

---

### 2. Risk Scoring & Anomaly Detection (Excel / SQL)

* Each transaction (row) had a unique batch number.  
* Total transactions: 10,000  
* Assigned **risk scores** for each transaction:  
  - **Price risk:** 1 if price < 70% of average price for that drug; 0 otherwise  
  - **Quantity risk:** 1 if quantity > 1.5 × average quantity; 0 otherwise  
  - **Expiry risk:** 1 if sold <180 days to expiry; 0 otherwise  
* Calculated the percent of transactions flagged as high risk.  

---

### 3. Data Insights

* **Price anomalies:** 33.74% of transactions show price risk → possible supply chain manipulation  
* **Quantity anomalies:** 24.68% of transactions flagged  
* **Expiry anomalies:** 0.22% of transactions flagged  
* **Pharmacies with high-risk sales:** Blake and Sons showed the most price anomalies  
* **Unknown brands with high sales:**  
  - Hea1thFirst (20.2k)  
  - Biokare (19.6k)  
  - Medipluz (19.0k)  
  - FarmaTrust (18.8k)  
  These brands pose high health risk due to unknown origins  
* **Suppliers linked to anomalies:** Supplier Jones Inc showed the highest anomalies due to inconsistent pricing strategies and expiry manipulation  
* **Urban vs Rural Sales:** Rural areas accounted for 50.53% of sales; Urban areas 49.47%  
* **Drug-specific insights:** Amoxicillin had the highest number of drugs sold close to expiry  

---

### 4. Recommendations

**Short-Term:**  
* Increase routine inspections of brands, pharmacies, and suppliers  
* Prioritize high-risk pharmacies, suppliers, and brands for investigation  
* Enforce mandatory licensing and renewal  
* Ensure presence of licensed pharmacists  
* Sensitize pharmacies to detect counterfeit drugs  
* Educate the public about fake drugs  

**Long-Term:**  
* Update drug laws to reflect modern threats  
* Implement a national end-to-end drug traceability system  

---

### 5. Conclusion

* Counterfeit and substandard drugs pose a significant threat to public health in Nigeria.  
* Analysis revealed **pricing, quantity, and expiry anomalies** across suppliers and pharmacies.  
* Some drugs were sold near expiry, while some unknown brands had high sales volumes.  
* Addressing these risks through **inspection, verification, and public education** is crucial to protect public health.  

---

## Power BI Dashboard

Below is a snapshot of the interactive Power BI dashboard, showcasing pharmacy sales anomalies and potential fake drugs:

![Pharmacy Dashboard](images/dashboard.png)

Key metrics visualized:  
* Total high-risk transactions by Price, Quantity, and Expiry  
* Top pharmacies with anomalies  
* Brand-level sales and risk trends  
* Supplier anomalies  
* Urban vs Rural comparison  
* Drug-specific expiry risks  

---

## How to Run/View the Project

1. **Clone the Repository:**
```bash
git clone https://github.com/YourUsername/Pharmacy-Sales-Fake-Drug-Detection.git
cd Pharmacy-Sales-Fake-Drug-Detection

View Power BI Dashboard:

Download and install Power BI Desktop


Open powerbi/PharmacyDashboard.pbix in Power BI Desktop to interact with the dashboard.

Explore Analysis Files:

Open Excel sheets or SQL scripts in the data/ and notebooks/ directories to see risk scoring and anomaly analysis.

Technologies Used

Microsoft Excel 📝

SQL 🐍

Power BI 📊

Contact

For any questions or collaborations, feel free to reach out:

LinkedIn: www.linkedin.com/in/modupeaderibigbe/
