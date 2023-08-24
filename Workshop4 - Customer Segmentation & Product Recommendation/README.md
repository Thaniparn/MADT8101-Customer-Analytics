# :white_check_mark: Workshop4 - Customer Segmentation & Product Recommendation
## Objective
HDI is a family of companies with established businesses in various industries.  Company would like to leverage data-driven insights to enhance customer understanding, optimize business strategies, and drive informed decision-making across various departments within the organization.

### Customer Segmentaion
Notebook: [Customer Segmentation](https://github.com/Thaniparn/MADT8101-Customer-Analytics/blob/3c4c7237beebf777b05eb25615b8f4790ab733cb/Workshop4%20-%20Customer%20Segmentation%20%26%20Product%20Recommendation/HDIAnalyticSegmentation.ipynb)

Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Thaniparn/MADT8101-Customer-Analytics/blob/main/Workshop4%20-%20Customer%20Segmentation%20%26%20Product%20Recommendation/HDIAnalyticSegmentation.ipynb)

### Product Recommendation
Notebook: [Product Recommendation](https://github.com/Thaniparn/MADT8101-Customer-Analytics/blob/3c4c7237beebf777b05eb25615b8f4790ab733cb/Workshop4%20-%20Customer%20Segmentation%20%26%20Product%20Recommendation/HDIAnalyticProdRecommendation.ipynb)

Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Thaniparn/MADT8101-Customer-Analytics/blob/main/Workshop4%20-%20Customer%20Segmentation%20%26%20Product%20Recommendation/HDIAnalyticProdRecommendation.ipynb)

## Customer Segmentation
1. Only non-churner customers are selected to analyse.
   
   Non-churner customers defintion is customers who have transaction in the last 3 months.
   
2. Create features for 3 dimensions for segmentation
   
   a. Dimension 1: Customer spending
   
   b. Dimension 2: Purchase frequency
   
   c. Dimension 3: Social network analysis
   
   This is heatmap result for all features (all dimensions)
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/8146eba3-66d1-4aab-8bb2-9861506ec7f6)
   
3. K-Mean in each dimension
   a. Dimension 1: Customer spending
   
     - Spending group 0 - Low spending
   
     - Spending group 1 - Agressive spending in online
   
     - Spending group 2 - Agressive spending in offline
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/83ee1ea2-3a5c-42ba-906b-5574b8d3dee5)
   
   b. Dimension 2: Purchase frequency
   
     - Frequency group 0 - Low
   
     - Frequency group 1 - High
   
     - Frequency group 2 - Moderate
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/2e46262e-f4b2-44d8-a180-7e25ebe13a07)
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/d0b38b10-fbcf-484b-b354-b4df070ab815)
   
   c. Dimension 3: Social network analysis
   
     - SNA group 0 - Low-level upline
   
     - SNA group 1 - High-level upline
   
     - SNA group 2 - Mid-level upline
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/5a01b799-92c8-4422-9f6d-89bf75fdebb6)
   
4. Final classification result with number
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/4b9ed3f7-c91a-4210-a59f-68fbdb71ac42)

## Product Recommendation
1. Transaction criteria for this analysis are:
   
   a. Transaction amount should be more than 0
   
   b. Purchase member should be in below segment
   
       - Spending group 0 - Low spending
   
       - Frequency group 0 - Low
   
       - SNA group 0 - Low-level upline
   
2. Use Apriori for analysis
    
       - Filter: Support should be equal or more than 0.2
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/c75588a6-8974-46e2-9345-650394dd0f98)
   
3. Finding association rule
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/bbabe5f1-1579-475f-ae1e-733519cc2780)
   
   ![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/b2dd68ed-39c7-42e3-a710-497b14f8281f)

