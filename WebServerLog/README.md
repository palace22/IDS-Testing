# Web Server Log Analisys

L'analisi dei log dei web server è essenziale per poter monitorare chi e come agisce con il nostro server. 
Le principali informazioni che vengono riportate sono:
* Numero, durata, data e luogo della visita;
* Pagine visitate, numero di volte e periodo;
* Sistema operativo e browser utilizzato;
* Errori durante la visita ( pagine inesistenti, errori del server, etc.);

Da questi e altri dati attraverso analisi statistiche e comparazioni con attacchi noti è possibile capire se il nostro server è a rischio o meno. 

Per effettuare un analisi dei log di un server ci sono varie possibilità:
1. Analizzare manualmente i log; è una soluzione impensabile sia perchè la quantità di dati può essere troppa sia perchè l'occhio umano può lasciarsi sfuggire strghe rilevanti essendo i log riportati in file di test e apparentemente molto simili;
2. Implementare un sistema di analisi di log con software di analisi di stream come ad esempio Kafka e Spark;
3. Utilizzare un apposito tool; molto comodo in quanto i dati sono mostrati anche con grafici, spesso esistono sistemi di notifica di errori;

I tool che verranno analizzati sono:
* ### GrayLog
* ### AWStats
