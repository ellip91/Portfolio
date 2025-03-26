# Data Science Portfolio
Questo portfolio raccoglie tutti i progetti di Data Science che ho realizzato durante il mio master, nel mio percorso di auto-apprendimento e per pura passione.


## Projects

  
### [Software gestionale negozio vegano](https://github.com/ellip91/Software-gestionale-negozio-vegano.git) 
<img src="https://raw.githubusercontent.com/ellip91/Images/main/vegan%20store.jpg?token=GHSAT0AAAAAADBFG5E2U3FSPEH3NJ5MXJECZ7D5RTA" alt="Vegan Store" width="200"/> 

Questo software gestionale è pensato per ottimizzare le operazioni quotidiane di un negozio vegano, dalla gestione dell'inventario alla vendita dei prodotti.

### [Analisi descrittiva del mercato immobiliare in Texas](https://github.com/ellip91/Analisi-statistica-descrittiva-del-mercato-immobiliare.git)
<img src="https://github.com/ellip91/Images/blob/main/mercato-immobiliare.jpg" alt="mercato" width="200"/>


Questo progetto mostra l'analisi esplorativa del mercato immobiliare in texas.
Sono stati calcolati gli indici di posizione, forma e variabilità per le veriabili di interesse, valutando anche l'efficacia degli annunci di vendita e la distribuzione delle vendite degli immobili nelle diverse città.
L'analisi è stata condotta usando R e l'output report è un file pdf ottenuto tramite l'utilizzo del RMarkdown.

### [Un modello statistico per prevedere il peso dei neonati](https://github.com/ellip91/Modello-statistico-per-prevedere-il-peso-dei-neonati.git)
<img src="https://github.com/ellip91/Images/blob/main/peso%20neonati.jpg" alt="peso%20neonati" width="200"/> 

Il progetto ha lo scopo di creare un modello per la previsione del peso dei neonati basandosi sullo studio di variabili legate alla madre e al nascituro stesso.
I dati presenti nel dataset includono 2500 osservazioni raccolte da 3 differenti ospedali con 10 variabili per ciascuna osservazione.
Per prevedere il peso del nascituro, è stata studiata l'influenza di ciascuna variabile sulla variabile di risposta Peso al fine di creare un modello di regressione lineare multipla. Sono stati eseguiti vari test, come il Test di Correlazione, il Test T di Student e il Test del Chi Quadrato, per verificare varie ipotesi. L'analisi è stata condotta utilizzando R,  mentre per la visualizzazione dei dati è stato utilizzato ggplot2.


### [Software anti-spam](https://github.com/ellip91/Spam-Detection.git) 
<img src="https://github.com/ellip91/Images/blob/main/spam.jpeg" alt="spam" width="200"/>

Il responsabile di una azienda ha richiesto di identificare le email di tipo SPAM sulle quali fare analisi contenutistiche.
Nel dettaglio viene richiesto di:
- Addestrare un classificatore per identificare SPAM
- Individuare i Topic principali tra le email SPAM presenti nel dataset
- Calcolare la distanza semantica tra i topics ottenuti, per dedurne l'eterogeneità.
- Estrarre dalle mail NON SPAM le Organizzazioni presenti.

Il dataset è in formato csv. Dopo aver effettuato un'analisi esplorativa del dataset, si è proceduto con il preprocessing che include pulizia del dataset (rimozione punteggiature,lemming, stemming, lemmatization e rimozione stopwords e numeri) e la vettorizzazione tramite la funzione bow_tfidf(). Si addestra il modello di classificazione, partendo da un modello semplice come la logistic regression.
Per i punti successivi utilizzo tecniche di NLP.
Al fine di individuare i Topic principali tra le email SPAM presenti nel dataset è stato creato il dizionario e il corpus tramite doc2bow() che verrà utilizzato dal modello LDA. 
Per identificare i topic di maggior rilevanza, ho utilizzato Counter() per aggregare le probabilità dei topic per ciascun documento nel corpus generato dal modello LDA e il metodo most_common() dell'oggetto Counter, che restituisce una lista delle N tuple (topic_id, count) più comuni.
Per calcolare la distanza semantica tra i topics ottenuti, per dedurne l'eterogeneità, ho utilizzato cosine_similarity(), mentre per estrarre le organizzazioni nelle mail non spam faccio ricorso alla tecnica di Named Entity Recognition (NER)

