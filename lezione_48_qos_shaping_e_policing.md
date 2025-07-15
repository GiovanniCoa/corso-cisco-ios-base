# QoS: shaping e policing

Nel contesto delle reti informatiche, la gestione della Qualità del Servizio (QoS) riveste un'importanza fondamentale per garantire prestazioni ottimali e una distribuzione efficiente delle risorse di rete. Tra le tecniche utilizzate per controllare il flusso del traffico e gestire la banda disponibile, due approcci principali sono il shaping e il policing.

## Traffic Shaping

Il traffic shaping è una tecnica che consente di controllare il flusso del traffico in uscita da un nodo di rete, limitandone la velocità di trasmissione e regolando la quantità di dati inviati in determinati intervalli di tempo. Questo permette di evitare congestioni e garantire una distribuzione equa delle risorse di rete tra gli utenti.

Il shaping può essere implementato in diversi modi, ad esempio utilizzando algoritmi di buffering e scheduling per gestire la priorità dei pacchetti in transito. In questo modo è possibile garantire che il traffico critico, come le chiamate VoIP o il video in streaming, abbia la precedenza rispetto a altre tipologie di dati meno sensibili alla latenza.

## Policing

Il policing, invece, si concentra sul controllo del traffico in ingresso, verificando che i pacchetti rispettino determinati parametri di qualità del servizio definiti a livello di politica di rete. Questa tecnica permette di limitare la quantità di dati che un utente può inviare o ricevere, evitando congestioni e garantendo una distribuzione equilibrata delle risorse di rete.

Il policing può essere implementato attraverso filtri di controllo del traffico che verificano se i pacchetti soddisfano i criteri definiti, ad esempio limitando la larghezza di banda disponibile per determinati tipi di traffico o per singoli utenti. In questo modo è possibile garantire che le risorse di rete siano utilizzate in modo efficiente e che il traffico critico abbia la priorità rispetto a quello non essenziale.

## Conclusioni

In conclusione, il shaping e il policing sono due tecniche fondamentali per garantire una gestione efficace della banda e una distribuzione equa delle risorse di rete. Attraverso queste metodologie è possibile ottimizzare le prestazioni della rete, evitare congestioni e garantire una qualità del servizio adeguata per tutte le tipologie di traffico. Grazie all'implementazione di queste tecniche, è possibile assicurare un'esperienza utente ottimale e massimizzare l'efficienza delle reti informatiche.