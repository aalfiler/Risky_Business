# Unit 11 | Classification - Risky Business

### Resampling

> Which model had the best balanced accuracy score?

- Oversample: 0.653 - best balanced accuracy score 
- SMOTE: 0.647
- Undersample: 0.566
- SMOTEEN: 0.652

> Which model had the best recall score?

- Oversample: 0.61 
- SMOTE: 0.67 - best recall score
- Undersample: 0.56
- SMOTEEN: 0.57

> Which model had the best geometric mean score?

Oversample, SMOTE and SMOTEEN models had the same geo scores:

- Oversample: 0.65 
- SMOTE: 0.65
- Undersample: 0.57
- SMOTEEN: 0.65


### Ensemble Learning

> Which model had the best balanced accuracy score?

- BalancedRandomForestClassifier: 0.729
- EasyEnsembleClassifier: 0.931 - best balanced accuracy score

> Which model had the best recall score?

- BalancedRandomForestClassifier: 0.84
- EasyEnsembleClassifier: 0.94 - best recall score

> Which model had the best geometric mean score?

- BalancedRandomForestClassifier: 0.72
- EasyEnsembleClassifier: 0.93 - best geo score

>
> What are the top three features?

- (0.076, 'total_rec_prncp')
- (0.068, 'last_pymnt_amnt')
- (0.056, 'total_pymnt')
