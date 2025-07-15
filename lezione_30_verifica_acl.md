# Verifica ACL

Durante la configurazione di una rete, una delle operazioni fondamentali è la definizione delle Access Control Lists (ACL) per controllare il flusso del traffico di rete. Le ACL vengono utilizzate per consentire o negare il passaggio dei pacchetti in base a determinati criteri come indirizzo IP, porta di origine o destinazione, protocollo, ecc.

Per verificare correttamente il funzionamento delle ACL è necessario utilizzare alcuni comandi specifici sui router o sui firewall. Tra i comandi più comuni troviamo `show access-lists` e `debug ip packet`.

Il comando `show access-lists` permette di visualizzare l'elenco delle ACL configurate sul dispositivo di rete, insieme alle relative regole e statistiche di utilizzo. Questo comando è particolarmente utile per verificare la corretta configurazione delle ACL e per identificare eventuali errori o inconsistenze.

Per esempio, digitando il comando `show access-lists` su un router Cisco è possibile ottenere un output simile al seguente:

```
Router# show access-lists
Standard IP access list 1
    10 permit 192.168.1.0, wildcard bits 0.0.0.255
Extended IP access list 100
    10 permit tcp any any eq 80
    20 deny ip any any
```

In questo caso, l'output mostra due ACL configurate sul router: una ACL standard che permette il traffico proveniente dalla rete 192.168.1.0 e una ACL estesa che consente il traffico TCP sulla porta 80 e nega tutto il resto.

Il comando `debug ip packet` invece è utile per visualizzare in tempo reale i pacchetti che attraversano il dispositivo di rete e che vengono controllati dalle ACL. Questo comando è molto utile per individuare eventuali problemi di filtraggio del traffico e per monitorare il comportamento delle regole definite nelle ACL.

Per utilizzare il comando `debug ip packet` è sufficiente digitare il comando sul router o sul firewall e monitorare l'output mentre il traffico di rete viene analizzato.

In conclusione, la verifica delle ACL è un passaggio fondamentale nella gestione della sicurezza di una rete e nella corretta definizione delle politiche di filtraggio del traffico. Utilizzando i comandi `show access-lists` e `debug ip packet` è possibile controllare e monitorare in modo efficace le ACL e garantire un corretto funzionamento del sistema di sicurezza della rete.