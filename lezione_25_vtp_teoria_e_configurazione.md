# VTP: teoria e configurazione

Il VTP (VLAN Trunking Protocol) è un protocollo utilizzato nelle reti Ethernet per semplificare la gestione delle VLAN. Questo protocollo consente di distribuire automaticamente le informazioni sulle VLAN all'interno di un dominio VTP, facilitando la configurazione e la manutenzione delle VLAN su più switch.

## VTP Modes

Esistono tre modalità di funzionamento per il VTP:

- **Server mode**: in questa modalità, uno switch può creare, modificare e cancellare le VLAN all'interno del dominio VTP. Le modifiche effettuate su uno switch in modalità server vengono propagate automaticamente a tutti gli altri switch nel dominio.
  
- **Client mode**: uno switch in modalità client riceve le informazioni sulle VLAN dal server e le applica alla propria configurazione. Gli switch in modalità client non possono modificare le VLAN all'interno del dominio.
  
- **Transparent mode**: uno switch in modalità transparent riceve e inoltra le informazioni sulle VLAN, ma non le applica alla propria configurazione. Questa modalità è utile quando si desidera mantenere VLAN locali che non devono essere propagate al resto del dominio.

## VTP Domain

Un dominio VTP è un insieme di switch che condividono le informazioni sulle VLAN tramite il protocollo VTP. Tutti gli switch all'interno dello stesso dominio devono avere lo stesso nome di dominio VTP per poter scambiare informazioni correttamente. È importante assicurarsi che tutti gli switch all'interno del dominio siano configurati con lo stesso nome di dominio per evitare problemi di compatibilità.

## VTP Password

Per garantire la sicurezza delle informazioni scambiate tramite il protocollo VTP, è possibile configurare una password VTP che deve essere la stessa su tutti gli switch all'interno del dominio. In questo modo, solo gli switch con la password corretta saranno in grado di scambiarsi informazioni sulle VLAN.

In conclusione, il VTP è uno strumento utile per semplificare la gestione delle VLAN all'interno di una rete Ethernet. Con la corretta configurazione delle modalità, del dominio e della password VTP, è possibile garantire un'efficace distribuzione delle informazioni sulle VLAN all'interno di un dominio VTP.