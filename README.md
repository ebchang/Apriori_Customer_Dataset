# Apriori_Customer_Dataset

The Aprori function takes a dataset and a minimum support. 

This will give the frequent sets and the support_data along with the frequent sets. 
freq_sets, support_data = apriori(dataset, 0.5)

Then you can generate the rules using GenerateRules to make rules based on confidence or use GenerateRules_lift to make rules based on lift. 

Sample output for generateRules based on confidence.

[(frozenset({' White'}), frozenset({' United-States'}), 0.9307692307692308), (frozenset({' United-States'}), frozenset({' White'}), 0.8752260397830018), (frozenset({' White'}), frozenset({' Male'}), 0.7009615384615385), (frozenset({' Male'}), frozenset({' Wh
ite'}), 0.8868613138686132), (frozenset({' Private'}), frozenset({' <=50K\n'}), 0.7857948139797069), (frozenset({' <=50K\n'}), frozenset({' Private'}), 0.7667766776677668), (frozenset({' Private'}), frozenset({' White'}), 0.8602029312288613), (frozenset({' White'}), frozenset({' Private'}), 0.7336538461538461), (frozenset({' <=50K\n'}), frozenset({' United-States'}), 0.9086908690869087), (frozenset({' United-States'}), frozenset({' <=50K\n'}), 0.7468354430379747), (frozenset({' <=50K\n'}), frozenset({' White'}), 0.8426842684268426), (frozenset({' White'}), frozenset({' <=50K\n'}), 0.7365384615384615), (frozenset({' Private'}), frozenset({' United-States'}), 0.9098083427282976), (frozenset({' United-States'}), frozenset({' Private'}), 0.7296564195298373), (frozenset({' Male'}), frozenset({' United-States'}), 0.9172749391727494), (frozenset({' <=50K\n'}), frozenset({' White', ' United-States'}), 0.7766776677667766), (frozenset({' Private'}), frozenset({' United-States', ' <=50K\n'}), 0.7080045095828635), (frozenset({' Private'}), frozenset({' White', ' United-States'}), 0.7959413754227733), (frozenset({' Male'}), frozenset({' White', ' United-States'}), 0.8284671532846716)]

The frozen sets is the key and items and the number is the confidence calculated. 

For generateRules_lift sample output will be: 
[(frozenset({' White'}), frozenset({' United-States'}), 1.1625), (frozenset({' United-States'}), frozenset({' White'}), 1.093128390596745), (frozenset({' White'}), frozenset({' Male'}), 1.1625), (frozenset({' Male'}), frozenset({' White'}), 1.4708029197080292), (frozenset({' Private'}), frozenset({' <=50K\n'}), 1.363021420518602), (frozenset({' <=50K\n'}), frozenset({' Private'}), 1.33003300330033), (frozenset({' Private'}), frozenset({' White'}), 1.363021420518602), (frozenset({' White'}), frozenset({' Private'}), 1.1624999999999999), (frozenset({' <=50K\n'}), frozenset({' United-States'}), 1.33003300330033)

The frozen set are the items and the number after is the lift. It will give rules where the lift is greater than 1. 

find_freq() Takes a set dataset, the number of transactions, candidates list of 1 and the minimum_support threshold.

joint_set() will take the candidate sets of 1 and 2, which will join and append all the combination of data sets. 

reference: Machine Learning in Action by Peter Harrington. Chapter 11
