# Machine-Learning

## Decision Tree
`Step 1 - Load your prepared data`
```
import pandas as pd

df = pd.read_csv('datasetName.csv')
df.head()
```
 
`Step 2 - Specify your prediction target - Y`
```
Y = df.columnName
```
 
`Step 3 - Specify your prediction features - X`
```
# Starts by grouping all needed columns in a list

features_list = ['columnName1','columnName2','columnName3','columnName4','columnNamen']
X = df[features_list]

print(X.head())
```

`Step 4 - Specify your model and fit/train it`
```
from sklearn.tree import DecisionTreeRegressor

#For model reproducibility, set a numeric value for random_state when specifying the model
model = DecisionTreeRegressor(random_state=1)

model.fit(X,Y)
```

`Step 5 - Make predictions`
```
print(X.head(7))
model.predict(X.head(7))
```
