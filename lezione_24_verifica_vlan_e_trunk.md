# Verifica VLAN e trunk

Nel contesto delle reti informatiche, le VLAN (Virtual Local Area Network) e i trunk sono elementi fondamentali per garantire una corretta segmentazione e gestione del traffico all'interno di una rete. In questo articolo, ci focalizzeremo sulla verifica delle VLAN e dei trunk attraverso due comandi essenziali: `show vlan brief` e `show interfaces trunk`.

## Show VLAN brief

Il comando `show vlan brief` consente di visualizzare in modo conciso l'elenco delle VLAN presenti su uno switch di rete. Questo comando fornisce informazioni utili come il numero della VLAN, il nome e lo stato della VLAN. È importante verificare regolarmente lo stato delle VLAN per garantire che siano correttamente configurate e funzionanti.

Ecco un esempio di output del comando `show vlan brief`:

```
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Gi1/0/1, Gi1/0/2, Gi1/0/3
10   marketing                        active    Gi1/0/4, Gi1/0/5
20   sales                            active    Gi1/0/6, Gi1/0/7
```

## Show interfaces trunk

Il comando `show interfaces trunk` è utilizzato per verificare lo stato dei trunk sullo switch di rete. I trunk sono collegamenti ad alta velocità che consentono il passaggio di traffico tra switch e sono fondamentali per il corretto funzionamento delle VLAN. È importante verificare che i trunk siano correttamente configurati e attivi per garantire una corretta comunicazione tra i dispositivi di rete.

Ecco un esempio di output del comando `show interfaces trunk`:

```
Port        Mode             Encapsulation  Status        Native VLAN
Gi1/0/1     on               802.1q         trunking      1
Gi1/0/2     desirable        n-isl          trunking      1
Gi1/0/3     auto             802.1q         trunking      1
```

## Conclusioni

In conclusione, la verifica delle VLAN e dei trunk è un'attività fondamentale per garantire un corretto funzionamento della rete. Utilizzando i comandi `show vlan brief` e `show interfaces trunk`, è possibile ottenere informazioni dettagliate sullo stato delle VLAN e dei trunk e intervenire prontamente in caso di eventuali problemi. Assicurarsi di eseguire regolarmente queste verifiche per mantenere la rete efficiente e sicura.