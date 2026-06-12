[README.md](https://github.com/user-attachments/files/28874246/README.md)
# tecnoservice-mappa
mappa interventi e gestione tecnici da DB in excel
# Mappa Operativa Interventi — TecnoService Industriale Srl

Strumento web per la gestione e il controllo visivo degli interventi tecnici sul territorio.

---

## Il problema

Chi coordina tecnici sul campo sa che il problema non è mai uno solo: ci sono manutenzioni programmate, chiamate urgenti, preventivi aperti, interventi in attesa di conferma. Tutto insieme, tutto urgente, tutto su clienti sparsi su un territorio ampio.

Il CRM aziendale registra le attività, ma non risponde alla domanda più pratica: **chi ho disponibile vicino a quel cliente?**

La soluzione tradizionale era un foglio Excel con una colonna "Zona" — un numero che identificava l'area geografica del cliente, assegnato tramite una tabella di lookup città→zona. Funzionava, ma richiedeva di tenere tutto in testa: quale tecnico era in quale zona, quali attività erano aperte, chi era già impegnato.

---

## L'evoluzione

Questo progetto nasce per rendere quella logica visiva e immediata.

I dati restano strutturati come nel DB originale (Cliente, Tipo attività, Città, Zona, Tecnico, Stato, Date), ma vengono proiettati su una mappa geografica reale dell'Emilia-Romagna.

Il risultato è una dashboard operativa che permette di:

- vedere in un colpo d'occhio dove sono concentrate le attività aperte
- filtrare per tecnico e capire il suo carico di lavoro sul territorio
- identificare chi è geograficamente più vicino a un nuovo intervento urgente
- tenere separato lo storico (attività chiuse) dal lavoro corrente

---

## Funzionalità

- **Mappa interattiva** con marker colorati per stato: Da fare · Pianificata · Stand by · Da ripianificare · Chiusa
- **Sidebar** con lista attività scrollabile, aggiornata in tempo reale al cambio filtro
- **Filtri** per Stato, Tipo chiamata (CH / MP / INT / NOR_CON / MC) e Tecnico
- **Popup** su ogni marker con dettaglio completo: cliente, tipo, tecnico assegnato, date, note
- **KPI in header**: attività aperte, da pianificare, pianificate, totale

---

## Stack tecnico

| Strumento | Ruolo |
|---|---|
| HTML / CSS / JS | Single-file, zero dipendenze backend |
| Leaflet.js | Mappa interattiva con tile CartoDB |
| GitHub + Netlify | Hosting e deploy automatico |

Il file è completamente autonomo — nessun server, nessuna API, nessun framework. I dati sono incorporati direttamente nel file HTML a partire da un DB Excel strutturato.

---

## Dati

Il dataset utilizzato è fittizio e generato appositamente per questa demo: aziende, numeri di attività e tecnici sono tutti inventati. Le città e le coordinate geografiche sono reali (hinterland bolognese e province limitrofe).

---

## Demo

[tencoservice-mappa.netlify.app/mappa_operativa.html](https://tencoservice-mappa.netlify.app/mappa_operativa.html)

---

*Progetto sviluppato come parte del portfolio professionale di Alessandro Dardi — Operations & Digital Transformation.*
