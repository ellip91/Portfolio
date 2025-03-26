# Data Science Portfolio
Questo portfolio raccoglie tutti i progetti di Data Science che ho realizzato durante il mio master, nel mio percorso di auto-apprendimento e per pura passione.


## Projects

  
### [Software gestionale negozio vegano](https://github.com/ellip91/Software-gestionale-negozio-vegano.git) 
<img src="https://github.com/ellip91/Images/raw/main/vegan%20store.jpg" alt="Vegan Store" width="200"/> 

Questo software gestionale è pensato per ottimizzare le operazioni quotidiane di un negozio vegano, dalla gestione dell'inventario alla vendita dei prodotti.

### [Analisi descrittiva del mercato immobiliare in Texas](https://github.com/ellip91/Analisi-statistica-descrittiva-del-mercato-immobiliare.git)
<img src="https://github.com/ellip91/Images/blob/main/mercato-immobiliare.jpg" alt="mercato-immobiliare" width="200"/> 

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
