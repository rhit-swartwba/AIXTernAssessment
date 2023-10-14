# AIXTernAssessment

Given the data set, do a quick exploratory data analysis to get a feel for the distributions and biases of the data. Report any visualizations and findings used and suggest any other impactful business use cases for that data.

I did a quick exploratory analysis by plotting each data column on a histogram. Based on this quick exploration, there are a few worrying trends. All the students are Year 3 and Year 2 students, mainly in Year 2. So this data is not representative of all college students, but just these specific years. Therefore, this model cannot be used as a general predictor for all college students. Secondly, certain majors are sampled much more than others. For example, Chemistry and Biology majors are very heavily sampled, while other majors such as engineering and computer science are hardly taken into account. This represents bias in the data towards certain majors. Furthermore, most of the data was taken from 4 colleges like Butler and Indiana State University. The count for these are 1000+, but other colleges have much fewer students sampled. Therefore, this data is not representative of all colleges in Indiana and is biased to a few. Fortunately, the distribution of orders is even which is good for making sure the tested values are equally represented. There are certain times when orders are made more often than others, but this makes sense. 

Consider implications of data collection, storage, and data biases you would consider relevant here considering Data Ethics, Business Outcomes, and Technical Implications.

Discuss Ethical implications of these factors

Data bias is an important ethical factor in avoiding discrimination against underrepresented groups. If models are geared toward being better predictors of some groups over others, then this is unfair and ethically immoral. This is relevant here because there are heavy biases in the data, and an ethical mapping of participants would be very useful. FoodX needs to have make sure they are morally inclusive for all students. Furthermore, for data collection, it is important that all the data taken was given with consent to make sure it was ethical and signs were posted where students ordered to acknowledge this. This data also has to be stored safely and anonymized (if orders had names to them, etc.) so that it is secure and away from others. Also, no data is leaked and no names and confidential information should be stored or kept.
   
Discuss Business outcome implications of these factors

There are legal rules when it comes to collecting data. Businesses have their own rules, but the government does as well. Since I am more acquainted with research, I know the IRB rules for data collection and how any research project needs IRB approval to be published. I am sure there is a similar set of rules for taking data and storing it as well in business. Businesses cannot sell or give away information, even as something small as this project with what students are ordering. Also, if a business does violate and leak data, this can destroy a business's reputation. Customers will no longer buy the product and may believe that the company is biased towards certain groups. If FoodX's model seems to be biased and students see it, this could lead to FoodX going out of business.

The most obvious outcome, if data is biased, is that products will not perform and sell as well as expected. This can lead to a loss of revenue and hurt the company financially. FoodX will lose a lot of money giving free discounts if their model is flawed.
   
Discuss the Technical implications of these factors

The model, collection of data, and its storage have to be done very well. The technical choice of model and way of collecting data has to be efficient and technically easy to use and parse for this program to be effective. 


Build a model to predict a customers order from their available information.  You will be graded largely on your intent and process when designing the model, performance is secondary. It is strongly suggested that you use SKLearn for this model as to not take too much time.  You may use any kind implementation you would like though, but it must be pickelable and have a “.predict()” method similar to SKLearn

Outline your process for model selection, training and testing. Including data preparation.

The final predictor of this data is different categories of orders. We are grouping data based on this - thus, this is a multiclassification problem. With my prior knowledge, I know that random forests can solve this, and I know how to implement this. I actually have a class assignment on a problem very similar to this, and thus I used that given template from school to implement this to save time. Thus, I will use this. I decided on a standard 0.7 training and 0.3 testing data split. For data preparation, I know I should use some kind of encoding for the categorical variables. I chose one-hot encoding in the second version of my model. For Year, I also looked up online a quick way to parse the year number so the data is easier to get. In hindsight, I could have just done my own replacing method. The x data is all the other categories, but the y data is for the orders because that is what we are trying to predict. I also printed out the accuracy for the data and the f1 score to make sure the recall and precision of my model was balanced. I also displayed the confusion matrix so we could see the predictions versus the true labels of the data for a quick sketch of accuracy.

I did not design a specific function because my current design worked fine with the template I followed from my previous assignment. I just used a pandas dataframe to get the data and split it into X and Y as mentioned above.

Again, I just used the prebuild scikit learn methods to run it. This followed my template, and also I know how to use these methods from a LinkedIn Learning course I took online on scikit learn specifically. 

I sent my visual data code and the initial neural network and then the one I adapted from my project in one file. 

Done

Given the work required to bring a solution like this to maturity and its performance, what considerations would you make to determine if this is a suitable course of action?

I would first make sure that the model is overall more accurate. I would also run some financial analysis based on the model accuracy to see if the 10% discount vs the increase in the number of purchases with this offer is actually returning a profit to the company. There should be a threshold accuracy level to make sure that this plan and model will be profitable. The model definitely needs more tuning than 1-2 hours of work and can be fine-tuned to be improved. The biases in the data collection also should be addressed to determine if the model is used. As of now, this model is far from applicable - but it is a good start. 


