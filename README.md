# Project Name
This project is NLP-Driven Stock Price Prediction and Market Analysis. 


Abstract:
 Stock prices are influenced by a multitude of factors, with the reaction of investors
 to news being one of the most significant. News headlines often contain keywords
 that summarize the emotion of an event, providing us with an opportunity to
 analyze how stocks would be affected for that day. Recognizing this
 interdependency, the objective of this project is to establish a meaningful
 correlation between news articles and stock prices.
 The project aims to provide a comprehensive analysis and develop a best-fit model
 for predicting stock prices. The study will examine the impact of news on stock
 prices, identifying the most influential news sources and the types of news that are
 most likely to impact stock prices. The research will also look at how quickly the
 market reacts to news, the duration of the effect, and whether any patterns emerge.
 To achieve this, we will collect data on news articles and stock prices for a
 specified period. We will then use machine learning algorithms to develop a
 predictive model to forecast stock prices based on news headlines. The model will
 be tested against real-time data to evaluate its effectiveness and refine it if
 necessary.
 Overall, the findings of this study will provide valuable insights into the impact of
 news on stock prices and contribute to the development of more accurate predictive
 models for stock market analysis. The project will be useful for investors, analysts,
 and financial institutions looking to make informed investment decisions and
 mitigate risks associated with the stock market.
 
Introduction
 The stock market is a complex and dynamic system that is influenced by a range of
 factors, including economic indicators, company performance, and global events.
 One of the most significant factors that can impact stock prices is the reaction of
 investors to the news. News headlines provide a snapshot of the sentiment and
 emotion surrounding an event, which can be a critical determinant of how stock
 prices will move.
 The use of news headlines to predict stock prices has been the focus of extensive
 research in recent years. With the availability of vast amounts of data and machine
 learning, it is now possible to extract valuable insights from news headlines to
 forecast stock prices.
 This project aims to explore the relationship between news headlines and stock
 prices, developing a predictive model that can be used to forecast stock prices
 based on news sentiment. The research will focus on identifying the most
 influential news sources, the types of news that have the most significant impact on
 stock prices, and the duration of the effect. By analyzing news data, we hope to
 gain a deeper understanding of the underlying factors that drive the stock market.
 The study will be useful for investors, financial analysts, and institutions looking to
 make informed investment decisions and manage risks associated with the stock
 market. By leveraging the power of machine learning, this research has the
 potential to provide valuable insights into the stock market's behavior and help
 investors make better-informed decisions.
 
Methodology
 This design may be logically divided into three parts, with the first column of
 blocks representing Phase 1 and the second column representing Phase 2,
 respectively. News stories with their polarity score are the phase 1 outcome. This
 outcome serves as phase 2's input. Phase 2 involves converting text into tf-idf
 vector space so the classifier can use it. The identical data is then programmed into
 three separate classifiers to compare the outcomes. At the conclusion of phase 2,
 we assess the outcomes provided by each classifier and test the effectiveness of
 each classifier for brand-new news items. Phase 3 involves looking for connections
 between news reports and stock price information. Using the R programming
 language, we plot the data and document the findings. Each building block of the
 design is discussed in the sections that follow.
 
Goals
 Here with the selected dataset, we are trying to understand the correlation
 of stocks as we have seen that many market trends are also related to
 multiple dips and rises in the stock market and impact our industry. Here we
 are trying to:- Todetermine whether there is a correlation between the daily news
 sentiments and the stock market performance of Reliance Industries.- Toanalyze the impact of positive or negative news sentiment on the
 stock market performance of Reliance Industries.- Toexplore the relationship between news sentiment and specific
 events or announcements related to Reliance Industries.- Toprovide insights for investors on how they can use news sentiment
 to make informed decisions about investing in Reliance Industries.- Tohighlight the limitations of using news sentiment as a predictor of
 stock market performance and provide recommendations for future
 research.
 Weintend to address and discuss these objectives throughout the paper,
 which define its direction and reasons.
 
