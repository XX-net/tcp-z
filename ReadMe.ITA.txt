<I am Unicode File!>

Programma di patch e monitoraggio delle connessioni parziali TCP/IP

Nome del progetto:		TCP-Z  (TCP-Z Network Monitor)
Sistemi operativi supportati:	Windows XP/2003/2008/Vista/Windows 7, tutti i SP*, tutte le versioni a 32 bit (x86) e 64 bit (x64)
Autore:			deepxw#126.com
Blog:			http://deepxw.lingd.net/article-1415261-1.html
			http://deepxw.blogspot.com   (in inglese)

Aumenta il numero delle connessioni parziali TCP in entrata, aumentando la potenza della rete, accelerando i download e consentendo l'esecuzione di più attività contemporaneamente.

Funzioni:
1) Facile e sicuro: Modifica il file Tcpip.sys nella memoria. La patch è immediata; non è necessarrio riavviare il computer.

2) Ampia compatibilità: Cerca l'offset limitato attraverso la firma, senza focalizzarsi sugli aggiornamenti MS.
   Sono supportate tutte le versioni di Windows che hanno le connessioni parziali limitate.

3) Grafici professionali: TCP-Z mostra in tempo reale il numero delle connessioni stabilite, delle connessioni parziali, della creazione depth e della velocità di download e upload. 
TCP-Z, inoltre, mostra ogni minuto il numero degli eventi delle connessioni TCP.

****************
*  Istruzioni  *
****************
1) Utilizzo manuale: 
Usa l'interfaccia del programma tcpz.exe o tcpz64.exe per modificare i valori.

Anche dopo la chiusura di TCP-Z, i valori modificati rimarranno nella memoria del kernel fino allo spegnimento del computer.

Questa è una modifica temporanea. Dopo il riavvio del computer, verranno ripristinati i valori predefiniti.
Sarà necessario modificare i valori ad ogni avvio del computer.


Clicca su questo pulsante per applicare il nuovo valore

2) Utilizzo automatico: 
Installa TCP-Z Virtual Device per applicare la patch automaticamente. 

Virtual Device applica la patch nella memoria del kernel, in modo del tutto automatico e senza l'intervento dell'utente.

Usa la finestra Proprietà di Gestione dispositivi per personalizzare i valori.

Il driver andrà installato solo una volta. I valori modificati verranno applicati ad ogni avvio del computer, fino a che non si disinstallerà il driver.

Anche dopo importanti aggiornamenti, come i Service Pack, non sarà necessario reinstallare il driver.

Installa o disinstalla.
32 bit, esegui il programma come amministratore: "TCPZ_Setup-x86.exe".
64 bit, esegui il programma come amministratore: "TCPZ_Setup-x64.exe"


Le due versioni di TCP-Z sono completamente indipendenti e svolgono la stessa funzione. Scegli la versione che preferisci.

Se vuoi applicare direttamente la patch al file tcpip.sys, prova "Universal Tcpip.sys Patch".


**********************************
*  Soluzioni ai problemi comuni  *
**********************************
1, Per usare il programma tcpz.exe è necessario eseguirlo come amministratore.

2, Nelle versioni a 64 bit di Vista e Win7, è necessario abilitare la modalità TESTSIGNING. Ecco come fare: 
Apri il Prompt dei comandi come amministratore ed esegui i seguenti comandi:
bcdedit.exe -set loadoptions DDISABLE_INTEGRITY_CHECKS
bcdedit.exe -set TESTSIGNING ON
Al termine, riavvia il computer.
Questo script va avviato solo una volta.
Se compare la scritta "Test Mode" sul desktop, è possibile rimuoverla con "RemoveWatermarkX64.exe".

Non è necessario eseguire queste operazioni nei sistemi operativi a 32 bit.

3, Se l'applicazione va in crash, dopo averla avviata, è probabile che compaia un messaggio che avvisa che non è possibile caricare il driver. Per ripstinare tutto, vai nella seguente chiave di registro:
Per 32 bit:
REG DELETE HKLM\SYSTEM\CurrentControlSet\Services\tcpz-x86
Per 64 bit:
REG DELETE HKLM\SYSTEM\CurrentControlSet\Services\tcpz-x64

Cancella la sezione: [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\Root\LEGACY_TCPZ-X86]
Riavvia il computer e avvia di nuovo il programma per vedere se il problem è stato risolto.

Alcuni antivirus potrebbero bloccare il caricamento del driver di TCP-Z, perciò, potrebbe essere necessario impostare delle regole per consentire il caricamento del driver di TCP-Z.

4, Windows XP supporta File Patcher e Memory Patcher. Vista e Windows 7 supportano solo Memory Patcher.

5, Per applicare la patch al file tcpip.sys in Windows XP x64, è necessario usare TCPZ64.exe per 64 bit.

6, In Windows 2003 e 2008 non ci sono limiti alle connessioni.

7, Vista e Windows 7 supportano un'opzione illimitata in TCP-Z Virtual Driver. Imposta come valore 0 per rendere illimitate le connessioni.

8, E' possibile controllare l'interfaccia del programma anche tramite tatiera. Premi Ctrl + Tab per passare alla scheda successiva; premi Tab per passare al controllo successivo.

//Cronologia delle versioni precedenti:
2008.09.14
  * Aggiornamento alla versione Unicode, ora sono supportate le lingue Inglese/Cinese Cinese semplificato/tradizionale.

2008.09.21
  + Aggiunto un nuovo programma d'installazione.
  * Driver: Azione di rilevamento aumentata. Percentuale di successo aumentata.

2008.10.13
  + Aggiunto il supporto per la lettura del valore dal file tcpip.sys di Windows 7.

