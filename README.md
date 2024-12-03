# SIEM - Detection Lab 🚀🔍

Questo progetto è stato realizzato come parte di una challenge del canale YouTube **MYDFIR** e prevede la creazione di un laboratorio completo di Detection e Response. Utilizzando lo stack **ELK**, un server di Command & Control (C2) basato su **Mythic**, e un sistema di ticketing con **osTicket**, il progetto si propone di simulare scenari realistici di attacco e risposta. L'infrastruttura configurata consente di acquisire e analizzare log provenienti da server **Windows** e **Linux**, monitorare attività come attacchi Brute Force e autenticazioni tramite RDP e SSH, e gestire alert e indagini tramite dashboard interattive e sistemi di ticketing. L'obiettivo finale è costruire un ambiente pratico per imparare a monitorare, rilevare, investigare e rispondere a incidenti di sicurezza informatica.

---

# Fasi operative del progetto:

- Progettazione dell'archittetura di rete utilizzata
- Predisposizione di una VPC sul cloud provider **Vultr** e deployment di un server con Elasticsearch e Kibana
- Inserimento all'interno della VPC di un Fleet Server
- Predisposizione di un server Windows e di un server Ubuntu al di fuori della VPC
- Installazione Elastic agents su tali macchine al fine di monitorare l'attività di queste
- Simulazione tentativi di autenticazione su tali macchine, generazione di alert su Elasticsearch
- 
## 📁 Struttura del Repository

- `Days/`: Contiene la documentazione completa delle fasi del progetto in formato PDF.
  - [01 - Diagramma dell'infrastruttura](https://github.com/RosarioVeneruso/Detection-Lab/blob/main/Days/Day%201%2030-day-MyDfir-Challange.png)
  - [02 - Introduzione allo stack ELK](https://github.com/RosarioVeneruso/Detection-lab/blob/493dfec62c8480937383f034012db6670894c592/Days/Day%202%20-%20ELK%20%20Stack.pdf)
  - [03 - Setup di Elasticsearch](https://github.com/RosarioVeneruso/Detection-lab/blob/493dfec62c8480937383f034012db6670894c592/Days/Day%203%20-%20Elasticsearch%20Setup.pdf)
  - [04 - Setup di Kibana](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%204%20-%20Kibana%20Setup.pdf)
  - [05 - Setup del server Windows](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%205%20-%20Windows%20Setup.pdf)
  - [06 - Introduzione agli agent di Elastic](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%206%20-Elastic%20Agents.pdf)
  - [07 - Setup del 'Fleet Server' e dell'agent sul server Windows](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%207%20-Elastic%20Agent%20and%20Fleet%20Server%20Setup.pdf)
  - [08 - Sysmon: monitoraggio degli eventi sul server Windows](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%208%20-%20Sysmon.pdf)
  - [09 - Setup di Sysmon](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%209%20-%20Sysmon%20Setup.pdf)
  - [10 - Acquisizione dei log di Sysmon e Windows Defender e trasmissione ad Elasticsearch tramite agent](https://github.com/RosarioVeneruso/Detection-lab/blob/c29a027dadb16460b28a710a55a9a9468cd54165/Days/Day%2010%20-%20Elasticsearch%20Ingest%20Data.pdf)
  - [11 - Cos'è un attacco Brute Force](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2011%20-%20Brute%20Force%20Attack.pdf)
  - [12 - Setup del server Ubuntu](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2012%20-%20Ubuntu%20Server%2024.02%20Installation.pdf)
  - [13 - Setup dell' Elastic agent sul server Ubuntu](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2013%20-%20Elastic%20Agent%20on%20Ubuntu.pdf)
  - [14 - Rilevazione attività di Brute Force sul server Ubuntu](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2014%20-%20Create%20Alerts%20and%20Dashboards%20in%20Kibana.pdf)
  - [15 - Introduzione sul servizio RDP](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2015%20-%20Remote%20Desktop%20Protocol%20.pdf)
  - [16 - Rilevazione eventi relativi all'autenticazione su server Windows e Ubuntu](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2016%20-%20Create%20Alerts%20and%20Dashboards%20parte%202.pdf)
  - [17 - Creazione dashboard per l'attività di autenticazione tramite RDP e SSH sui server Windows e Ubuntu](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2017%20-%20Create%20Alerts%20and%20Dashboards%20parte%203.pdf)
  - [18 - Introduzione al Command & Control](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2018%20-%20Command%20and%20Control%20Introduction.pdf)
  - [19 - Diagramma di attacco sul server Windows](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2019%20-%20Attack%20Diagram.pdf)
  - [20 - Setup di un server Mythic](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2020%20-%20Mythic%20Server%20Setup.pdf)
  - [21 - Installazione dell'agent di Mythic sulla macchina attaccata](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2021%20-%20Mythic%20Agent%20Setup.pdf)
  - [22 - Creazione di alert e dashboard basati sulla telemetria generata da Mythic](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2022%20-%20Create%20Alerts%20and%20Dashboards%20in%20Kibana%20-%20parte%204.pdf)
  - [23 - Introduzione sul sistema di ticketing](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2023%20-Ticketing%20System.pdf)
  - [24 - Setup di osTicket](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2024%20-osTicket%20Setup.pdf)
  - [25 - Integrazione di osTicket con Elasticsearch e generazione di un ticket](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2025%20-osTicket%20%2B%20ELK%20Integration.pdf)
  - [26 - Come investigare su attacchi Brute Force SSH](https://github.com/RosarioVeneruso/Detection-lab/blob/8ecdfe8ed8ef126d63acb88ffac8e91534cde1fd/Days/Day%2026%20-Investigate%20SSH%20Brute%20Force%20Attack%20.pdf)
  - [27 - Come investigare su attacchi Brute Force RDP](https://github.com/RosarioVeneruso/Detection-lab/blob/74bbf4704291c02ecfedb170cbf56153c45911b3/Days/Day%2027%20-Investigate%20RDP%20Brute%20Force%20Attack.pdf)
  - [28 - Come investigare sull'attività di Mythic](https://github.com/RosarioVeneruso/Detection-lab/blob/74bbf4704291c02ecfedb170cbf56153c45911b3/Days/Day%2028%20-Investigate%20Mythic%20Agent%20.pdf)
  - [29 - Installazione dell'EDR Elastic Defend](https://github.com/RosarioVeneruso/Detection-lab/blob/74bbf4704291c02ecfedb170cbf56153c45911b3/Days/Day%2029%20-Elastic%20Defend%20Setup%20Tutorial.pdf)
  - [30 - Situazioni di troubleshooting affrontate nel progetto](https://github.com/RosarioVeneruso/Detection-lab/blob/74bbf4704291c02ecfedb170cbf56153c45911b3/Days/Day%2030%20-Troubleshooting.pdf)
