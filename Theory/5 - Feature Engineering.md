# Feature Engineering

## Issues

## Possible Solutions

## Processing Strings

Feature Engineering
Binary categorical features
I dati delle feature binarie, che hanno come possibili valori solo due valori diversi, si possono mappare in 0 e 1.
K-nary categorical features
Le feature categoriali, che hanno diversi possibili valori, si possono mappare in numeri interi utilizzando il OneHot encoding, ovvero per ogni possibile valore viene mappato verso una variabile binaria. L’implementazione di sk-learn permette di svolgere questo processo in automatico oppure manualmente, fornendo in input un array con le possibili categorie.
K-nary categorical class label
Analogamente al caso precedente, si può mappare ogni possibile valore di una variabile categoriale verso un numero intero.
Features with unique values
In un dataset con una o più feature che presentano lo stesso valore, non ha senso mantenere dei dati uguali per tutti. Questo perché l’entropia della feature sarebbe 0, e quindi non porterebbe informazione aggiuntiva ai dati.
Missing values
I valori mancanti possono essere approcciati in tre modalità differenti:
Si possono rimpiazzare con la media, se il tipo del valore è numerico.
Si possono rimpiazzare con la moda, in caso di feature categoriali.
Si possono sostituire con feature binarie.
Data Scaling and Normalization
- Best scaling depends on data
  - **StandardScaler** does not remap every feature into the interval 0-1, but it depends on variance. A feature with a large variance may strongly impact on the overall distance
  - **MinMaxScaling** is usually more sensitive to outliers, but weights features more evenly
- Euclidean Distance assumes all features are equally important, and this is usually not the case
