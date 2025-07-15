# Access Control List (ACL) base

L'Access Control List (ACL) è uno strumento fondamentale utilizzato nei dispositivi di rete per controllare il flusso del traffico in ingresso e in uscita. In questo articolo, ci concentreremo sull'ACL standard e sulla sua applicazione su un'interfaccia di rete.

## Cos'è un access-list standard

Un access-list standard è un tipo di ACL che consente di filtrare il traffico in base a indirizzi IP sorgente. Questo tipo di ACL è utilizzato principalmente per controllare il traffico in ingresso verso una determinata interfaccia di rete.

## Applicazione su interfaccia

Per applicare un access-list standard su un'interfaccia di rete, è necessario seguire una serie di passaggi. In primo luogo, è necessario creare l'access-list specificando l'indirizzo IP sorgente che si desidera filtrare. Ad esempio, se si desidera bloccare il traffico proveniente dall'indirizzo IP 192.168.1.1, è possibile creare una regola simile:

```
access-list 1 deny host 192.168.1.1
```

Successivamente, è necessario applicare l'access-list all'interfaccia di ingresso desiderata. Ad esempio, se si desidera applicare l'access-list alla porta Ethernet 0/0, è possibile utilizzare il seguente comando:

```
interface Ethernet0/0
ip access-group 1 in
```

In questo modo, l'access-list verrà applicata all'interfaccia di ingresso Ethernet 0/0 e il traffico proveniente dall'indirizzo IP 192.168.1.1 verrà bloccato.

## Conclusioni

In conclusione, l'utilizzo di un access-list standard su un'interfaccia di rete è un modo efficace per controllare il flusso del traffico in ingresso. Seguendo i passaggi corretti per la creazione e l'applicazione dell'ACL, è possibile garantire una maggiore sicurezza e controllo sulla propria rete.