Data
 The Kaggle Reliance Stock and News Data dataset is being utilized. This dataset
 contains daily stock market information from Reliance Industries as well as daily
 news items and news sentiments. This notebook, which is set to run daily, is
 created and maintained. This information can be used to inform stock market
 strategies or choices based on the tone of the news. It includes current stock market
 information, news stories, and their sentiment (positive, negative, or neutral). All
 of this information is appended to the input data before being exported to the
 dataset. This data set contains more than 600 new articles which have multiple data
 predictions based on the title and a description of the specific news article which
 will help us produce a prediction on how this affects the current stock market. We
 have also included a Yahoo Finance data set for more interactive and time analysis
 implementation which would help us draw out more trends and theories from the
 data and help us make informed decisions on the stock market.
 Stock Market Dataset: We have taken the dataset from Kaggle Reliance stock and
 News. The dataset has two CSV files and one JSON file. The news Sentiment
 Analysis was performed and the sentiment scores have been saved onto the
 sentiment analysis CSV file. We used this data and moved forward with the stock
 market prediction. For the second part of the project we have taken the data from
 Yahoo Finance, the reliance stock prices from 2014 to 2019.
 NewSentiment Analysis Dataset: We have taken the sentiment scores in the
 Reliance_news_sentiment.csv dataset for the stock prediction.
 
Pre-processing Workflow
 Here our basic idea was to start with Data cleaning Check for and remove any duplicated
 irrelevant, or missing data points. This can involve checking for duplicates across the entire
 dataset, removing any irrelevant or unnecessary data points, and imputing or removing missing
 values. And then Check for and remove any duplicated, irrelevant, or missing data points. 
 This can involve checking for duplicates across the entire dataset, removing any irrelevant or
 unnecessary data points, and imputing or removing missing values. 
 Clean and preprocess the text data by removing stop words, punctuation, or special characters, and performing stemming or
 lemmatization. This can involve using tools such as NLTK or spaCy to tokenize the text,
 removing stop words and punctuation, and performing stemming or lemmatization to normalize
 the text. 
 Scale and normalize the data to ensure that all variables have similar ranges, which can
 improve the performance of machine learning models. This can involve using techniques such as
 min-max scaling or standardization to normalize the data
 The preprocessing steps that we followed in our project were mostly done manually. We had 647
 rows in the News data set with sentiment scores, however we had only 57 rows for the stock
 market data during the same time frame. 
 The sentiment scores were given for 5 to 6 news articles on the same date, so we have decided to take the mean values of the sentiment scores on one
 given date and apply that for the stock prediction on the same date respectively. This step was
 taken in order to match the timeline of stock prices and news articles. During this process, we
 have shrunk the entire data into 57 rows. The dataset being very small, we didn’t encounter any
 issues such as missing values or NULL values.
 
 However, we did follow and perform functions to remove the missing and null values if there
 were any. Moving on, We removed a few unnecessary features such as Dividends and Stock To
 make the data more efficient. For the second Dataset that we used for the time-series analysis, we
 have taken the reliance stock data from yahoo finance from 2014 to 2019. We performed
 functions to remove the Null values and empty values to avoid the wrong visualization of data.
These steps were pretty easy to perform given the predefined functions on R: ‘ quantmod ‘ and ‘dplyr ‘

