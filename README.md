# Dendrite

# Screening Test: 

## --> As part of the screening test, you will write code to parse the JSON file provided(algoparams_from_ui) and kick off in sequence the following machine learning steps programmatically.

   --> Keep in mind your final code should be able to parse any Json that follows this format.
   
   --> It is crucial you have a generic parse that can read the various steps like feature handling, feature generation and model building using Grid search after parsing hyper params.


1) Read the target and type of regression to be run

![image](https://user-images.githubusercontent.com/110006271/211156010-6a8041eb-3f8a-4b66-96b7-2cc16fea0e6e.png)

 
2) Read the features (which are column names in the csv) and figure out what missing imputation needs to be applied and apply that to the columns loaded in a dataframe

![image](https://user-images.githubusercontent.com/110006271/211156028-5df1aea0-45ba-4531-bcaf-2664a5a6bccc.png)

 
3) Compute feature reduction based on input. See the screenshot below where there can be No Reduction, Corr with Target, Tree-based, PCA. Please make sure you write code so that all options can work. If we rerun your code with a different Json it should work if we switch No Reduction to say PCA.

![image](https://user-images.githubusercontent.com/110006271/211156038-853fdadf-a44c-48e2-a75a-6cfb6548814e.png)

 
4) Parse the Json and make the model objects (using sklean) that can handle what is required in the “prediction_type” specified in the JSON (See #1 where “prediction_type” is specified). Keep in mind not to pick models that don’t apply for the prediction_type specified

![image](https://user-images.githubusercontent.com/110006271/211156047-2445347b-894d-4549-b00d-539939bc8a14.png)

 
5) Run the fit and predict on each model – keep in mind that you need to do hyper parameter tuning i.e., use GridSearchCV

![image](https://user-images.githubusercontent.com/110006271/211156056-81559b5a-f251-4044-89ec-747242610ec0.png)

 
6) Log to the console the standard model metrics that apply
