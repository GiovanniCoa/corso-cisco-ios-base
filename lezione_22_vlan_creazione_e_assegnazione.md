# VLAN: creazione e assegnazione

Le VLAN (Virtual Local Area Network) sono una tecnologia molto utile per suddividere una rete locale in segmenti logici separati, consentendo di migliorare la sicurezza, l'efficienza e la gestione della rete stessa. In questo articolo, vedremo come creare e assegnare le VLAN su un dispositivo di rete, come uno switch.

## Creazione di una VLAN

Per creare una VLAN su uno switch, è necessario accedere alla sua interfaccia di configurazione tramite un client di gestione di rete, come ad esempio il protocollo SNMP o un'interfaccia web. Una volta connessi al dispositivo, è possibile procedere con la creazione della VLAN. 

Ad esempio, supponiamo di voler creare una VLAN con il numero di identificazione 10 e un nome descrittivo "VLAN10". La sintassi per creare la VLAN su uno switch Cisco è la seguente:

```
Switch(config)# vlan 10
Switch(config-vlan)# name VLAN10
```

Con questi comandi, abbiamo creato con successo una VLAN con il numero 10 e il nome "VLAN10" sullo switch.

## Assegnazione di una VLAN a una porta

Una volta creata la VLAN, è necessario assegnarla alle porte desiderate dello switch. Per farlo, è possibile utilizzare il comando `switchport access vlan` seguito dal numero della VLAN da assegnare alla porta. Ad esempio, se vogliamo assegnare la VLAN 10 alla porta Ethernet 1/0/1, possiamo utilizzare il seguente comando:

```
Switch(config)# interface ethernet 1/0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
```

Con questi comandi, abbiamo configurato la porta Ethernet 1/0/1 dello switch in modalità access e abbiamo assegnato la VLAN 10 ad essa.

## Conclusioni

In questo articolo abbiamo visto come creare e assegnare le VLAN su uno switch di rete. Le VLAN sono uno strumento potente per segmentare una rete e migliorare la sua gestione e sicurezza. È importante comprendere come configurare correttamente le VLAN per ottenere i massimi benefici da questa tecnologia.