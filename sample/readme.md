is q1 over?


Harshil - The total lab is only one question right. Now, i have updated the code in the train and have added one more file. Just run both of them. Run the train code first and the val code next.

Please let me know if anything more is required
---------------------------------------------------------------------------
FileNotFoundError                         Traceback (most recent call last)
/tmp/ipykernel_12161/3428856166.py in 
      2 
      3 # Load the models
----> 4 with open('model.pkl', 'rb') as f:
      5     model = pickle.load(f)
      6 

FileNotFoundError: [Errno 2] No such file or directory: 'model.pkl'


it shows this error how to fix this


harshil - I have added one more cell of code in the Puja_train_code.ipynb. Run that first and then run the Puja_val_Code.ipynb

FileNotFoundError                         Traceback (most recent call last)

<ipython-input-3-520b3cb6f623> in <cell line: 1>()
----> 1 df = pd.read_csv('Cyber2_train.csv')

4 frames

/usr/local/lib/python3.10/dist-packages/pandas/io/common.py in get_handle(path_or_buf, mode, encoding, compression, memory_map, is_text, errors, storage_options)
    857         if ioargs.encoding and "b" not in ioargs.mode:
    858             # Encoding
--> 859             handle = open(
    860                 handle,
    861                 ioargs.mode,

FileNotFoundError: [Errno 2] No such file or directory: 'Cyber2_train.csv'

this shows in second line of train code

