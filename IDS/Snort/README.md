# Snort
[](https://www.html.it/pag/69358/installazione-4/)

Snort è *"an open source intrusion prevention system capable of real-time traffic analysis and packet logging"*. Dunque non è solo un IDS ma permette anche di prevenire gli attacchi, esso ha quattro livelli di sicurezza: 
1. Sniffer: cattura i pacchetti
2. Packet logger: legge i pacchetti catturati
3. IDS: monitora e analizza i pacchetti e in caso di pacchetti sospetti notifica l'intrusione
4. IPS: tenta di difendere il sistema dall'attacco


## Installazione 
Andremo a installare l'ultima versione di **Snort**, la **2.9.15.1** su una VM *Ubuntu 19.10*.

Installiamo prima di tutto il pacchetto *Data Acquisition library*, introdotto dalla versione 2.9, volto a creare un livello di astrazione rispetto a chiamate dirette alle funzioni *libpcap* ( libreria che fornisce funzioni per catturare pacchetti ).

Fatto ciò possiamo passare all'installazione vera e propria riportata in *InstallSnort*.

![Alt text](Snort-V.png )

## Regole Snort
Esistono tre modalità per istanziare nuove regole:
1. Download delle [regole ufficiali](https://www.snort.org/advisories/talos-rules-2020-01-22)
2. Download delle [regole della community](https://www.snort.org/downloads/community/community-rules.tar.gz) 
3. Creazione manuale
