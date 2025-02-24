# **Classification - Tata Steel Machine Failure Prediction**
**capstone project**

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

   ## **Model Summary**  

## **What was our goal?**  
- We needed a machine learning model capable of predicting **machine failures in advance** so that preventive measures could be taken.  

## **Did our model achieve that goal?**  
- **Yes**, we successfully built two models capable of predicting machine failures.  

## **What is the performance?**  
- **Random Forest:**  
  - Achieves a **recall of ~80%** when tuned to a threshold of **0.11247**, with a **precision of 92.2%** and an **F1 score of 85.7%**.  
  - This means the model correctly predicts machine failures **80% of the time** and identifies negative instances correctly **92.2% of the time**.  
  - Increasing recall further is possible, but it would come at the cost of a **significant drop in precision**.  
  - A higher false positive rate (lower precision) could lead to **unnecessary downtime**, impacting operational efficiency.  

- **XGB Classifier:**  
  - Performs similarly, with a **precision of ~91%**, a **recall of 80%**, and an **F1 score of 85.2%** when tuned to a threshold of **0.12083**.  
  - Its behavior is **comparable to the Random Forest model** in terms of trade-offs between recall and precision.  

## **Which model should we pick?**  
- Both models perform similarly, but **Random Forest has a slight edge** in performance.  
- The choice depends on **available computational resources** and **processing power** required for deployment.  

## **How can we improve the model further?**  
- **Hyperparameter tuning:**  
  - We could explore a broader range of hyperparameters using advanced tuning methods, though this would be **computationally expensive**.  
- **Handling class imbalance:**  
  - We could try **SMOTE (Synthetic Minority Over-sampling Technique)** for balancing the dataset, though we have already applied proper techniques in hyperparameter tuning.  
- **Feature engineering:**  
  - The **ProductID** column could be processed by **removing letters** and replacing them with empty spaces to extract numerical patterns.  
- **Feature selection:**  
  - We could attempt to **remove redundant features** and retrain the model. However, this might be **time-consuming** and may not yield a **significant performance boost**.  


