# Intrusion detection System

L'**IDS** è un componente hardware o software ( come nel nostro caso ) che ha il fine di rilevare, salvare i log e notificare ( a volte anche prevenire: Intrusion Prevention System) accessi non autorizzati alla rete.

Un IDS può essere di tre tipi:
* Network IDS: internamente alla rete locale
* Host IDS: Internamente a un host 
* Hybrid IDS

Verrano installati e testati due tra gli **Intrusion Detection System** più conosciuti e validi:

* ### Snort
* ### Suricata

Per i dettagli si rimanda alle due cartelle presenti. Si descrivono qui le conclusioni e il confronto.

## Conclusioni e confronto

**Snort** si può considerare il padre degli IDS, Martin Roesch, colui che lo sviluppò è stato il primo a creare un sistema flessibile, leggero e soprattutto open-source di Intrusion Detection System. Essendo il primo è anche l'IDS che vanta di una community molto ampia a differenza del "neo arrivato" **Suricata**. Le regole Snort sono in costante aggiornamento da parte della community, inoltro la sistassi non è troppo difficile, chiunque può cimentarsi a creare una regola e testare Snort. Suricata permette di utilizzare anche le regole di Snort, inoltre ha le proprie regole che permettono di utilizzare alcune features non presenti in Snort per esempio il *file detection* e il *file extraction*. 

Il *file extraction* è una funzionalità la quale, una volta che un pacchetto ha corrisposto ad una regola con l'opzione *filestore* attiva,  permette di salvare il file o la parte di file contenuto nel pacchetto così da poterlo analizzare più accuratamente.

Insieme a questo uno dei punti a favore di Suricata è che è stato sviluppato molto più recentemente di Snort, da qui il supporto al multithreading, quasi indispensabile visto l'aumento di traffico che si sta verificando anno dopo anno. Per quanto riguarda Snort, ad oggi non ci sono soluzioni semplici per poterlo eseguire in multithread, ma questa caratteristica sarà implementata nella futura versione, attualmente in beta, Snort3.

Abbiamo visto come ognuno dei due IDS ha i propri vantaggi e svantaggi. La preferenza di uno rispetto a l'altro è da rimandarsi allo scopo del suo utilizzo e al tipo e alla quantità di traffico dati del proprio sistema.