<img width="475" alt="image" src="https://github.com/user-attachments/assets/5d23adf4-4573-4bc6-b6b6-87efcfd8689b">

 
Exploratory Data Analysis
 Exploratory Data Analysis (EDA) is a critical step in stock market prediction as it
 enables researchers to understand the underlying patterns and relationships in
 the data. EDA involves visualizing and summarizing the data to identify potential
 trends, outliers, and relationships between the variables. By conducting EDA,
 analysts can discover critical features that may impact stock prices, such as market
 trends, economic indicators, or company-specific metrics. 
 Through EDA, researchers can also identify correlations between different variables and detect
 any multicollinearity issues, which can affect the accuracy of predictive models.
 In addition to identifying potential data quality issues, EDA can also help
 researchers identify key variables that may have a significant impact on stock
 market performance. 
 For example, by examining the correlations between different variables, analysts can identify potential drivers of stock prices, such as
 changes in interest rates, company earnings reports, or news events. One of the
 challenges of EDA in stock market prediction is dealing with the sheer volume of
 data. Stock market data can be extremely large, making it challenging to visualize
 and analyze effectively. To address this issue, researchers often use techniques
 such as sampling or dimensionality reduction to make the data more manageable.
 Another challenge of EDA in stock market prediction is dealing with the dynamic
 nature of the data. Stock market data is constantly changing, with new data points
 being added daily. This requires researchers to constantly update their EDA and
 predictive models to ensure that they are capturing the most up-to-date
 information. Despite these challenges, EDA remains an essential step in stock
 market prediction. By understanding the patterns and relationships in the data,
 researchers can develop more accurate and effective predictive models that can
 help investors make more informed investment decisions.
 
One of the key benefits of EDA in stock market prediction is that it helps
 researchers identify potential data quality issues. For example, missing values or
 outliers can significantly impact the accuracy of the predictive model. By using
 EDA techniques such as box plots, scatter plots, and histograms, analysts can
 identify and address these issues before building a predictive model. Additionally,
 EDA helps researchers understand the distribution of the data, which can inform
 the choice of predictive models. For instance, if the data is non-linear, a linear
 model may not besuitable, and non-linear models such as decision trees or neural
 networks may be more appropriate. 
 In summary, EDA is a critical step in stock market prediction as it enables researchers to identify patterns, relationships, and
 issues in the data that can inform the selection of appropriate predictive models.
 During EDA, we first focused on describing the datasets that we were using, the
 following are the screen-shots of the results :
Next step we wanted to get a correlation matrix in order to see to what extent the features are
 dependent on each other, from here we expected a decent correlation score between the
 sentiment scores of news articles and stock prices, unfortunately, we saw the worst nightmare of
 data analysts! There was 0 correlation between the sentiment scores and stock prices. We have
 tried changing the timeline of sentiment scores to compare past news sentiments with current
 stock prices but that has not changed our correlation rate even a small bit.
Wedecided to move forward and conduct a few more visualizations to understand if this was the
 final report of our dataset. We performed scatter plot representation on the data and the results
 were as follows :
From the scatter plots as well we see no relation between sentiment scores and stock prices. We
 have tried to adjust the data by using sentiment score with closing price, or sentiment score with
 opening price but they have given similar results.
 Wewere very disappointed by the results we achieved as all the papers that we have referred to
 have shown a strong correlation between the sentiment scores and stock prices, Then again we
 had a very small and possibly bad dataset, which didn’t yield the results that we wished for.
 Wehave then decided to continue with a time series regression, to analyze the stock prices over
 the time frames.
 Here we have used the Reliances stock market dataset from Yahoo finance page.
 First we have built up a chart series :
 Decomposition of additive time series :
For example, suppose we are analyzing the monthly closing prices of a stock over a five-year
 period. If the seasonal graph shows a consistent pattern of higher prices during certain months or
 quarters, but the observed graph shows an overall upward trend, this could indicate that the stock
 has been experiencing steady growth over the five-year period, even though there are seasonal
 fluctuations.
 
 Time period representations :

