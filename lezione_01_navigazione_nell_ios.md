# Navigazione nell’IOS

La navigazione nell’IOS (Internetwork Operating System) è un processo essenziale per chiunque lavori con dispositivi Cisco. Conoscere le modalità EXEC, privilegiata e globale, così come i prompt e la struttura dei comandi, è fondamentale per muoversi con agilità all’interno del sistema operativo di questi dispositivi di rete.

## Modalità EXEC

Nell’IOS esistono due modalità EXEC principali: la modalità EXEC utente e la modalità EXEC privilegiata. La modalità EXEC utente è quella di default a cui si accede quando si effettua il login al dispositivo. In questa modalità si possono eseguire comandi di visualizzazione di informazioni di base sul dispositivo.

La modalità EXEC privilegiata, invece, offre un livello maggiore di controllo e possibilità di configurazione del dispositivo. Per accedere a questa modalità è necessario utilizzare il comando `enable` seguito dalla password di privilegio. Una volta in modalità EXEC privilegiata, il prompt del dispositivo cambierà da `>` a `#`.

## Modalità globale

La modalità globale è una modalità di configurazione avanzata in cui è possibile apportare modifiche alle impostazioni globali del dispositivo. Per accedere a questa modalità dalla modalità EXEC privilegiata, è sufficiente utilizzare il comando `configure terminal` o `conf t`. Il prompt cambierà da `#` a `(config)`.

## Prompt e struttura dei comandi

Il prompt di un dispositivo Cisco nell’IOS fornisce informazioni utili sullo stato corrente e sulla modalità in cui ci si trova. Ad esempio, il prompt può indicare se si è in modalità EXEC utente (`>`) o privilegiata (`#`), se si è in modalità globale `(config)` o se si è in modalità di configurazione di una specifica interfaccia o servizio.

La struttura dei comandi nell’IOS di solito segue uno schema ben definito, con il comando principale seguito da eventuali argomenti e opzioni. Ad esempio, per visualizzare le informazioni di routing di un dispositivo si può utilizzare il comando `show ip route`. Per configurare un'interfaccia di rete si può utilizzare il comando `interface` seguito dal nome dell’interfaccia e dalle relative opzioni di configurazione.

In conclusione, la navigazione nell’IOS richiede la conoscenza delle modalità di esecuzione, privilegiate e globali, così come dei prompt e della struttura dei comandi. Questa conoscenza è fondamentale per poter gestire con efficacia e sicurezza i dispositivi Cisco e garantire un corretto funzionamento delle reti di cui fanno parte.