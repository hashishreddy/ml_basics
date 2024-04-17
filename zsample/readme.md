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


harshil - i have kept one more code with accuracy 0.99. who ever wants use it guys. 