Modeling
 RNN- LSTM
 Recurrent Neural Networks (RNNs) are a type of neural network designed to
 handle sequential data, such as time series, text, and speech. Unlike feedforward
 neural networks, RNNs have loops that allow information to be passed from one
 step of the sequence to the next, making them ideal for tasks where context and
 history matter. However, traditional RNNs have a shortcoming known as the
 "vanishing gradient" problem, where the gradients used for training diminish
 exponentially over time, making it difficult for the network to capture long-term
 dependencies. Long Short-Term Memory (LSTM) is a type of RNN that was
 introduced to address the vanishing gradient problem. LSTMs are designed to
 allow the network to selectively remember or forget information over long periods,
 making them ideal for tasks such as speech recognition, natural language
 processing, and music composition. LSTMs are made up of several layers of
 memory cells, each of which contains an input gate, an output gate, and a forget
 gate. These gates control the flow of information into and out of the cell, allowing
 the network to selectively retain or discard information over time.
 One of the key advantages of LSTMs is their ability to capture long-term
 dependencies in sequential data. Traditional RNNs struggle with this because the
 gradients used for training vanish over time, making it difficult for the network to
 remember information from earlier steps in the sequence. LSTMs solve this
 problem by using memory cells to store information over long periods, allowing
 the network to maintain a longer-term memory of the sequence. Overall, RNN
 LSTMis a powerful tool for handling sequential data and has been successfully
 applied to a wide range of applications including speech recognition, language
 translation, and stock price prediction. By understanding the architecture and
 capabilities of RNN LSTMs, researchers and data scientists can apply this
 technology to a variety of challenging problems.
We get a test MSE of 203.037
Regenerate response
 One potential avenue for improvement is to add more features to the model. It's
 possible that the current model is not capturing all of the relevant information that
 influences stock prices. Including additional features, such as market trends or
 economic indicators, could help improve the model's accuracy. Another strategy is
 to fine-tune the model using different hyperparameters or architectures. It's
 possible that the current model is not optimized for the dataset or the specific
 problem. Experimenting with different hyperparameters or architectures, such as
 adjusting the learning rate or increasing the number of hidden layers, could help
 improve the model's performance. It may also be beneficial to compare the
 performance of different machine learning algorithms to see if there is another
 method that yields better predictions.
While RNN-LSTM is a powerful algorithm for time-series data, other algorithms
 such as Random Forest or Gradient Boosting could be tested to see if they provide
 better results. Another potential avenue for improvement is to collect or integrate
 more data into the model. The current dataset may not be representative enough of
 the larger market, or there may be additional sources of data that could help
 improve the model's accuracy. By incorporating more data, we could improve the
 model's ability to make accurate predictions. Overall, an MSE of 203.037 indicates
 that there is room for improvement in the current model. By exploring additional
 features, fine-tuning the algorithm, comparing it with other algorithms, or
 incorporating more data, we may be able to achieve better predictive performance.
Our Conclusions and Future Scope
 While our study did not find a significant correlation between news
 sentiment scores and stock prices for Reliance Industries, there are still
 promising avenues for future research. For instance, exploring the impact
 of news sentiment on other factors that may affect stock prices, such as
 market volatility or investor sentiment, could provide a more nuanced
 understanding of the relationship between news and stock prices.
 Moreover, while our LSTM model achieved a mean squared error of
 203.037, there is still potential for improving its predictive accuracy. Future
 research could explore alternative model architectures or consider
 additional features to enhance the model's performance. Additionally,
 further investigation could focus on improving the quality and quantity of the
 dataset, such as by incorporating more news sources or utilizing more
 advanced natural language processing techniques to analyze news
 sentiment.
 In conclusion, our study highlights the need for continued research into the
 complex relationship between news sentiment and stock prices. By
 exploring new approaches and incorporating additional data sources, future
 work can further advance our understanding of this important area and
 improve predictive models for stock market analysis.

 
References
 1.) https://www.rpubs.com/AurelliaChristie/time-series-and-stock-analysis
 2.) https://finance.yahoo.com/quote/RELIANCE.NS?p=RELIANCE.NS&.tsrc=
 fin-srch
 3.) https://www.tidyverse.org/packages/
 4.) https://www.researchgate.net/publication/336087787_Stock_Price_Predictio
 n_Using_News_Sentiment_Analysis
 5.) https://www.red-gate.com/simple-talk/databases/sql-server/bi-sql-server/text-mining-and-sentiment-analysis-with-r/

