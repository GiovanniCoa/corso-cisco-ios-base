# Configurazione Port Security

La configurazione della sicurezza delle porte su uno switch di rete è fondamentale per garantire la sicurezza e l'integrità della rete stessa. Una delle funzionalità principali per implementare la sicurezza delle porte su uno switch è il port security.

## switchport port-security

La configurazione del port security su uno switch Cisco avviene tramite il comando `switchport port-security`. Questo comando consente di specificare il numero massimo di indirizzi MAC che possono essere associati a una determinata porta dello switch. Ad esempio, se si imposta il valore a 2, la porta accetterà solo due indirizzi MAC e bloccherà eventuali altri dispositivi che tentano di connettersi tramite la stessa porta.

## violation

In caso di violazione del port security, è possibile configurare diverse azioni da intraprendere. Le opzioni di violazione includono:

- `protect`: la porta non accetta nuovi indirizzi MAC, ma continua a inoltrare il traffico per gli indirizzi già autorizzati.
- `restrict`: la porta blocca il traffico proveniente da indirizzi MAC non autorizzati, ma continua a inoltrare il traffico per gli indirizzi autorizzati.
- `shutdown`: la porta viene disabilitata in caso di violazione del port security.

La scelta dell'azione da intraprendere dipende dalle politiche di sicurezza della rete e dalle esigenze specifiche dell'ambiente.

## aging

Per garantire la gestione efficace delle tabelle degli indirizzi MAC, è possibile configurare un timeout per gli indirizzi MAC non utilizzati. Questa funzionalità è nota come "aging" e consente di rimuovere automaticamente gli indirizzi MAC non utilizzati dalla tabella del port security dopo un determinato periodo di tempo.

Ad esempio, utilizzando il comando `switchport port-security aging time <timeout>` è possibile specificare il tempo di inattività dopo il quale un indirizzo MAC viene rimosso dalla tabella del port security.

In conclusione, la corretta configurazione del port security su uno switch di rete è fondamentale per garantire la sicurezza e l'integrità della rete stessa. Utilizzando le funzionalità di port security, è possibile limitare l'accesso alla rete solo ai dispositivi autorizzati e proteggere la rete da potenziali minacce esterne.