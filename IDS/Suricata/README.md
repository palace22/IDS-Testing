# Suricata

Suricata è un IDS open-source nato nel 2009, sviluppato dalla OISF ( Open Information Security Foundation ). 

Caratteristica peculiare di qesto IDS è che esegue le analisi in multithreadig, riuscendo a diminuire i consumi della CPU; il suo file di configuzaione è in *.yaml* ed è il competitor per eccellenza di *Snort*. 

Oltre ad essere un IDS è anche un IPS e NSM ( Network Security Monitoring ), oltre a notificare possibili attacchi può inviare notifiche attraverso la rete.


## Installazione

Per l'installazione su *Kali Linux*, basta seguire la guida della pagina ufficiale che riporta le dipendenze e i file e cartelle da creare. 

Andremo a installare *Suricata* come solo IDS. Aprendo il file di configurazione si nota quanto è più intuitivo rispetto a quello di *Snort*. Settiamo il path di un nostro file *.rules* e testiamo.

```yml
default-rule-path: /var/lib/suricata/rules

rule-files:
  - suricata.rules
```

![Alt text](Screen/Suricata.png )

## Regole Suricata



## Test

Abbiamo visto come le regole si Snort sono supportate anche da Suritata dunque proviamo a settarne una e pingare i pacchetti *icmp*:

```
alert icmp any any -> $HOME_NET any (msg:"Qualcuno sta pingando!"; GID:1; sid:10000001; rev:001; classtype:icmp-event;)
```

Troveremo i log complett all'interno dei file in */var/log/suricata/*:

```json
{"timestamp":"2020-02-05T16:59:06.593199+0100","flow_id":1888256170528047,"in_iface":"eth0","event_type":"alert","src_ip":"192.168.1.85","dest_ip":"192.168.1.176","proto":"ICMP","icmp_type":8,"icmp_code":0,"alert":{"action":"allowed","gid":1,"signature_id":10000001,"rev":1,"signature":"Qualcuno sta pingando!","category":"Generic ICMP event","severity":3},"flow":{"pkts_toserver":1,"pkts_toclient":0,"bytes_toserver":98,"bytes_toclient":0,"start":"2020-02-05T16:59:06.593199+0100"}}
```






