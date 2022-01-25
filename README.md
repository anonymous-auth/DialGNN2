# DialGNN

## the reproduction of DialGNN, the instructions of source code 
1. Concatenate the data/xcs_data_* to one file.
2. preprocess_al.py: preprocess alibaba dataset
3. calw2c_tfidf, calw2s_tfidf: calculate the tfidf for sentences and conversation.
4. data_loader.py: load preprocessed data to construct heterogeneous graph.
5. train.py: train and evaluate model.
6. predict.py: predict label with trained model.
7. utils/config.py: configuration.
8. utils/log.py: record the log.
9. models/HiGraph.py: The heterogeneous graph model.

## the instructions for the data file:
1. Each line contains a dialogue sample.
2. The columns are separated with '\001'
3. The first column stands for a unique key of the dialogue
4. The second column is the sequence of json ids in the dialogue
5. The third column is the json list, in which the keys are respectively "id": id of json, related to the sequence, "text": the content of sentence, "member type": 1 for customer, 2 for customer service, 3 for automatic AI customer service
6. The fourth and the last column stand for the category in coarse and fine level.
