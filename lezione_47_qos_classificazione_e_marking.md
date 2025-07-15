# QoS: classificazione e marking

Nell'ambito delle reti di comunicazione, la Quality of Service (QoS) svolge un ruolo fondamentale per garantire un adeguato livello di servizio agli utenti. Tra le varie funzionalità offerte dalla QoS, la classificazione e il marking dei pacchetti sono elementi chiave per gestire in maniera efficiente il traffico di rete.

## Classificazione dei pacchetti

La classificazione dei pacchetti è il processo mediante il quale vengono identificati e suddivisi i flussi di traffico in categorie omogenee, al fine di applicare politiche specifiche per ciascuna categoria. Per effettuare la classificazione, è possibile utilizzare strumenti come le class-map, che consentono di definire criteri di corrispondenza basati su parametri come indirizzi IP, porte TCP/UDP, protocolli e altri campi dei pacchetti.

## Marking dei pacchetti

Il marking dei pacchetti consiste nell'applicare un'etichetta o un valore specifico ai pacchetti in base alla loro categoria di appartenenza. Questo processo è fondamentale per identificare e distinguere i diversi flussi di traffico all'interno della rete, consentendo di privilegiare o limitare determinati tipi di traffico in base alle esigenze di QoS. Per effettuare il marking, è possibile utilizzare strumenti come le policy-map, che definiscono le azioni da applicare ai pacchetti in base alle regole stabilite nelle class-map.

## Utilizzo delle policy-map

Le policy-map rappresentano uno strumento potente per gestire il traffico di rete in base alla QoS. Attraverso le policy-map è possibile definire diverse classi di traffico utilizzando le class-map, e associare a ciascuna classe azioni specifiche come il marking dei pacchetti, la limitazione della larghezza di banda, la prioritizzazione del traffico e altre funzionalità avanzate. Una volta configurate le policy-map, è possibile applicarle alle interfacce di rete mediante l'utilizzo delle service-policy, garantendo l'applicazione coerente delle politiche di QoS all'interno della rete.

In conclusione, la classificazione e il marking dei pacchetti sono elementi fondamentali per garantire un adeguato livello di servizio all'interno delle reti di comunicazione. Attraverso l'utilizzo di strumenti come le class-map, le policy-map e le service-policy, è possibile definire e applicare politiche di QoS efficaci per gestire in maniera ottimale il traffico di rete e soddisfare le esigenze degli utenti.