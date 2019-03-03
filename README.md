# ml-prediction-skip-action

If you want to see the further ML projects, you may visit my main repo: https://github.com/erdiolmezogullari/ml-projects

![Image](https://raw.githubusercontent.com/erdiolmezogullari/ml-prediction-skip-action/2c3d0dcef096a475c6bf214c71cab23a22fd6bf8/img/waiting_time.jpg)

Since we don't have any class already labelled and any continuous target variable, we need to pick a feature for our target feature to predict skipping action of listener. According to the features we created, `per_listen` will be more suitable for that problem since it obviously gives idea about skipping action. If we pick it as a target feature, this problem will turn out a scoring/probability problem because of having ratio of listening time, which tends between 0 to 1.

If we want to convert that problem to a classfication problem, we can determine a treshold for skipping aciton as a rule of thump. `per_listen` denotes how much percentage of the track that were listened by listener. So, our threshold could be 25%, 50% even 51% and so on. However, before making a decision, we can check out Complementary Cumulative Distribution Function (CCDF) of  `per_listen`. It would be give an idea about our reasonanle threshold. According the following plot, we have 65% of instances, whose per_listen value is greater than 0.5. Therefore, 0.5 is reasonable, however, when we think about it more realistic, less than 0.5 around 0.25 would be more suitable determine any skipping action.
