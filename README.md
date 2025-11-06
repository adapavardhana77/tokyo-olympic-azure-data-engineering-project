---

# **DETAILED PROJECT DOCUMENTATION**

## **1. Creating the Azure Resource Group**
The first step is to create a **Resource Group** that holds all Azure resources (ADF, Databricks, Storage, Synapse, etc.).  
This ensures organized resource management and easy cost tracking.

---

## **2. Creating Azure Storage Account and Container**
Next, a **Blob Storage account** is created. Inside it, a **Container** is made to store CSV datasets related to the Tokyo Olympics.

---

## **3. Uploading Datasets**
Datasets such as:  
- Athletes.csv  
- Coaches.csv  
- EntriesGender.csv  
- Medals.csv  
- Teams.csv  

are uploaded into the container. These files are used for transformation and analysis.

---

## **4. Setting Up Azure Data Factory (ADF)**
Azure Data Factory is used to **orchestrate** data movement and transformation.

### **Steps:**
- Created Linked Services for Blob Storage, Databricks, and Synapse.  
- Created Datasets for each CSV file.  
- Built a pipeline to copy raw data from **Blob → Databricks → Synapse**.

---

## **5. Data Transformation using Azure Databricks**
In this step, transformations are performed using **PySpark** in Databricks notebooks.

### **Examples:**
- Removing duplicates  
- Filtering rows with missing values  
- Joining multiple datasets  
- Aggregating athlete and medal information  

---

## **6. Loading Transformed Data into Synapse Analytics**
After transformation, the cleaned datasets are written into **Azure Synapse Analytics** for advanced querying and analytics.

---

## **7. Final Data Pipeline Workflow**
The final **ADF pipeline** integrates all the activities:  
1. Copy data from Blob to Databricks  
2. Transform data using Databricks  
3. Load processed data into Synapse  

This end-to-end flow ensures **automation** and **reusability**.

---

## **8. Results and Insights**
Once the pipeline executes successfully:  
- The data is transformed and stored in **Synapse tables**.  
- Analysts can now connect **Synapse** to **Power BI** or other visualization tools to generate reports on Olympic performance by country, gender, and event.

---

## **9. Key Learnings**
Through this project, I learned:  
- How to integrate **Azure services** for an end-to-end data solution.  
- How to use **Data Factory pipelines** for data orchestration.  
- How to perform large-scale data transformations in **Databricks**.  
- How to store and query structured data in **Synapse Analytics**.  

---

## **10. Power BI**
Integrated **Power BI dashboards** for visualization.

---

**This documentation clearly demonstrates the flow, screenshots, and outcomes of the entire Tokyo Olympics Data Engineering project.**

---
