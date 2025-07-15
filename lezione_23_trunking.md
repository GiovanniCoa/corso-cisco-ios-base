# Trunking

Il trunking è una tecnica utilizzata nelle reti informatiche per consentire la trasmissione di più VLAN attraverso un singolo collegamento di rete. Grazie al trunking, è possibile ottimizzare l'utilizzo della larghezza di banda, migliorare l'efficienza della rete e semplificare la gestione delle VLAN.

## Switchport mode trunk

Nelle reti Cisco, per abilitare il trunking su una porta di uno switch è necessario configurare il parametro "switchport mode trunk". Questo comando indica allo switch di accettare e trasmettere il traffico di più VLAN sulla porta specificata. È importante specificare che tutte le porte coinvolte in un trunk devono essere configurate nello stesso modo, altrimenti potrebbero verificarsi errori di comunicazione all'interno della rete.

## Native VLAN

La native VLAN è una VLAN predefinita assegnata a un trunk, utilizzata per il traffico di controllo di rete non contrassegnato. È importante specificare correttamente la native VLAN su entrambe le estremità del trunk, in modo che lo switch possa interpretare correttamente il traffico non contrassegnato e instradare correttamente i pacchetti attraverso la rete.

In conclusione, il trunking è una tecnica essenziale per ottimizzare le prestazioni e la gestione delle reti VLAN. Configurare correttamente il trunking, impostando il parametro "switchport mode trunk" e specificando correttamente la native VLAN, è fondamentale per garantire un funzionamento efficiente della rete e massimizzare l'utilizzo della larghezza di banda disponibile.