# Multi-Model Object Detection

Applicazione web per il rilevamento di oggetti, mani e pose corporee in tempo reale utilizzando la fotocamera del dispositivo.

## 📋 Descrizione

Questo progetto è un'applicazione browser-based che combina diversi modelli di machine learning per analizzare il flusso video della webcam e rilevare:

- **Oggetti comuni** (80 classi tramite COCO-SSD)
- **Mani** (tramite Handtrack.js e HandPose)
- **Pose corporee complete** (tramite BlazePose)

## 🚀 Funzionalità

- **Multi-modello**: Supporta 4 diversi modelli di rilevamento selezionabili dall'utente
- **Tempo reale**: Analisi del flusso video in tempo reale
- **Interfaccia configurabile**: Pannello impostazioni per personalizzare i parametri
- **Visualizzazione grafica**: Bounding box e scheletri disegnati sul canvas
- **Log di debug**: Sistema di logging per il troubleshooting

## 🛠️ Tecnologie Utilizzate

- **TensorFlow.js** - Framework per machine learning nel browser
- **COCO-SSD** - Modello per il rilevamento di 80 classi di oggetti
- **Handtrack.js** - Rilevamento rapido delle mani
- **HandPose** - Rilevamento dettagliato dei landmark delle mani
- **BlazePose** - Rilevamento della posa corporea completa

## ⚙️ Impostazioni Disponibili

| Parametro | Descrizione |
|-----------|-------------|
| **Modello Attivo** | Seleziona il modello da utilizzare (COCO, Handtrack, HandPose, BlazePose o Tutti) |
| **Confidenza Minima** | Regola la soglia di confidenza per i rilevamenti (10% - 90%) |
| **Velocità** | Controlla la frequenza di elaborazione (1-4 livelli) |
| **Mostra Log** | Abilita/disabilita il pannello di debug |

## 📦 Come Utilizzare

1. Apri il file `index.html` in un browser moderno (Chrome, Firefox, Edge)
2. Clicca sul pulsante **"AVVIA CAMERA"**
3. Consenti l'accesso alla webcam quando richiesto
4. Usa il pannello impostazioni (⚙️) per configurare il modello desiderato

## 🏗️ Struttura del Codice

```
index.html          # File unico contenente HTML, CSS e JavaScript
```

Il codice è organizzato in un singolo file HTML che include:
- **Stili CSS** per l'interfaccia utente
- **Script esterni** per i modelli TensorFlow.js
- **Logica JavaScript** per:
  - Gestione della webcam
  - Caricamento dei modelli
  - Elaborazione del video frame-by-frame
  - Disegno delle annotazioni sul canvas

## 🔍 Modelli Supportati

### COCO-SSD
Rileva 80 classi di oggetti comuni come persone, auto, animali, cibo, ecc.

### Handtrack.js
Rilevamento veloce della presenza e posizione delle mani.

### HandPose
Rilevamento dettagliato dei 21 landmark di ciascuna mano.

### BlazePose
Rilevamento completo della posa corporea con 33 keypoint del corpo umano.

## 💡 Note

- L'applicazione funziona interamente nel browser, senza bisogno di server backend
- Richiede una connessione internet per caricare le librerie TensorFlow.js dai CDN
- Le prestazioni dipendono dalle capacità hardware del dispositivo

## 📄 Licenza

Progetto open source per scopi educativi e dimostrativi.
