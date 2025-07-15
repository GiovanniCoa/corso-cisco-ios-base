# EIGRP base

Il protocollo di routing EIGRP (Enhanced Interior Gateway Routing Protocol) è un protocollo avanzato e efficiente che viene utilizzato per determinare il percorso migliore per inviare pacchetti all'interno di una rete. In questo articolo esamineremo i concetti di base relativi a EIGRP, dalla configurazione iniziale all'implementazione pratica.

## Autonomous system

Un Autonomous System (AS) è un insieme di router che condividono un protocollo di routing comune e sono sotto il controllo di una singola autorità amministrativa. EIGRP utilizza numeri di AS per distinguere tra diverse aree di routing e garantire che i router all'interno dello stesso AS possano comunicare tra loro in modo efficiente.

## Configurazione

Per configurare EIGRP su un router, è necessario seguire alcuni passaggi fondamentali. Prima di tutto, è necessario abilitare il protocollo EIGRP utilizzando il comando `router eigrp [numero AS]` nella modalità di configurazione del router. Successivamente, è possibile aggiungere le reti che si desidera annunciare utilizzando il comando `network [indirizzo di rete] [wildcard mask]`.

Inoltre, è possibile configurare parametri aggiuntivi come la metrica di routing, il tempo di convergenza e i filtri di route per ottimizzare le prestazioni della rete e la stabilità del routing.

## Verifica

Una volta configurato EIGRP su tutti i router all'interno dello stesso Autonomous System, è importante verificare che il protocollo di routing stia funzionando correttamente. È possibile utilizzare comandi come `show ip eigrp neighbors` per visualizzare i router vicini e assicurarsi che la comunicazione tra di loro sia stabilita.

Inoltre, è possibile utilizzare il comando `show ip route` per visualizzare le tabelle di routing e verificare che le reti siano correttamente annunciate e aggiornate tra i router. Queste informazioni sono cruciali per garantire che il traffico di rete venga instradato in modo efficiente e affidabile.

In conclusione, la configurazione e la verifica di EIGRP sono passaggi fondamentali per garantire un routing ottimizzato e stabile all'interno di un Autonomous System. Con una corretta implementazione e monitoraggio costante, è possibile garantire prestazioni di rete elevate e una comunicazione fluida tra i dispositivi connessi alla rete.

---
Tag: EIGRP, routing, Autonomous System, configurazione, verifica