# Configurazione IP SLA

IP SLA (Internet Protocol Service Level Agreement) è una funzionalità di Cisco IOS che consente di monitorare la rete e misurare le prestazioni dei percorsi di rete in modo proattivo. Questo articolo fornirà una panoramica sulla configurazione di IP SLA, inclusa la configurazione del monitoraggio IP SLA e delle reazioni.

## Configurazione del monitoraggio IP SLA

Per configurare il monitoraggio IP SLA, è necessario seguire i seguenti passaggi:

1. Creare un'istanza IP SLA utilizzando il comando `ip sla monitor` seguito dal tipo di operazione da monitorare e dai parametri specifici dell'operazione. Ad esempio, per monitorare la latenza di un percorso di rete utilizzando il protocollo ICMP, si può utilizzare il comando:
   ```
   ip sla monitor 1
   type echo protocol ipIcmpEcho 8.8.8.8
   ```
2. Attivare l'istanza IP SLA utilizzando il comando `ip sla schedule` seguito dall'ID dell'istanza IP SLA e da un intervallo di esecuzione. Ad esempio, per eseguire il monitoraggio ogni 5 minuti, si può utilizzare il comando:
   ```
   ip sla schedule 1 life forever start-time now
   ```
3. Verificare lo stato dell'istanza IP SLA utilizzando il comando `show ip sla statistics`.

## Configurazione delle reazioni

Le reazioni sono azioni che vengono eseguite in base ai risultati dell'IP SLA. È possibile configurare diverse reazioni, ad esempio inviare una notifica tramite email o modificare dinamicamente le route di rete.

Per configurare una reazione, è necessario seguire i seguenti passaggi:

1. Creare una policy di reazione utilizzando il comando `ip sla reaction-configuration` e specificare il tipo di reazione e i parametri associati alla reazione. Ad esempio, per inviare una notifica tramite email in caso di fallimento del monitoraggio, si può utilizzare il comando:
   ```
   ip sla reaction-configuration 1 react connectionLoss threshold-type immediate action-type trapOnly
   ```
2. Associare la policy di reazione all'istanza IP SLA utilizzando il comando `ip sla monitor reaction-configuration` seguito dall'ID dell'istanza IP SLA e dall'ID della policy di reazione. Ad esempio:
   ```
   ip sla monitor reaction-configuration 1 react 1
   ```

## Conclusioni

La configurazione di IP SLA consente di monitorare attivamente le prestazioni della rete e di reagire rapidamente a eventuali problemi. Seguendo i passaggi descritti in questo articolo, è possibile configurare facilmente il monitoraggio IP SLA e le reazioni associate. Ricordate sempre di verificare lo stato dell'istanza IP SLA e delle reazioni per assicurarvi che la rete funzioni correttamente e che vengano attivate le azioni appropriate in caso di problemi.