### [Cross-selling di polizze assicurative](https://github.com/ellip91/Cross-selling-di-polizze-assicurative.git)
<img src="https://github.com/ellip91/Images/blob/main/polizza-vita-rami-polizze-assicurative.jpg" alt="polizze" width="200"/>

Il cliente è una compagnia di assicurazioni che ha fornito un'assicurazione sanitaria ai suoi clienti e ha bisogno di costruire un modello predittivo in grado di prevedere se gli assicurati dell'anno passato potrebbero essere interessati ad acquistare anche un'assicurazione per il proprio veicolo. Questo è molto utile per l'azienda in quanto può raggiungere tali clienti e ottimizzare i suoi ricavi.

Poichè il dataset risulta fortemente sbilanciato, sono stati utilizzati diversi approcci (oversampling, undersampling e class_weight balanced) per trovare il modello con le migliori performance. Il modello scelto è una regressione logistica e le previsioni ottenute sono state salvate nel file Excel predictions.

### [Affidabilità creditizia per il rilascio delle carte di credito](https://github.com/ellip91/Affidabilit-Creditizia-per-il-Rilascio-della-Carta-di-Credito)
<img src="https://github.com/ellip91/Images/blob/main/bonus-carta-di-credito.jpeg" alt="carta" width="200"/>

Questo progetto prevede la creazione di un modello in grado di stimare l'affidabilità creditizia dei clienti, al fine di aiutare il team dedicato a comprendere se accettare o meno la richiesta per il rilascio della carta di credito. A tale scopo, dopo aver effettuato un preprocessing dei dati, testo diversi modelli tra cui regressione logistica, naive bayes, SVM e random forest.

In base ai modelli testati il random forest classifier è quello che da migliori risultati in termini di AUC e log loss. Inoltre, dalla matrice di confusione ottenuta possiamo vedere che il modello riconosce bene i veri negativi e questo permette di escludere le persone poco affidabili dal rilascio della carta di credito.

### [Filtro anti-hater per social network](https://github.com/ellip91/Filtro-Anti-Hater-per-Social-Network)
<img src="https://github.com/ellip91/Images/blob/main/social%20media.jpg" alt="social" width="200"/>


In questo progetto si costruisce un modello in grado di filtrare i commenti degli utenti in base al grado di dannosità del linguaggio.

PREPROCESSING:
-Effettuo il preprocessing: Definisco la funzione preprocess_text. Questa funzione esegue la rimozione di punteggiatura, conversione a minuscolo, tokenizzazione, rimozione delle stopwords e lemmatizzazione.
-Separo le features dalle label: Separo i commenti preprocessati (X) dalle etichette (y)
-Divido il dataset in train e test: Utilizziamo train_test_split per dividere il dataset in dati di training e di test.

CREAZIONE DEL MODELLO: 
Inizio con l'addestramento e la valutazione di due modelli più semplici per la classificazione di testi: la regressione logistica e il Naive Bayes. Nel primo caso utilizzo LogisticRegression con il parametro class_weight='balanced' in quanto abbiamo sbilanciamento di classi. Nel caso sei Naive Bayes addestro diversi modelli per vedere quale performa meglio. In entrambi i casi, trasformo i testi in feature numeriche tramite TfidfVectorizer. Inoltre, tramite OneVsRestClassifier adatterò modelli di classificazione binaria a problemi di classificazione multilabel. 
Le metriche da tenere in considerazione per la valutazione del modello sono l'F1-score, la precisione e il recall, più appropriate perché tengono conto dello sbilanciamento delle classi e della natura multilabel del problema. 
La regressione Logistica performa meglio del naive Bayes in questo problema di classificazione multilabel ma le metriche non sono ancora ottimali. Testo allora l'utilizzo delle reti neurali ricorrenti, adatte a questo tipo di problemi.

Per la RNN eseguo un ulteriore preprocessing del dataset:
Tokenizzazione e Padding: I testi vengono tokenizzati e trasformati in sequenze di numeri interi e di lunghezza uniforme. Per la costruzione del modello creiamo una RNN che utilizza strati LSTM mentre l'output utilizza l'attivazione sigmoid per gestire la classificazione multilabel. Sia per Early Stopping che per compile monitoriamo come metrica l'f1 score.

Il prodello prescelto per le previsioni è un LSTM con dropout.
