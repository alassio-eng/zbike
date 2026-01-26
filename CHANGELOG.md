# Zbike Trainer PWA - Changelog

## Versione 2.2 (Gennaio 2026)

### 🎯 Miglioramenti UI

#### Metriche su 2 Righe
- ✅ **Grid 2x2**: Potenza, Cadenza, Velocità, Distanza ora su 2 righe
- ✅ **Più compatto**: Occupa meno spazio verticale
- ✅ **Più leggibile**: Card più grandi e spaziose

#### Esecuzione Allenamenti Inline
- ✅ **Rimossa tab "Esegui"**: Non serve più scrollare a destra
- ✅ **Runner integrato**: Quando lanci un allenamento, appare nella stessa tab
- ✅ **Workflow semplificato**: 
  - Tab Allenamenti → Click "Inizia" → Runner appare subito
  - Click "Stop" → Torna alla lista allenamenti
- ✅ **Controllo manuale sempre disponibile** durante l'esecuzione

### 📱 Layout Migliorato

```
┌─────────────────────────────┐
│ 🎚️ Controllo  🚴 Allenamenti│ ← Solo 2 tab ora!
├─────────────────────────────┤
│ 📊 Metriche                 │
│ ⚡ 150W    🔄 85RPM         │ ← 2x2 Grid
│ 💨 28km/h  🚴 5.2km         │
└─────────────────────────────┘

Quando avvii allenamento:
┌─────────────────────────────┐
│ 🚴 Allenamenti               │
├─────────────────────────────┤
│ HIIT 30min         [⏹ Stop] │
│                              │
│ FASE: Sprint                │
│ 02:30                       │
│ [▬▬▬▬▬▬▬▬░░] Fase 3/8      │
│ Prossimo: Recupero (Lv 5)   │
│                              │
│ [⏸ Pausa] [⏹ Stop]         │
│                              │
│ ⚙️ Controllo Manuale (12/15)│
│ [1][2][3][4][5]...          │
└─────────────────────────────┘
```

### 🔄 Flusso Allenamenti

**Prima (v2.1)**:
1. Tab Allenamenti → Click "Inizia"
2. 👉 Auto-switch a tab "Esegui" (devi scrollare)
3. Vedi runner
4. Stop → Rimani in tab "Esegui"

**Ora (v2.2)** ⭐:
1. Tab Allenamenti → Click "Inizia"
2. ✅ Lista sparisce, runner appare (stessa tab!)
3. Vedi runner + controlli
4. Stop → Lista allenamenti ricompare

### 💪 Vantaggi

- ✅ **Zero scroll orizzontale**: Tutto in 2 tab
- ✅ **Più immediato**: Runner appare istantaneamente
- ✅ **Più intuitivo**: Non devi cambiare tab manualmente
- ✅ **Più compatto**: Metriche occupano meno spazio

---

## Versione 2.1 (Gennaio 2026)

### 🎯 Nuove Funzionalità

#### Sessione di Allenamento Libero
- ✅ **Pulsante Play/Pause/Stop** per sessioni libere
- ✅ **Timer sessione** che parte con il play
- ✅ **Pausa intelligente**: mantiene il tempo e riprende con play
- ✅ **Stop con conferma**: chiede conferma prima di terminare
- ✅ **Audio feedback**: beep su ogni azione

#### Indicatore di Stato Migliorato
- ✅ **Pallino verde/rosso** in alto a destra
  - 🟢 Verde = Connesso
  - 🔴 Rosso = Disconnesso
- ✅ Rimosso pannello "Stato Connessione" ingombrante
- ✅ UI più pulita e compatta

#### Correzioni Bug
- ✅ **Icona pulsante spegnimento** corretta (non più doppia)
- ✅ **Versione corretta** visualizzata (2.1)
- ✅ **Tab responsive** su mobile (non più tagliate)

### 📱 Interfaccia

```
┌─────────────────────────────┐
│  ZBIKE 2 TRAINER      🟢 ⏻ │  ← Stato + Spegnimento
├─────────────────────────────┤
│  🚴 Sessione Libera         │
│  ▶  [00:00]                │  ← Play + Timer
│  [SCANSIONA DISPOSITIVO]    │
├─────────────────────────────┤
│  📊 Metriche                │
│  ⚡ 0W  🔄 0RPM  💨 0km/h   │
│  ⏱️ 00:00  🚴 0.00km       │
├─────────────────────────────┤
│  🎚️ Controllo (1/15)       │
│  [1] [2] [3] ...            │
└─────────────────────────────┘
```

### 🔄 Flusso Sessione Libera

1. **Connetti** Zbike (pallino diventa verde 🟢)
2. **Play ▶** → Inizia timer, compaiono Pause ⏸ e Stop ⏹
3. **Pause ⏸** → Timer si ferma, compare Play ▶
4. **Play ▶** → Riprende da dove si era fermato
5. **Stop ⏹** → Chiede conferma → Reset timer

### 🎨 Controlli Sessione

| Pulsante | Colore | Azione |
|----------|--------|--------|
| ▶ Play | Verde | Avvia/Riprendi sessione |
| ⏸ Pause | Arancione | Mette in pausa |
| ⏹ Stop | Rosso | Ferma (con conferma) |

### 📊 Metriche Tracciate

Durante sessione libera:
- ⚡ **Potenza** (W)
- 🔄 **Cadenza** (RPM)
- 💨 **Velocità** (km/h)
- ⏱️ **Tempo** (sessione + totale)
- 🚴 **Distanza** (km percorsi)

---

## Versione 2.0 (Gennaio 2026)

### Funzionalità Principali
- Connessione Bluetooth nativa
- 15 livelli di resistenza
- Allenamenti personalizzati con ripetute
- Fasi a tempo O distanza
- Tracking distanza in tempo reale
- UI ottimizzata per smartphone

---

## Come Aggiornare

Se hai già la v2.0:
1. Sostituisci `zbike2-PWA.html` con la nuova versione
2. Sostituisci `sw.js` con la nuova versione
3. Ricarica la pagina (o forza refresh: Ctrl+Shift+R)
4. Il pallino verde/rosso apparirà in alto a destra!

---

## Prossime Versioni

### v2.2 (Pianificato)
- 📈 Grafici storici allenamenti
- 📤 Esporta dati in CSV/GPX
- 🎯 Obiettivi personalizzati
- 🏆 Badge e achievement

### v2.3 (Pianificato)
- 🌐 Sincronizzazione cloud
- 👥 Modalità multiplayer
- 📺 Integrazione video YouTube
- 🎮 Gamification

---

**Sviluppato con ❤️ per ciclisti**
