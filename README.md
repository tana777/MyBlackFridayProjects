

This is my approach on [Analytics Vidhya Black Friday hackathon](https://datahack.analyticsvidhya.com/contest/black-friday/). You can find a complete step-by-step analysis on the issue as well as my Python code and conclusions.


## Machine Learning Project Checklist
My machine learning project workflow mainly includes the following parts and it also shows how I tackle this series of problems. Suppose we get the dataset, then start our journey and let the data lead us and see what information could we get and how to accomplish the task.


- **Frame the Problem**

 1. Specify business objective.
 2. Transform the problem that can be addressed using data and ML algorithms.<br>
 (Supervised/Unsupervised, classification/regression/clustering, online/offline, etc.)?<br>
 
 The right set up is often more important than the choice of algorithm. Make sure you are solving the right problem.

- **Get the Data**<br>

  Build robust dataset to solve real-world problems and see how your data preparation ultimately impacts how effective you models are.
 1. List the data you need and how much you need.
 2. Try to collect the data and check the size and type of data.
 3. Some problems you might meet like imbalanced data.
 4. Sample a test set and never touch it until last moment.
  

- **Explore the Data**

 1. Study each attribute and its characteristics: Name, Type, % of missing values, Noisiness, Type of distribution, etc.
 2. Visualize the data involving a bunch of plot.
 3. Study the correlations between variables.
 4. Identify the promising transformations you may want to apply.
 5. Gain insights for feature engineering.
 6. Identify extra data that would be useful and go back to 'Get the Data'.
 

- **Prepare the Data**
 1. Data cleaning:
    - Fix or remove outliers.
    - Fill in missing values or drop their rows or columns.
 2. Feature selection<br>
   More features may not lead to a better-fitted model. Pay attention to the curse of dimensionality. If needed, drop the features that provide no useful information for the task.
 3. Feature engineering<br>
 
    Building better features is after data, the second most important way to impact Machine Learning performance. Feature engineering is how we take our knowledge about the world and encode it into a format that our model can leverage effectively. Coming up with new features is difficult and time-consuming, it needs domain knowledge or familiarity with your dataset. However, deep learning blurs the difference between the features and the model. In general, feature engineering includes:
    - Discretize continuous features
    - Decompose features like categorical, date/time, etc.
    - Add promising transformations of features like log(x), sqrt(x), x^2, etc.
    - Aggregate features into promising new features.
    
  4. Feature scaling: standardize or normalize features.
  5. Partition data. According to your concrete situation, split the dataset into train, validation and test set. Make sure every set should work properly.
  
- **Evaluate Model Performance**

  For a specific task, we have various metrics as candidates like accuracy, error, AUC or F score. Choosing the most proper one that helps us identify what it means to be successful and how to measure it. The metric should be consistent with your business goal or your task.



- **Short-List Promising Models**

 1. Train many quick and dirty models from different categories using standard parameters.
 2. Measure and compare their performance.
 3. Analyze the most significant variables for each algorithm.
 4. Analyze the types of errors the models make.
 5. Have a quick round of feature selection and engineering.
 6. Have one or two more quick iterations of the five previous steps.
 7. Short-list the top three to five most promising models, preferring models that make different types of errors.
 
    Ideally, features and data should govern model choice. A good understanding of statistical learning and the fundamentals of the different algorithms can help make the choice naturally, but we also need to think about tradeoffs. 
For model, sole objective is reducing the loss on the test set as far as possible. For the real world, a few areas we should think about are:
interpretability and ease to debug, data volume, and training and prediction considerations.

- **Fine-Tune the System**
 1. Fine-tune the hyperparameters using cross-validation with Random search or Grid search.
   Hyperparameters are not only about models but also about your data transformation choices, especially when you are not sure about them. For example, the way you treat missing values or converting formats you use.
 2. Try ensemble methods. Ensemble can usually boost performance and often perform better than running them individually. But be observant of making the tradeoff between precise prediction and time cost.
 3. Measure the final model on the test set to estimate the generalization error.
 
 
- **Present Your Solution**
 1. Make sure you highlight the big picture first.
 2. Explain why your solution achieves the business objective.
 3. Describe what worked and what did not.
 4. List your assumptions and your system's limitations.
 4. Ensure your key findings are communicated through beautiful visualizations or easy-to-remember statements.
 

 Tips: <br>
 Once you start to explore the dataset, stick to your pipeline and order end to end and let the data tell you how to change your process. Iterate the previous steps because, from my own perspective, data science is about an iterative process with your model performance improving or decreasing over time until you get the best one you could obtain. 


*Nothing ever becomes real till it is experienced.* <br>
*-John Keats*

#### Reference:
Book: Hands-On Machine Learning with Scikit-Learn and TensorFlow <br>
http://shop.oreilly.com/product/0636920052289.do<br>
https://research.fb.com/the-facebook-field-guide-to-machine-learning-video-series/ <br>
