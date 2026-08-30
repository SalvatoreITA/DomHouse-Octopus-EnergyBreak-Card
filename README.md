# 🐙 DomHouse Octopus Energy Break Card per Home Assistant

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)
[![version](https://img.shields.io/badge/version-v1.0.0-blue.svg)]()
[![maintainer](https://img.shields.io/badge/maintainer-Salvatore_Lentini_--_DomHouse.it-green.svg)](https://www.domhouse.it)

Una Custom Card dal design premium per monitorare in tempo reale le tue sfide **Octopus Energy Break** su Home Assistant.  
Questa card è il compagno visivo perfetto per l'integrazione [Octopus Energy Break Helper](https://github.com/SalvatoreITA/Octopus-EnergyBreak-Helper).

<div align="center">
  <img src="IMAGE.PNG" alt="Card Preview" width="300">
</div>

## 🎁 Sconto Octopus

Se devi attivare un nuovo abbonamento con Octopus Energy puoi usare questo [link](https://octopusenergy.it/octo-friends/quiet-gaur-553): otterrai **uno sconto fino a 50 €**

## ✨ Caratteristiche

* **Design Glassmorphism Moderno**: Interfaccia grafica elegante e pulita con sfondi trasparenti dinamici che si adattano perfettamente a qualsiasi tema di Home Assistant (chiaro o scuro).
* **Banner Ufficiale Integrato**: Collegamento visivo e diretto con l'immagine ufficiale della sfida Energy Break per un look professionale sulla dashboard[cite: 1].
* **Gestione Data e Orari Interattivi**: Riquadri dedicati per visualizzare e modificare al volo la data e la finestra oraria dell'evento (Inizio e Fine) direttamente con un click.
* **Monitoraggio Baseline e Obiettivi**: Visualizzazione immediata della media dei consumi degli ultimi 10 giorni e dei target di riduzione esatti in kWh per assicurarsi gli sconti da 1€ e 3€.
* **Barra Live (HUD in Tempo Reale)**: Un misuratore interattivo che mostra i consumi istantanei durante l'evento, arricchito da tacche per gli obiettivi e colori dinamici (verde, giallo e rosso).
* **Modalità Letargo (Smart Sleep)**: Il sistema riconosce automaticamente se l'evento è attivo o meno, spegnendo la barra e mostrando una schermata pulita e inattiva quando non ci sono sfide in corso.
* **Allarme Visivo Pulsante**: Animazione di emergenza che fa lampeggiare di rosso il riquadro live nel momento esatto in cui si superano i limiti di consumo per lo sconto.

## ⚠️ Prerequisiti
Per far funzionare questa card, **DEVI** prima installare il componente base che calcola i dati.
👉 **[Scarica l'integrazione backend da qui](https://github.com/SalvatoreITA/Octopus-EnergyBreak-Helper/)**.

## 📦 Installazione

### Metodo 1: Tramite HACS (Consigliato)
Poiché la card non è ancora tra i repository predefiniti di HACS, puoi aggiungerla facilmente:

1. Apri **HACS** nel tuo Home Assistant.
2. Vai nella sezione **Frontend** (o Interfaccia Utente).
3. Clicca sui tre puntini in alto a destra e seleziona **Repository personalizzati**.
4. Incolla l'URL di questo repository: `https://github.com/SalvatoreITA/DomHouse-Octopus-EnergyBreak-Card`
5. Scegli la categoria **Lovelace** (o Dashboard) e clicca su Aggiungi.
6. Cerca "DomHouse Octopus PowerUp", clicca su **Scarica** e ricarica la pagina del browser.

### Metodo 2: Manuale
1. Scarica il file `domhouse-octopus-energybreak-card.js` dall'ultima release.
2. Copia il file nella cartella `/config/www/` del tuo Home Assistant.
3. Vai su **Impostazioni > Plance > Risorse** (potresti dover attivare la Modalità Avanzata nel tuo profilo utente per vedere questa voce).
4. Aggiungi una risorsa con URL `/local/domhouse-octopus-energybreak-card` e seleziona il tipo **Modulo JavaScript**.
5. Ricarica la pagina.

## ⚙️ Come Usarla

1. Vai sulla tua Plancia (Dashboard) di Home Assistant.
2. Clicca sulla matita in alto a destra per **Modificare la plancia**.
3. Clicca su **Aggiungi Scheda**.
4. Scorri l'elenco o cerca **"DomHouse Octopus Card - Energy Break"**.
5. Usa l'editor visivo per personalizzare il titolo o nascondere i suggerimenti di strategia.
6. Salva e goditi il tuo PowerUp!

## 🎁 Bonus:Octopus Energy Break - Notifiche Smart (Blueprint)

Un Blueprint per automatizzare le notifiche della tua sfida "Energy Break" su Home Assistant. 
Questo strumento gestisce in totale autonomia gli avvisi di inizio e fine evento, calcolando l'esito della tua sfida in tempo reale.

## ✨ Cosa fa questo Blueprint?

* **Fischio d'inizio:** Ti invia una notifica nel minuto esatto in cui inizia l'Energy Break, ricordandoti i tuoi obiettivi in kWh (Soglia 1€ e Soglia 3€) in modo da sapere subito quanto puoi consumare.
* **Arbitro a fine partita:** Nell'istante in cui la sfida termina, legge il tuo consumo live prima che il sensore si azzeri.
* **Esito dinamico:** A seconda del tuo risultato, riceverai uno dei 3 messaggi personalizzati:
  * 🎉 **Vittoria 3€:** Se sei rimasto sotto la soglia massima di risparmio.
  * 👏 **Vittoria 1€:** Se hai raggiunto l'obiettivo base.
  * ❌ **Sconfitta:** Se hai purtroppo superato i limiti.

Nella cartella `blueprints` di questo repository troverai i file YAML pronti all'uso (Luce e Gas). 

<div align="center">
  <img src="notifiche.jpg" alt="Card Preview" width="300">
</div>

### 🎉 Blueprint
[![Importa Blueprint in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/SalvatoreITA/DomHouse-Octopus-EnergyBreak-Card/refs/heads/main/blueprints/octopus_energybreak_notifiche.yaml)

## ☕ Supporta il Progetto

Ogni piccolo supporto fa un'enorme differenza: mi aiuta a mantenere vivo l'entusiasmo e mi stimola a creare e condividere nuove soluzioni per la community. Grazie di cuore per il tuo aiuto! 🚀

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/salvatore_dh)

## ❤️ Crediti
Sviluppato da [Salvatore Lentini - DomHouse.it](https://www.domhouse.it)
