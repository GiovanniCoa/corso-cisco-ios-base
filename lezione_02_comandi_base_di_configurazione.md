# Comandi base di configurazione

Nell'ambito della configurazione di dispositivi di rete, esistono una serie di comandi base che permettono di accedere e modificare le impostazioni di un dispositivo. Questi comandi sono fondamentali per garantire il corretto funzionamento e la sicurezza della rete.

## enable

Il comando `enable` permette di accedere alla modalità privilegiata su un dispositivo di rete. Questa modalità consente di accedere a comandi avanzati e di configurare le impostazioni di sistema.

```bash
Router> enable
Router# 
```

## configure terminal

Una volta entrati nella modalità privilegiata, il comando `configure terminal` permette di accedere alla modalità di configurazione globale del dispositivo. In questa modalità è possibile modificare le impostazioni di base del dispositivo.

```bash
Router# configure terminal
Router(config)#
```

## exit

Il comando `exit` consente di uscire dalla modalità corrente e tornare alla modalità precedente. Ad esempio, se si è nella modalità di configurazione globale, il comando `exit` riporterà all'interno della modalità privilegiata.

```bash
Router(config)# exit
Router#
```

## end

Il comando `end` permette di uscire direttamente dalla modalità di configurazione e tornare alla modalità privilegiata. Questo comando è particolarmente utile quando si desidera uscire rapidamente dalla modalità di configurazione.

```bash
Router(config)# end
Router#
```

## write

Il comando `write` o `copy running-config startup-config` permette di salvare la configurazione corrente su un file di backup. Questo è fondamentale per garantire che le modifiche apportate non vengano perse in caso di riavvio del dispositivo.

```bash
Router# write
Building configuration...
[OK]
Router#
```

## copy

Il comando `copy` consente di copiare file da una posizione all'altra. Ad esempio, è possibile utilizzare il comando `copy tftp flash` per copiare un file da un server TFTP alla memoria flash del dispositivo.

```bash
Router# copy tftp flash
Address or name of remote host []? 192.168.1.1
Source filename []? router-config
Destination filename [router-config]? 
Accessing tftp://192.168.1.1/router-config...
Loading router-config from 192.168.1.1 (via Ethernet0): !
[OK - 1234 bytes]
Router#
```

In conclusione, i comandi base di configurazione sono essenziali per gestire correttamente un dispositivo di rete. Conoscere e utilizzare correttamente questi comandi permette di configurare e mantenere una rete in modo efficace e sicuro.