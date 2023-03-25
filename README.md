## Changes made in "travelling/components/data_ingestion.py" at line 86,87 & 88 to resolve error as follows :

#added target column 'ProdTaken' instead of 'default.payment.next.month'
for train_index,test_index in split.split(travel_data_frame,travel_data_frame['ProdTaken']):

  #no column as ID,so changed to .drop(["CustomerID"],axis=1)
  strat_train_set = travel_data_frame.loc[train_index].drop(["CustomerID"],axis=1)  
  strat_test_set = travel_data_frame.loc[test_index].drop(["CustomerID"],axis=1)    
