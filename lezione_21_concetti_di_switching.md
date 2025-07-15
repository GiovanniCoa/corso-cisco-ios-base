# Concetti di switching

Il concetto di switching è fondamentale nel campo delle reti informatiche, in quanto permette il trasferimento efficiente dei dati da un dispositivo all'altro. Esistono diverse tecniche di switching, tra cui store and forward e cut through, che verranno analizzate nel presente articolo.

## Store and forward

Lo switching store and forward è una tecnica che prevede la ricezione completa di un frame da parte dello switch prima di inoltrarlo alla destinazione. Questo permette di verificare l'integrità del frame e di eventuali errori prima di procedere con l'invio. Se il frame è danneggiato, viene scartato e non inoltrato alla destinazione.

Questa tecnica è particolarmente utile in situazioni in cui la velocità della rete è prioritaria rispetto alla latenza, in quanto garantisce una maggiore affidabilità nella trasmissione dei dati.

## Cut through

Lo switching cut through è una tecnica che prevede l'inoltro dei dati non appena vengono ricevuti dallo switch, senza attendere il completamento del frame. Questo permette di ridurre la latenza nella trasmissione dei dati, in quanto i pacchetti vengono inoltrati più rapidamente rispetto allo store and forward.

Tuttavia, questa tecnica presenta il rischio di inoltrare dati danneggiati o erronei, in quanto non viene effettuato un controllo completo sull'integrità del frame. Di conseguenza, lo switching cut through è più adatto a reti ad alta velocità in cui la latenza è prioritaria rispetto alla ridondanza.

In conclusione, sia lo switching store and forward che cut through hanno vantaggi e svantaggi specifici che li rendono adatti a contesti di rete differenti. È importante comprendere le caratteristiche di ciascuna tecnica per poter scegliere quella più adatta alle esigenze specifiche della propria infrastruttura di rete.