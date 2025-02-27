# Port Scanner TCP MultiThread 
Un port scanner TCP è uno strumento utilizzato per analizzare le porte di un dispositivo o server su una rete, verificando quali sono aperte, chiuse o filtrate.
Serve principalmente per identificare i servizi in esecuzione su un sistema e per valutare la sicurezza di una rete.

# 🔍 Come funziona?
Il port scanner invia pacchetti TCP a una serie di porte di destinazione e analizza le risposte ricevute per determinare lo stato di ogni porta.
Il funzionamento si basa sulla gestione delle connessioni TCP, che seguono il Three-Way Handshake:

• SYN → Il client invia una richiesta di connessione alla porta target.

• SYN-ACK → Se la porta è aperta, il server risponde con un pacchetto SYN-ACK.

• ACK → Il client completa la connessione con un pacchetto ACK.

Se invece la porta è chiusa, il server risponde con un RST (Reset), e se è filtrata (es.Firewall), potrebbe non rispondere affatto.

# 🎯 A cosa serve?

• Sicurezza e Penetration Testing → Identificare porte aperte e vulnerabilità.

• Amministrazione di rete → Verificare quali servizi sono attivi su un host.

• Rilevamento di servizi → Determinare quali applicazioni girano su un server.

# 🛠 Strumenti | Dipendenze
• Versione Python  →  Python 3.13.0.

• Moduli  →  socket - sys - pyfiglet - rich - json - ThreadPool - os 

• Target  →  scanme.nmap.org (un server pubblico usato per testare scanner di rete).

<img width="455" alt="Port Scanner TCP Multi Thread " src="https://github.com/user-attachments/assets/23223188-f78a-43f0-8c40-328c7116c4e7" />



Per impostazione predefinita, PScan esegue la scansione solo di alcune porte comunemente utilizzate, il cui elenco è disponibile nel file "common_ports.json".

Il repo include anche un file "iana_tcp_ports,json" contenente un numero maggiore di porte e il relativo servizio comune. 
Per utilizzare questo file, basta aggiornare il valore di PORTS_DATA_FILE nella classe PScan.

⚠️⚠️__________________________________________________________⚠️⚠️

• Utilizzo Responsabile: Questo Port Scanner TCP MultiThread è solo a scopo didattico.

• Non utilizzare su siti web senza autorizzazione esplicita.

• Testare in sicurezza: eseguire sempre test di sicurezza in un ambiente controllato e autorizzato.
