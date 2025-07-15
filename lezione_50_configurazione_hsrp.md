# Configurazione HSRP

Il Protocollo di Redundanza Hot Standby Routing Protocol (HSRP) è un protocollo di routing progettato per fornire un livello aggiuntivo di ridondanza e disponibilità ad una rete. Questo protocollo consente di creare un gruppo di router che possono condividere un indirizzo IP virtuale e un indirizzo MAC virtuale, garantendo che uno dei router sia sempre attivo mentre gli altri rimangono in standby.

## Vantaggi della configurazione HSRP

La configurazione HSRP offre numerosi vantaggi, tra cui:

- Ridondanza: in caso di guasto di uno dei router, il router standby può prendere immediatamente il controllo senza interruzioni nel servizio.
- Load balancing: HSRP consente di distribuire il carico di traffico tra più router attivi nel gruppo.
- Failover rapido: il passaggio da un router attivo a uno standby avviene in modo rapido e trasparente per gli utenti.

## Configurazione di base di HSRP

Per configurare HSRP, è necessario seguire i seguenti passaggi:

1. Assegnare un indirizzo IP virtuale al gruppo HSRP.
2. Configurare l'interfaccia di rete per il gruppo HSRP.
3. Impostare il router attivo e il router standby nel gruppo HSRP.
4. Verificare che la configurazione HSRP sia corretta.

Ecco un esempio di configurazione HSRP su un router Cisco:

```
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# standby 1 ip 192.168.1.254
Router(config-if)# standby 1 priority 110
Router(config-if)# standby 1 preempt
```

In questo esempio, stiamo configurando l'interfaccia GigabitEthernet0/0 con l'indirizzo IP 192.168.1.1 e il gruppo HSRP 1 con l'indirizzo IP virtuale 192.168.1.254. Il router attivo ha una priorità di 110 e il comando `preempt` consente al router attivo di riprendere il controllo una volta che è nuovamente disponibile.

## Conclusioni

La configurazione di HSRP è un modo efficace per garantire la ridondanza e la disponibilità della rete. Seguendo i passaggi corretti e monitorando attentamente la configurazione, è possibile garantire un funzionamento senza problemi del protocollo HSRP. Ricordate sempre di effettuare test di failover regolari per assicurarsi che la configurazione HSRP funzioni correttamente in caso di guasto del router attivo.