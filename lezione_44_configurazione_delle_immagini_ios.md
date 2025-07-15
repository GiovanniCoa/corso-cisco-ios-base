# Configurazione delle immagini IOS

Nell'ambito delle reti informatiche, la corretta configurazione delle immagini IOS (Internetwork Operating System) è fondamentale per garantire il corretto funzionamento di dispositivi di rete come router e switch. In questo articolo vedremo come configurare le immagini IOS utilizzando comandi come `boot system` e come effettuare l'upgrade dell'IOS tramite TFTP/FTP.

## Configurazione del boot system

Il comando `boot system` viene utilizzato per specificare quale immagine IOS deve essere caricata al momento dell'avvio del dispositivo. Per configurare il boot system su un dispositivo Cisco, è sufficiente accedere alla CLI (Command Line Interface) e digitare il seguente comando:

```
Router(config)# boot system [percorso_immagine_IOS]
```

Dove `[percorso_immagine_IOS]` rappresenta il percorso dell'immagine IOS sul dispositivo.

## Upgrade dell'IOS via TFTP/FTP

Per effettuare l'upgrade dell'IOS tramite TFTP (Trivial File Transfer Protocol) o FTP (File Transfer Protocol), è necessario seguire i seguenti passaggi:

1. Assicurarsi di avere un server TFTP/FTP accessibile dalla rete su cui si trova il dispositivo da aggiornare.
2. Scaricare l'immagine IOS desiderata dal sito ufficiale Cisco o da altre fonti attendibili.
3. Configurare il dispositivo per consentire il trasferimento dell'immagine tramite TFTP o FTP. Ecco un esempio di configurazione:

```
Router(config)# ip tftp source-interface [interfaccia]
Router(config)# tftp-server flash:[percorso_immagine_IOS]
```

4. Avviare il trasferimento dell'immagine utilizzando il comando `copy` seguito dal protocollo di trasferimento e dal percorso dell'immagine sul server:

```
Router# copy tftp flash
Indirizzo IP del server TFTP: [indirizzo_IP]
Nome file di origine: [nome_immagine_IOS]
Nome file di destinazione: [nome_immagine_IOS]
```

5. Seguire le istruzioni visualizzate a schermo per completare il processo di aggiornamento.

## Conclusioni

La corretta configurazione delle immagini IOS è essenziale per garantire la stabilità e le funzionalità dei dispositivi di rete. Utilizzando i comandi descritti in questo articolo, è possibile gestire in modo efficace le immagini IOS e aggiornarle tramite TFTP o FTP. Ricordate sempre di effettuare backup delle configurazioni e delle immagini prima di procedere con operazioni di aggiornamento, per evitare eventuali problemi di compatibilità o perdita di dati.