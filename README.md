# **Classification - Tata Steel Machine Failure Prediction**
**Unguided capstone project**

Context - In the manufacturing sector, maintaining the efficiency and reliability of machinery is critical to achieving optimal production quality and minimizing downtime. TATA Steel, a leader in the steel manufacturing industry, is constantly looking to improve its production processes by leveraging advanced data analytics and machine learning techniques. The ability to predict and prevent machine failures is crucial for minimizing production losses, reducing maintenance costs, and ensuring product quality.

The dataset provided in this project represents various operational parameters and failure types of machinery used in steel production. The data is synthetically generated based on real-world scenarios, allowing us to explore different machine learning techniques to predict potential failures. By analyzing this data, TATA Steel aims to develop predictive models that can anticipate machine failures before they occur, thus enabling proactive maintenance and improved operational efficiency.

## **Hypothetical Business Objective**

 - TATA Steel aims to develop predictive models that can anticipate machine failures before they occur, thus enabling proactive maintenance and improved operational efficiency.

 - **How will the solution be used?**
     - To predict machine failure before its occurance.
     - Maintenance will then prevent a major damage that would have been caused due to machine failure to the machine as well as the supply chain delay.

 - **Current solutions?**
     - Manual inspection would probabily the current solution used in the factory.
   
 - **Framing the problem**
    - It is a Supervised Learning problem as labels are given.
    - It is a Classification problem as we require output whether maintainance is needed or not.
    - It is a binary classification problem.
 - **Assumptions**
    - We need categorical output i.e wheather machine needs maintenance or not , binary 0 and 1.

# **Model Summary**  

## **What was our goal?**  
- We needed a machine learning model capable of predicting **machine failures in advance** so that preventive measures could be taken.  

## **Did our model achieve that goal?**  
- **Yes**, we successfully built two models capable of predicting machine failures.  

## **What is the performance?**  
- **Random Forest:**

  - Achieves a **recall of ~76.7%** at **99% precision** and **F1 Score of 86.5**.
  - Achieves a **recall of ~90%** when tuned to a threshold of **0.13094**, with a **precision of ~90%** and an **F1 score of 0.899**.   
  - A higher false positive rate (lower precision) could also lead to **unnecessary downtime**, impacting operational efficiency.  

- **XGB Classifier:**  
  - Performs similarly, with a **precision of ~99%**, a **recall of 76.6%**, and an **F1 score of 86.4%**
  - Achieves a **recall of ~80%** when tuned to a threshold of **0.15502**, with a **precision of ~92%** and an **F1 score of 0.857**. 
  - Increasing recall further is possible, but it would come at the cost of a **significant drop in precision**. 

## **Which model should we pick?**  
- Both models perform similarly, but if thresholds are tuned the recall can be increased to 90% in case of **Random Forest** on optimal precision of 90%.  
- The choice depends on **available computational resources** and **processing power** required for deployment.  

## **How can we improve the model further?**  
- **Hyperparameter tuning:**  
  - We could explore a broader range of hyperparameters and use larger number of optuna trials, though this would be **computationally expensive** and time consuming.  
- **Handling class imbalance:**  
  - We could try **SMOTE (Synthetic Minority Over-sampling Technique)** for balancing the dataset, though we have already applied proper techniques in hyperparameter tuning.  
- **Feature engineering:**  
  - The **ProductID** column could be processed by **removing letters** and replacing them with empty spaces to extract numerical patterns.  
- **Feature selection:**  
  - We could attempt to **remove redundant features** and retrain the model. However, this may not yield a **significant performance boost**.  

