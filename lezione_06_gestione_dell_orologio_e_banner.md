# Gestione dell’orologio e banner

Nel contesto della configurazione di un dispositivo di rete, due elementi fondamentali da considerare sono la gestione dell'orologio e dei banner. In questo articolo, approfondiremo le varie modalità di configurazione di questi due aspetti cruciali per il corretto funzionamento di un dispositivo di rete.

## Clock set

La corretta sincronizzazione dell'orologio di un dispositivo di rete è essenziale per garantire la coerenza temporale all'interno di una rete. La configurazione dell'orologio può avvenire manualmente tramite il comando `clock set`, specificando data e ora, oppure automaticamente utilizzando protocolli di sincronizzazione come NTP (Network Time Protocol).

```
R1(config)# clock set 14:30:00 25 May 2022
```

## Banner MOTD

Il banner Message of the Day (MOTD) è un messaggio di benvenuto visualizzato all'utente al momento dell'accesso al dispositivo di rete. Questo banner può essere configurato tramite il comando `banner motd` seguito dal testo del messaggio tra delimitatori a scelta.

```
R1(config)# banner motd #
Enter message. End with the character '#'.
Welcome to Router 1. Authorized access only.
#
```

## Esecuzione di comandi all'avvio

Per automatizzare il processo di configurazione di un dispositivo di rete, è possibile utilizzare il comando `exec` per eseguire una serie di comandi all'avvio del dispositivo. In questo modo, è possibile garantire che determinate configurazioni siano sempre presenti dopo un riavvio.

```
R1(config)# exec
R1(config-exec)# interface gigabitethernet 0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
```

## Gestione dei messaggi in arrivo

Infine, la gestione dei messaggi in arrivo è un aspetto importante da considerare nella configurazione di un dispositivo di rete. Utilizzando il comando `incoming`, è possibile definire delle regole per gestire i messaggi in arrivo e garantire un corretto instradamento all'interno della rete.

```
R1(config)# access-list 1 permit any
R1(config)# interface gigabitethernet 0/0
R1(config-if)# ip access-group 1 in
```

In conclusione, la corretta gestione dell'orologio e dei banner è fondamentale per garantire il corretto funzionamento di un dispositivo di rete. Utilizzando i comandi descritti in questo articolo, è possibile configurare in modo preciso e efficace questi due aspetti cruciali per la sicurezza e l'efficienza di una rete.