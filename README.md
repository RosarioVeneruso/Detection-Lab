# SIEM - Detection Lab 🚀🔍

Questo progetto è stato realizzato come parte di una challenge del canale YouTube **MYDFIR** e rappresenta la creazione di un laboratorio di **Detection & Response** utilizzando lo stack **ELK**, un **C2 server** con Mythic, e un sistema di **ticketing** con osTicket. L'obiettivo è simulare scenari di attacco e configurare un'infrastruttura che consenta di monitorare, rilevare e rispondere agli incidenti di sicurezza.

---

## 📄 Descrizione del Progetto

Il progetto prevede i seguenti step principali:

### 1. Creazione dell'Infrastruttura su Vultr 🌐
   - **Cloud Provider**: Vultr
   - **Server ELK**: Per centralizzare i log e creare dashboard di monitoraggio.
   - **Fleet Server**: Per coordinare gli agent Elastic all'interno di una **Virtual Private Cloud (VPC)**.
   - **Macchine Virtuali**:
     - **Ubuntu** e **Windows** (al di fuori della VPC).
   - **Firewall Configuration**: Configurazione delle regole di firewall per permettere il traffico dati tra agent e server ELK.

### 2. Simulazione di Attacchi e Creazione degli Alert 🚨
   - **Simulazione di Attacchi Brute Force**:
     - **SSH** su Ubuntu.
     - **RDP** su Windows.
     - Attacchi lanciati da una macchina esterna con **Kali Linux**.
   - **Creazione di Alert** su **Kibana** per rilevare i tentativi di brute force.
   - **Dashboard con Chronoplot**: Visualizzazione temporale degli attacchi rilevati.

### 3. Configurazione di un C2 Server per la Persistenza 🎯
   - **Mythic C2 Server**: Installazione e configurazione di un **Command and Control (C2)** server per coordinare gli attacchi e mantenere la persistenza nelle macchine compromesse.

### 4. Implementazione di un Sistema di Ticketing 📝
   - **osTicket Server**: Installazione di **osTicket** all'interno della VPC per gestire gli alert generati.
   - Configurazione di regole per la generazione automatica di **ticket**:
     - Alert per tentativi di brute force (SSH/RDP).
     - Alert per le attività rilevate dal **C2 server Mythic**.

---

## 🛠️ Tecnologie Utilizzate

- **Cloud Provider**: Vultr
- **SIEM Platform**: ELK Stack (Elasticsearch, Logstash, Kibana)
- **Fleet Server**: Elastic Agent Management
- **Linux Distribution**: Ubuntu, Kali Linux
- **C2 Server**: Mythic
- **Sistema di Ticketing**: osTicket
- **Simulazioni di Attacco**: Brute Force su SSH e RDP

---

## 📊 Dashboard e Visualizzazioni

Le dashboard create su Kibana includono:
- **Visualizzazione Temporale degli Attacchi**: Grafici Chronoplot per monitorare i tentativi di brute force.
- **Dashboard di Monitoraggio C2**: Panoramica delle attività sospette e delle connessioni stabilite tramite il server Mythic.
- **Alert Filtering**: Filtro e visualizzazione degli alert per una risposta rapida.

---

## 📁 Struttura del Repository

- `docs/`: Contiene la documentazione completa delle fasi del progetto in formato PDF.
  - [01 - Setup del Lab su Vultr](./docs/01-setup-lab-vultr.pdf)
  - [02 - Configurazione di ELK e Fleet Server](./docs/02-configurazione-elk-fleet.pdf)
  - [03 - Installazione degli Agent e Configurazione Firewall](./docs/03-agent-firewall-setup.pdf)
  - [04 - Simulazione Attacchi e Configurazione Alert](./docs/04-simulazione-attacchi.pdf)
  - [05 - Installazione di Mythic C2](./docs/05-installazione-mythic.pdf)
  - [06 - Setup di osTicket](./docs/06-setup-osticket.pdf)
  - [07 - Analisi e Report Finale](./docs/07-analisi-report-finale.pdf)

---

## 📥 Come Avviare il Progetto

1. **Clona il Repository**:
   ```bash
   git clone https://github.com/tuoutente/siem-detection-response-lab.git
   cd siem-detection-response-lab
