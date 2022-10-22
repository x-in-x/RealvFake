# RealvFake

This project was for the capstone project of the Coursera IBM Advanced Data Science Specialization.  Here I use Kaggle datasets Real.csv and Fake.csv (https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset).  The ultimate goal was to do some supervised binary classification using both machine learning and deep learning models.  For the ML models, I used both Logistic Regression and Gradient Boosted Trees models from pyspark.ml.  For the DL model, I used an LSTM neural network in Keras.  It was done with a mix of pyspark and pandas dataframes for added practice of course content.  The train-test split was 80-20.  At the model evaluation stage, I also import a custom-built TestSet.csv file comprised of 10 recently scraped **True** articles and 10 articles from *The Onion* (denoting those as **False**).  The notebooks for the project were (in order):

1. **[RealvFake].data_exp.ipynb** <br>
     (data exploration with a mix of pyspark.sql, pandas, and native python methods, lots of word density analysis)
  
2.  **[RealvFake].etl.ipynb** <br>
      (data cleansing and processing, table concatenations, removal of trivial distinguishers between datasets)
  
3.  **[RealvFake].feature_eng.ipynb** <br>
      (selection and encoding of features)
  
4.  **[RealvFake].model_def.ipynb** <br>
      (definition of 4 ML models: LR and GBT each with either Word2Vec/Normalizer or HashingTF feature extractors, definition of LSTM model)
  
5.  **[RealvFake].model_train.ipynb** <br>
      (training phase for the 5 models)
 
6.  **[RealvFake].model_evaluate.ipynb** <br>
      (model evaluation, primarily using accuracy as metric--but also looking at area under ROC curve for the ML models.  The models are also applied to TestSet.csv at this point.)
  
7. **[RealvFake].model_deployment.pdf** <br>
     (entitled "deployment" for course, but is pdf report/summary of the project, as well as thoughts on future iterations/avenues for the project)
  
The accuracies of the models were exceptionally high, but I allude to potential reasons for this in the summary document.
