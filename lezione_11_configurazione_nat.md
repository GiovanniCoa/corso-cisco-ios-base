# Configurazione NAT

Il Network Address Translation (NAT) è una tecnica utilizzata nei router per consentire a più dispositivi di condividere un unico indirizzo IP pubblico. Questo articolo si concentrerà sulla configurazione del NAT, includendo concetti come ip nat inside, outside, static, dynamic e overload.

## ip nat inside

L'interfaccia di rete "inside" è quella che si trova all'interno della rete locale e che necessita di traduzione degli indirizzi IP per comunicare con la rete esterna. Per configurare l'interfaccia inside, si utilizza il comando:

```
Router(config)# interface gi0/0
Router(config-if)# ip nat inside
```

## ip nat outside

L'interfaccia di rete "outside" è quella che si trova all'esterno della rete locale e che comunica con la rete pubblica. Per configurare l'interfaccia outside, si utilizza il comando:

```
Router(config)# interface gi0/1
Router(config-if)# ip nat outside
```

## ip nat static

La traduzione statica degli indirizzi IP è utilizzata quando si desidera mappare un indirizzo IP privato a un indirizzo IP pubblico specifico. Per configurare una traduzione statica, si utilizza il comando:

```
Router(config)# ip nat inside source static 192.168.1.1 203.0.113.1
```

## ip nat dynamic

La traduzione dinamica degli indirizzi IP è utilizzata quando si desidera assegnare dinamicamente un indirizzo IP pubblico a un dispositivo all'interno della rete locale. Per configurare una traduzione dinamica, si utilizza il comando:

```
Router(config)# ip nat inside source list 1 interface gi0/1 overload
Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
```

## ip nat overload

L'overload NAT, noto anche come NAT mascherato, consente a più dispositivi di condividere un unico indirizzo IP pubblico. Questa tecnica è utile per risparmiare indirizzi IP pubblici. Per configurare l'overload NAT, si utilizza il comando:

```
Router(config)# ip nat inside source list 1 interface gi0/1 overload
Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
```

In conclusione, la corretta configurazione del NAT è essenziale per consentire la comunicazione tra dispositivi all'interno di reti pubbliche e private. Utilizzando i comandi corretti e comprendendo i concetti di ip nat inside, outside, static, dynamic e overload, è possibile ottimizzare la gestione degli indirizzi IP e migliorare le prestazioni della rete.