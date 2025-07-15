# Spanning Tree Protocol

Il **Spanning Tree Protocol (STP)** è un protocollo di rete utilizzato per prevenire i loop di rete in una topologia di rete a commutazione di livello 2. Il protocollo determina un albero di copertura che garantisce che ci sia un percorso senza loop da ogni nodo della rete a ogni altro nodo. Questo albero di copertura è chiamato *spanning tree*.

Il comando `show spanning-tree` è utilizzato per visualizzare le informazioni relative allo spanning tree su un dispositivo di rete. Questo comando fornisce dettagli sullo stato degli switch nella rete, sulle porte di upstream e di downstream e sui tempi di convergenza.

Lo **spanning-tree mode** determina come un dispositivo di rete partecipa allo spanning tree. I due modi principali sono il **STP** classico e il **Rapid Spanning Tree Protocol (RSTP)**. STP utilizza un algoritmo più lento per calcolare il percorso senza loop, mentre RSTP è più veloce e offre tempi di convergenza più rapidi.

La **priority** è un valore numerico utilizzato per determinare quale switch diventerà il *root bridge* dello spanning tree. Il root bridge è lo switch principale che stabilisce il percorso senza loop per tutti gli altri switch nella rete. Un lower value di priority significa che lo switch ha una maggiore probabilità di diventare il root bridge.

In conclusione, lo Spanning Tree Protocol è fondamentale per garantire la stabilità e l'efficienza delle reti a commutazione di livello 2. Utilizzando comandi come `show spanning-tree`, configurando il spanning-tree mode corretto e gestendo la priority dei dispositivi di rete, è possibile creare un ambiente di rete sicuro e affidabile.