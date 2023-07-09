# :white_check_mark: Workshop4 - Churn Prediction
## Dataset
Retail information contains sales transaction and repondings information per customer.

Notebook: [RetailChurnPrediction]()
Google Colab: Open In Collab

### Example of result:
Sales transaction
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/65ceafc9-016f-40d6-b210-a180bb53e023)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/6ffd9045-dcb4-40c2-8cd4-8a6dca266ec6)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/370af840-e464-4915-af2a-c38bf19281c5)

### Define churn value:
Below concept is used in this model.
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/ffd16aaf-f6ef-40cc-a351-0b3703c8e9f9)

3 month is used for churner target period, if they don't purchased a product in this time frame. Average time between perchase in each customer by transaction is about 73 days. Then, we assume to use 3 months in this case.
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/30a0fc58-51fa-495b-a8bd-9ef8783ea3a6)

### Define feature:
1. Recency (No. of days)
2. Frequency (Times)
3. Monetary Value (Spending amount)
4. Response (Yes/No)

Training datset validation
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/43e11b0e-c2db-42da-8e7a-3f4a51d16f7a)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/25fbfea9-a1db-4947-8fe8-a5668c0cd20d)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/896bdb0f-7ebe-4023-9cdc-9ca3f3e9f101)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/28ef0032-d03a-4800-b74b-67b527a263d0)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/cd209ef7-2450-41ac-8f33-086755782690)
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/6bc1f6fc-60d0-4942-960e-7505f340e5f1)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/af9f2479-0dab-44b9-8de2-97c6847285e7)
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/cac0c581-5931-483c-ab61-b424f2a86ef0)

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/3b8c7825-29dc-47db-9f81-fc094d356491)
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/827bdf5c-ccfb-456e-ae7a-3a56ba2aecc6)

### Training result:
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/7cc7ad1b-9bfb-4b4d-bdf5-a3281dc6983f)


