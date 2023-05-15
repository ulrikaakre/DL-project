## Project proposal form

Please provide the information requested in the following form. Try provide concise and informative answers.

**1. What is your project title?**

Exploring neural network architectures on time series prediciton

**2. What is the problem that you want to solve?**

One group member works part time in a company that we can get data from. That is a retail company that spends much of its resources on staffing employees. As having too many or too few employees working in at a given day is a waste of their resources, the problem would be to optimize this staffing. Using historical data on number of visitors and number of employees working at a given time in a given store, we have historical data on the previous optimization for many years. Plotting this as a time-series, one can use time series prediction algorithms to predict the staffing and save money for the business. Exploring the accuracy of deep learning algorithms on this case with *real world data* is the problem we are seeking to solve. The fact that we use real data will probably make the model have somewhat lower accuracy than if we were to used a cleaned and fixed dataset on Kaggle, however, we believe it will be of good learning and very interesting to see how it actually can be useful in business.

We hope, and take as an assumption, that it is not sheer accuracy of the model that is evaluated for the project grade, but the reasoning behind and sophistication of the architecture itself. If this is mistakenly assumed, please provide feedback.

**3. What deep learning methodologies do you plan to use in your project?**

Given the problem as a time series prediction problem, we will explore with the efficiency of different RNNs and transformer-based models. The more well-known architectures of RNNs, such as Long Short-Term Memory (LSTM) will be implemented as a basis of performance. Then, we will implement a transformer-based model and compare results to figure out which model that works best in this context.

**4. What dataset will you use? Provide information about the dataset, and a URL for the dataset if available. Briefly discuss suitability of the dataset for your problem.**

The dataset consists of customer visiting data and staffing data broken down into 30-minute slots. That gives us approximately 25000 rows (slots pr half hour), or 1500 rows when aggregated to whole days (right under 4 years of data). Given the nature of the problem, it does seem like it is fitting to use for a time series prediction algorithm. We have briefly discussed with the company and they agree that it should be a good use case for us to practice developing a time series model. 

A snippet of the dataset is below:

| time (id)                  | n_visits | n_shifts | n_cancellations | n_rooms | n_active_rooms | utilization |
|----------------------------|----------|----------|-----------------|---------|----------------|-------------|
| 2020-06-03 10:36:00.000000 | 0        | 0        | 0               | 2       | 2              | 100%        |
| 2020-06-03 18:30:00.000000 | 0        | 1        | 0               | 2       | 1              | 0%          |
| 2020-06-03 18:00:00.000000 | 1        | 2        | 1               | 1       | 1              | 50%         |
| ... | ...        | ...        | ...               | ...       | ...              | ...         |

Example images of plotted data with some applied smoothing (number of treatments on y-axis, date on x-axis):

<img src="https://github.com/lse-st456/project-2023-group-10/blob/main/time-series-1.png" width="300">

<img src="https://github.com/lse-st456/project-2023-group-10/blob/main/time-series-2.png" width="300">

**5. List key references (e.g. research papers) that your project will be based on?**

- https://warwick.ac.uk/fac/soc/economics/staff/lsilvaparanhos/paper_neuralnets.pdf
- https://towardsdatascience.com/how-to-use-transformer-networks-to-build-a-forecasting-model-297f9270e630#:~:text=Transformers%20are%20currently%20very%20popular,used%20for%20time%20series%20forecasting
- https://royalsocietypublishing-org.gate3.library.lse.ac.uk/doi/full/10.1098/rsta.2020.0209
- https://doi.org/10.1016/j.procir.2021.03.088
- https://ieeexplore-ieee-org.gate3.library.lse.ac.uk/stamp/stamp.jsp?tp=&arnumber=8437249
- https://doi.org/10.1016/j.cageo.2022.105126
- https://dl-acm-org.gate3.library.lse.ac.uk/doi/pdf/10.1145/3533382

**Please indicate whether your project proposal is ready for review (Yes/No):**

YES

## Feedback (to be provided by the course lecturer)

[MV 2nd April 2023] Project topic approved. For a baseline model for comparison, you may compare against traditional time series models such as ARIMA. I expect that your report will well explain any neural network architectures, training, and evaluation methods used. The problem formulation could have been more clear in explaining the prediction problem -- I understood you would consider prediction problems such as predicting the number of customer visits based on historical data. You may consider a multivariate time series forecasting if appropriate for your problem.
