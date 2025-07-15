# Salvataggio e caricamento configurazioni

Il salvataggio e il caricamento delle configurazioni sono operazioni fondamentali per garantire la corretta gestione e la sicurezza dei dispositivi di rete. In questo articolo approfondiremo le procedure per effettuare il salvataggio della configurazione in esecuzione (running-config), la configurazione di avvio (startup-config) e per cancellare eventuali configurazioni presenti sui dispositivi di rete.

## Salvataggio della configurazione

Per salvare la configurazione in esecuzione su un dispositivo di rete, è necessario utilizzare il comando `copy running-config startup-config`. Questo comando copia la configurazione attualmente in esecuzione nella memoria permanente del dispositivo, assicurando che le modifiche apportate non andranno perse in caso di riavvio del dispositivo.

## Caricamento della configurazione

Per caricare una configurazione precedentemente salvata nella memoria permanente del dispositivo, è sufficiente utilizzare il comando `copy startup-config running-config`. Questo comando sovrascrive la configurazione attualmente in esecuzione con quella presente nella memoria permanente, consentendo di ripristinare una configurazione precedentemente salvata.

## Cancellazione della configurazione

Per cancellare completamente la configurazione presente su un dispositivo di rete, è possibile utilizzare il comando `erase startup-config`. Questo comando cancella la configurazione presente nella memoria permanente del dispositivo, riportandolo alle impostazioni di fabbrica. È importante prestare attenzione quando si utilizza questo comando, poiché tutte le impostazioni presenti verranno eliminate e il dispositivo tornerà alle impostazioni di default.

In conclusione, il salvataggio e il caricamento delle configurazioni sono operazioni fondamentali per garantire la corretta gestione e la sicurezza dei dispositivi di rete. Utilizzando i comandi corretti è possibile salvare, ripristinare e cancellare le configurazioni in modo efficiente e sicuro. Ricordate sempre di effettuare il salvataggio delle configurazioni prima di apportare modifiche significative, per evitare la perdita di dati importanti.