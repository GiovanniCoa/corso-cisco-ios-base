# Routing statico

Il routing statico è una tecnica di instradamento di rete che coinvolge la configurazione manuale delle rotte all'interno di un dispositivo di rete. In questo articolo approfondiremo l'utilizzo di `ip route` per configurare rotte statiche sui router e i vantaggi e le sfide associate a questa pratica.

## Configurazione delle rotte statiche

Per configurare una rotta statica su un router, si utilizza il comando `ip route` seguito dall'indirizzo di rete di destinazione e dalla maschera di sottorete, nonché dall'indirizzo IP dell'interfaccia attraverso la quale instradare il traffico verso quella rete. Ad esempio, per instradare il traffico destinato alla rete 192.168.1.0/24 attraverso l'interfaccia GigabitEthernet0/0 con l'indirizzo IP 10.0.0.1, si utilizzerebbe il seguente comando:

`ip route 192.168.1.0 255.255.255.0 10.0.0.1`

È importante notare che le rotte statiche devono essere configurate manualmente e richiedono un'attenta pianificazione per garantire che il traffico venga instradato correttamente.

## Vantaggi del routing statico

Il routing statico offre diversi vantaggi rispetto al routing dinamico, tra cui:

- Controllo completo: le rotte statiche consentono agli amministratori di rete di avere un controllo completo sull'instradamento del traffico senza dipendere da protocolli di instradamento dinamici.
- Efficienza: le rotte statiche possono essere configurate per instradare il traffico in modo specifico e ottimizzato, riducendo la congestione di rete e migliorando le prestazioni complessive.
- Sicurezza: le rotte statiche possono essere utilizzate per instradare il traffico attraverso percorsi sicuri e controllati, contribuendo a proteggere la rete da minacce esterne.

## Sfide del routing statico

Nonostante i vantaggi, il routing statico presenta anche alcune sfide, tra cui:

- Gestione complessa: configurare e gestire un gran numero di rotte statiche può diventare complicato e richiedere un'attenta manutenzione per evitare errori di configurazione.
- Scalabilità limitata: il routing statico può essere difficile da scalare su reti complesse in rapida evoluzione, poiché richiede la configurazione manuale di ogni rotta.
- Ridondanza: in assenza di un meccanismo di failover automatico, il routing statico potrebbe non essere in grado di garantire la ridondanza e la disponibilità del traffico di rete in caso di guasti.

## Verifica delle rotte statiche

Per verificare le rotte statiche configurate su un router, è possibile utilizzare il comando `show ip route`. Questo comando visualizzerà un elenco delle rotte attualmente configurate sul dispositivo, inclusi i dettagli come l'indirizzo di rete di destinazione, la maschera di sottorete e l'interfacc