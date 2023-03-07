# Typical Exam Questions

## Discutere brevemente cosa si intende per dimensionality curse.
Per introdurre la dimensionality curse bisogna comprendere che nel contesto del data mining, i dati sono rappresentati tramite tensori a due dimensioni, ovvero matrici. Queste matrici hanno dimensione n  p dove: 
n rappresenta il numero di istanze o oggetti che condividono dei particolari attributi
p rappresenta il numero di attributi o features 
Generalmente, se p>100 si parla di alta dimensionalità dei dati.

La dimensionality curse o maledizione della dimensionalita’ si riferisce al fenomeno in cui l’analisi dei dati diventa drasticamente piu’ difficile al crescere della dimensionalita’ dei dati. 
Più precisamente, al crescere della dimensionalità i dati diventano più sparsi nello spazio che occupano. Dal momento che noi osserviamo spesso dei campioni, gli oggetti osservati non sono rappresentativi rispetto alla vera popolazione. 
Questo comporta anche una perdita di significato della misura di distanza o similarità utilizzata da alcuni algoritmi di data mining, poiché gli oggetti risultano equamente distanti. Ciò riduce la bontà di apprendimento e la precisione. Spesso si arriva addirittura a non riuscire a creare un modello.

La riduzione della dimensionalita’ aumenta le performance di molti algoritmi, in parte a causa della rimozione di feature non necessarie, rumore e per la maledizione della dimensionalita’. Inoltre, sia i modelli che i dati diventano piu’ interpretabili, il che ne agevola la visualizzazione, sebbene venga penalizzata l’accuratezza. Infine, ciò porta ad un utilizzo minore di memoria.
 
L’obiettivo della riduzione delle dimensioni è quello di eliminare la ridondanza dei dati, proiettando i dati esistenti su un altro vettore dimensionale. Così facendo è possibile allo stesso tempo:
Migliorare la presentazione dei dati;
Conservare i dati in maniera più efficiente;
Scoprire correlazioni nascoste

Vi sono varie tecniche di riduzione della dimensionalita’ tra cui la Principal Component Analysis che viene utilizzata per traslare i dati in una minore dimensionalita’ e per permettere di visualizzare i grafici di dati ad alta dimensionalita’ come i decision-boundary dei modelli. 

La PCA può essere suddivisa in cinque steps:
Standardizzare l’intervallo di variabili continue;
Calcolare la matrice di covarianza/correlazione per identificare le correlazioni;
Calcolare gli autovettori e gli autovalori della matrice di covarianza per identificare le componenti principali;
Crea un vettore di caratteristiche per decidere quali componenti principali mantenere;
Esegue un recasting dei dati lungo gli assi delle componenti principali.

PCA trova le direzioni ortogonali della varianza massima dei dati forniti. Può essere pensato come una trasformazione in un nuovo sistema di coordinate, dove la prima coordinata (la prima componente principale) identifica la proiezione di massima varianza, la seconda coordinata la seconda massima varianza, etc...

Il risultato che otteniamo sono p componenti principali y1, ..., yp in cui ogni componente principale e’ una combinazione lineare delle feature originali ed ognuna cattura la massima variabilita’ dei dati originali con la clausola che ogni componente principale sia ortogonale rispetto alla componente principale precedente. Questo porta ad una

PCA trova le direzioni ortogonali di massima varianza dei dati. Può essere pensato come una trasformazione in un nuovo sistema di coordinate, dove la prima coordinata (la prima
componente principale) identifica la proiezione di massima varianza, la seconda coordinata
la seconda massima varianza, ecc. ecc. Matematicamente, le componenti principali sono gli
autovettori della matrice di covarianza.

L’obiettivo della PCA e’ di trovare il numero di dimensioni che massimizza la varianza dei dati proiettati.

By applying PCA on the original data, we
obtain p principal components, y1, . . . , yp, where every principal component
is a linear combination of the original attributes. Each principal component
captures the maximum amount of variation in the original data subject to the
constraint that it must be orthogonal to the preceding principal components.
Thus, the amount of variation captured decreases for each successive principal
component, and hence, it is possible to approximate the original data using the
top k principal components, y1, . . . , yk. Indeed, if there is a hidden structure
in the normal class, we can expect to obtain a good approximation using a
smaller number of features, k < p.
Once, we have derived a smaller set of k features, we can project any
new data instance x to its k-dimensional representation y. Moreover, we can
also re-project y back to the original space of p attributes, resulting in a
reconstruction of x.

Una volta standardizzati i dati, si calcola la matrice delle covarianze C, ed i relativi autovalori i ed autovettori vi. Poi, si standardizzano gli autovettori in modo da ottenere dei vettori di modulo unitario, così da ottenere un nuovo sistema di vettori ortonormali per i dati.
Si procede infine diagonalizzando la matrice delle covarianze utilizzando la base ortonormale ottenuta, ottenendo così lungo la diagonale le varianze delle dimensioni corrispondenti.
Per ridurre la dimensionalità dello spazio dei dati è possibile troncare un certo numero di colonne della matrice degli autovettori utilizzata per la diagonalizzazione. 

Although PCA provides a simple approach for capturing low-dimensional
representations, it can only derive features that are linear combinations of the
original attributes. When the normal class exhibits nonlinear patterns, it is
difficult to capture them using PCA

Oltre alla PCA, vi sono altre tecniche che vengono utilizzate come la rimozione o aggregazione di feature, e la selezione di insiemi rilevanti di attributi.

---

## Discutere le misure di similarita’ viste e come si utilizzano

---

## Discutere degli algoritmi k-means e k-medoids e delle loro differenze

---

## Discutere un algoritmo di clustering gerarchico

---

## Discutere un algoritmo di clustering agglomerativo

---

## Descrivere l’algoritmo DBSCAN

---

## Discutere il classificatore K-NN e cosa succede quando il parametro k tende ad infinito

---

## Descrivere come gestisce una variabile non numerica KNN (Come si trattano le variabili non numeriche)

---

## Discutere del coefficiente di silhouette e fornire un esempio

---

## Descrivere brevemente il procedimento di costruzione di un albero di decisione per la classificazione

---

Discutere il processo di learning di un albero binario di classificazione

---

Discutere l’uso della similarita’ negli alberi di decisione

---

Spiegare il criterio di splitting basato su Information Gain index

---

Spiegare il criterio di splitting basato su GINI

---

Descrivere l’algoritmo di Bagging.

---

Descrivere l’algoritmo di Boosting.

---

Discutere le differenze tra bagging and boosting

---

Descrivere un metodo per stimare la similarità tra due istanze una random forest

---

Discutere come utilizzare le variabili categoriche

---

Discutere la definizione di ROC Curve di un classificatore Binario.

---

Discutere la rappresentazione vettoriale dei documenti basata to tf-idf

---

Discutere come stimare la distanza di Jaccard tra due insieme tramite MinHashing.

---

Shingles

---

Discutere User Based Recommeder System e il tipo di similarita’ utilizzata

