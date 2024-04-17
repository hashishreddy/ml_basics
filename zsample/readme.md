ml final


remember all of us should have different ml models or else .....problemmm


                             
ok
mention the name
somewhere in the code

Hello boys and girls we are working on it 
mean time u start finding github repos or kaggle notebooks that are using this dataset cause this is not a custom dataset it has been taken from somewhere


and if possible ask him if the target column is "label"


yes target column is label


i will upload in 10 min fellows harshil will also upload

can you guys talk to each other ?
reply fast


uploaded new.ipynb for akhila tara and hashish
there is random forest , logistic and xgboost 
take each one tell here  who are taking what and the one taking logistic also add random or xgboost for like better output
i have given each model in three different nodes so delete other two 

reply ichi saavandi first

hashish, i have uploaded the file for you. see that ra. and let me know if its okay. see the final score.


y=df['']


/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in get_loc(self, key, method, tolerance)
   3360             try:
-> 3361                 return self._engine.get_loc(casted_key)
   3362             except KeyError as err:

/opt/anaconda3/lib/python3.9/site-packages/pandas/_libs/index.pyx in pandas._libs.index.IndexEngine.get_loc()

/opt/anaconda3/lib/python3.9/site-packages/pandas/_libs/index.pyx in pandas._libs.index.IndexEngine.get_loc()

pandas/_libs/hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()

pandas/_libs/hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()

KeyError: ''

The above exception was the direct cause of the following exception:

KeyError                                  Traceback (most recent call last)
/tmp/ipykernel_27545/1592312252.py in <module>
----> 1 y=df['']

/opt/anaconda3/lib/python3.9/site-packages/pandas/core/frame.py in __getitem__(self, key)
   3456             if self.columns.nlevels > 1:
...
-> 3363                 raise KeyError(key) from err
   3364 
   3365         if is_scalar(key) and isna(key) and not self.hasnans:

KeyError: ''
harshil i am getting this error


what about other things ra ?
y = df['label'] kadha ra. just copy paste what i have done ra. i think it should be coming

ya gi

adithya - i updated new.ipynb again now i added accuracy function and if u guys are doing change the n_estimators parameter in the function ra u will get different output

tell me if its working ra i gotta go


harshil - i have kept one more code named Untitled.ipynb with accuracy 0.99. who ever wants use it guys. and let others know that you are using so that there will be no confusion.




hashish - harshil now we have to use this model and predict the lable for the Cyber1_val_students.csv data set

harshil - okay, so should i do the dump and pickle the model for the Cyber1_val_students.csv dataset?

emo edo okati chey


deshna?

adithya-
 import pickle

# Save the models
with open('clf_rf.pkl', 'wb') as f:
    pickle.dump(clf, f)

with open('clf_lr.pkl', 'wb') as f:
    pickle.dump(clf_lr, f)

with open('clf_xgb.pkl', 'wb') as f:
    pickle.dump(clf_xgb, f)

# Save the transformers
with open('scaler.pkl', 'wb') as f:
    pickle.dump(scaler, f)

with open('pca.pkl', 'wb') as f:
    pickle.dump(pca, f)
import pickle
import pandas as pd

# Load the models
with open('clf_rf.pkl', 'rb') as f:
    clf = pickle.load(f)

with open('clf_lr.pkl', 'rb') as f:
    clf_lr = pickle.load(f)

with open('clf_xgb.pkl', 'rb') as f:
    clf_xgb = pickle.load(f)

# Load the transformers
with open('scaler.pkl', 'rb') as f:
    scaler = pickle.load(f)

with open('pca.pkl', 'rb') as f:
    pca = pickle.load(f)


lab= LabelEncoder()
df_val = pd.read_csv('Cyber1_val_students.csv')
columns_to_en = ['proto', 'service', 'state', 'attack_cat']
for column in columns_to_en:
    df_val[column] = lab.fit_transform(df_val[column])

df_val_scaled = scaler.transform(df_val)

# Apply PCA
df_val_pca = pca.transform(df_val_scaled)

# Convert to DataFrame
df_val_pca = pd.DataFrame(df_val_pca, columns=[f'PC{i}' for i in range(1, len(df_val.columns) + 1)])

df_val_pca_top3 = df_val_pca[['PC1', 'PC2', 'PC3']]

# Predict the labels using the trained models
y_pred_rf = clf.predict(df_val_pca_top3)
y_pred_lr = clf_lr.predict(df_val_pca_top3)
y_pred_xgb = clf_xgb.predict(df_val_pca_top3)

# Create a DataFrame with the predictions
df_predictions = pd.DataFrame({
    'RandomForest': y_pred_rf,
    'LogisticRegression': y_pred_lr,
    'XGBoost': y_pred_xgb
})

print(df_predictions)


this is the extension for the latest file I uploaded for predicting label 


harshil na code lo update chey ra
harshil - updating it ra. just a min
ok


id,label
102165,1.0
54425,1.0
58825,1.0
85054,1.0
93048,1.0
69512,1.0
49298,0.99
159406,1.0
144618,1.0
59269,1.0
9874,0.0
100832,1.0
98179,1.0
43241,0.0

output ela csv file lo ravali
chesaka msg pettu


adithya-
df_predictions = pd.DataFrame({'RandomForest': y_pred_rf, 'LogisticRegression': y_pred_lr, 'XGBoost': y_pred_xgb})


df_predictions.to_csv('predictions.csv', index=False)
to convert to CSV files is anybody else other than hashish seeing this ???



i have uploaded all the other required things for all the people. please check and submit
