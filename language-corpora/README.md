# Language corporas

This exercise focused on measuring performance of classification task using embedding models trained on different language corporas.
Binary classification (pos/neg) of Booking.com reviews (>100k) was chosen as a task.

Co-author: [MrMiodek](https://github.com/MrMiodek)

## Classification models
- Simple MLP
- LSTM based
- Convolution based

## Embedding models
- CBOW
- SKIP-GRAM
- HerBERT

## Corporas
- Oscar
- KGR10
- Booking reviews

## Results

#### Detailed MLP
![F1_folds.png](plots/F1_folds.png)

#### All
![L3_F1_1.png](plots/L3_F1_1.png)

# Transfer learning

Part of the exercise was to try transfer learning between languages (pl, en) in different configurations on the same task (MLP).

## Results
![eng_50_50.png](plots%2Feng_50_50.png)
![eng_100_0.png](plots%2Feng_100_0.png)
![pol_50_50.png](plots%2Fpol_50_50.png)
![pol_100_0.png](plots%2Fpol_100_0.png)