2008.10.23  V1.5.3.15
  + Lettura e visualizzazione della creazione depth di tcpip.sys.
  + Patch della memoria di Windows 7 M1.
  * Impossibile leggere le informazioni da alcune interfacce NET.

2008.10.30  V1.5.5.20
  + Patch della memoria di Windows 7 M3 (x86).
  + Aggiunto messaggio di avviso per le CPU AMD multi-core.

2008.11.01  V1.5.6.25
  + Patch della memoria di Windows 7 M3 (x64). (Beta)
  * Limite del file di Windows XP modificato a 1000.
  * Funzione modificata per disabilitare SFC in NT5.
  
2008.11.07  V2.0.0.30 beta
  * Modificata la funzione di ricerca. Percentuale di successo aumentata.

2008.11.12  V2.1.0.33
  + Aggiunto tcpz64.exe, un programma x64 nativo.
  * Modificata la funzione di ricerca.
  * Limite della memoria di XP modificato a oltre 1000.
  * Corretta la compatibilità con le CPU multi-core.
  * Corretto l'errore di caricamento del driver in Windows 7 x64.

2008.11.29  V2.2.0.35
  + Unità virtuale, aggiunta un'opzione per personalizzare il valore limitato. Aggiunta un'opzione illimitata per Vista e Windows 7.
  + Interfaccia del programma, cattura dello schermo con i tasti  F5 e F6. E' necessario il supporto GDI+.
  * Interfaccia del programma, aggiunto manifest CAU di Vista. Potrebbe non essere compatibile con XP SP2, è possibile aggiornare il Service Pack, o continuare a usare la versione 2.1 di TCP-Z. 
  * L'interfaccia del programma può essere ridotta a un singolo file (versione portatile).

2008.12.16  V2.2.1.36
　* Modificato TcpzQueryRegParameters(), aggiunto un parametro nullo iNullAction, NOD32 non riporta più TCP-Z come virus.
　
2008.12.27  V2.3.0.42
　* Modificata la firma digitale dei file del programma.
　+ Modificata l'interfaccia del programma, aggiunta un'interfaccia bellissima.
　+ L'interfaccia del programma mostra l'indirizzo limitato della memoria del kernel e del file “Tcpip.sys”.
　  Per motivi di compatibilità, mostra solo la parte bassa nei sistemi operativi a 64 bit.
　* Corretto il valore limitato del file sconosciuto in Windows 7 Build 6.1.6936.0 e Windows 2003 5.2.3790.4331.
　* Corretto il fallimento della patch del file in Windows XP SP3, a causa dell'impossibilità nel modificare WFP.
　# Nessuna modifica ai driver.

2008.12.29  V2.3.1.43
  * Interfaccia del programma, rimossa la funzione per disabilitare WFP, a causa dell'incompatibilità di questo codice e perchè non c'è nessun SFC disabilitato. La patch del file non riesce sempre al 100%, perchè Windows ripristina automaticamente il file tcpip.sys.
    Metodo alternativo: usare la patch della memoria.

2009.01.08  V2.4.0.46
  + Patch della memoria in Windows 7 x64 6.1.7000.0.
  + L'interfaccia del programma supporta il controllo con la tastiera. Grazie a Aldares. 
                 Ctrl + Tab per passare alla scheda successiva; Tab per passare al controllo successivo.
  * Interfaccia del programma, Applica patch, aumentata la compatibilità della disattivazione di WFP in Windows XP. Grazie a BRD-IlLusioN-CCCP. 
  * Corretta l'interfaccia del programma, l'interfaccia in DPI non-standard non poteva essere visualizzata correttamente. 

2009.02.05, V2.5.1.50
  * Interfaccia del programma, identifica se il file tcpip.sys è il file originale senza modifiche.
  * L'interfaccia del programma supporta le versioni precedenti a Windows XP x64 SP1.
  * L'interfaccia del programma e i driver supportano Windows Vista SP2 RC v.275, x64, 6.0.6002.16659.

2009.03.07, V2.6.0.64 Beta
  + Altre lingue supportate. Tedesco (Mods.sub.cc); Italiano (FSoft); Polacco (PrEzi); Rumeno (Misaki-kun & StelistCristi). Grazie a tutti loro!
  + Statistiche dei tentativi di connessione in entrata e in uscita...
  + Statistiche delle connessioni di ogni programma.
  + Mini bar;
  + Funzione di modifica dell'allineamento dell'apice.
  + Salvataggio delle impostazioni dopo la chiusura del programma.

2009.03.16 V2.6.0.66
  + Support more language. Bulgarian by ExaFlop; Swedish by Marshall Mathers; Thai by Pruthisith; Turkish by Yekta Kayman; Ukraine by ShriEkeR. Thank them!

2009.04.06 V2.6.1.72
  + Support more language. Russian by Serhii Hlodin, Mixa, Qui Sum; Korean by deuxdoom; French by jacklours; Portugese by Anubis. Thank them!
  + Add options in tcpz.ini to customize the upper value of the graph.
  * Fixed: Y-axis label display not correct in big font. Error range of incoming connection graph.
  * Fixed: Transparence percentage display not correct.
  * Fixed: Can't display speed in some computer.
  * Fixed: Network traffic turn to zero when more than 4GB.
  * Fixed: Can't receive the shutdown message.
  * Build with WDK 6001.18002.

2009.04.09 V2.6.2.75
  * Hide the tunnel type of Adapter in Vista/Windows 7.
  * Increase the range of searcher, supports Windows 7 6.1.7077.0 (winmain_win7rc.090404-1255), x86.
