# Zbike Trainer PWA v2.0

## 📱 Progressive Web App per Zbike 2

App completa per controllare il rullo Zbike 2 tramite Bluetooth con funzionalità avanzate di allenamento.

---

## ✨ Novità Versione 2.0

### 🎯 Funzionalità Principali:
- ✅ **Connessione Bluetooth** nativa a Zbike 2
- ✅ **15 livelli di resistenza** controllabili
- ✅ **Metriche real-time**: Potenza, Cadenza, Velocità, Distanza, Tempo
- ✅ **Allenamenti personalizzati** con salvataggio
- ✅ **Ripetute/Intervalli** configurabili
- ✅ **Durata O Distanza**: ogni fase può essere in minuti o km
- ✅ **Notifiche audio** stile sci
- ✅ **UI ottimizzata** per smartphone
- ✅ **Tracking distanza** durante allenamento
- ✅ **Installabile** come app nativa (PWA)

### 🆕 Miglioramenti v2.0:
- 🚴 **Distanza in km** tracciata e visualizzata
- 📏 **Fasi a distanza**: crea fasi basate su km invece che minuti
- 🔁 **Ripetute ricostruite**: quando modifichi un allenamento, le ripetute non sono più "esplose"
- 📱 **UI compatta**: ottimizzata per schermi smartphone
- 🎨 **Power button** con icona corretta
- 📊 **Tab responsive**: non si tagliano più su mobile

---

## 📦 File Inclusi

```
zbike-trainer/
├── zbike2-PWA.html    → App principale
├── sw.js              → Service Worker (cache v2.0)
├── manifest.json      → Manifest PWA
└── README.md          → Questo file
```

---

## 🚀 Installazione

### Opzione 1: GitHub Pages (CONSIGLIATO)

1. Crea repository GitHub "zbike-trainer"
2. Upload tutti i file
3. Vai in **Settings** → **Pages**
4. Source: **main branch**
5. Dopo 2 minuti, URL disponibile: `https://username.github.io/zbike-trainer/zbike2-PWA.html`

### Opzione 2: Server Locale

```bash
# Metti i file in una cartella
python -m http.server 8000

# Apri browser
http://localhost:8000/zbike2-PWA.html
```

### Opzione 3: Netlify Drop

1. Vai su https://app.netlify.com/drop
2. Trascina i 3 file
3. URL disponibile istantaneamente

---

## 📱 Installazione come App

### Su Android:
1. Apri l'URL in Chrome
2. Menu → **"Aggiungi a Home"**
3. L'app apparirà nella home come app nativa

### Su iPhone/iPad:
⚠️ Safari non supporta Web Bluetooth
- Usa l'app da browser Chrome/Edge su PC
- Oppure tablet Android

---

## 🎯 Come Usare

### 1. Connessione
- Accendi Zbike 2
- Apri app → Tab **"Controllo"**
- Click **"Scansiona Dispositivo"**
- Seleziona Zbike dalla lista
- Connesso! ✅

### 2. Controllo Manuale
- Usa i 15 pulsanti per cambiare resistenza
- Vedi metriche in tempo reale
- Distanza si accumula automaticamente

### 3. Creare Allenamenti

**Fase Normale:**
- Nome: "Riscaldamento"
- Modalità: **⏱️ Min** (tempo) o **🚴 Km** (distanza)
- Valore: 5 min o 3 km
- Livello: 1-15

**Ripetuta:**
- Lavoro: 30 sec, Livello 14
- Recupero: 60 sec, Livello 5
- Ripetizioni: 8x
- Totale automatico: 12 min

### 4. Eseguire Allenamenti
- Tab **"Allenamenti"** → Click **"▶️ Inizia"**
- L'app cambia resistenza automaticamente
- Beep audio ai cambi fase
- Controllo manuale sempre disponibile

---

## 🔧 Aggiornamenti Futuri

Quando modifichi l'app:

1. **Aggiorna versione** in `zbike2-PWA.html`:
   ```html
   Versione <strong>2.1</strong>
   ```

2. **Aggiorna cache** in `sw.js`:
   ```javascript
   const CACHE_NAME = 'zbike2-v2.1';
   ```

3. Ricarica su GitHub → Utenti riceveranno update!

---

## 📊 Compatibilità

| Piattaforma | Browser | Bluetooth | PWA | Consigliato |
|-------------|---------|-----------|-----|-------------|
| Android | Chrome | ✅ | ✅ | ✅ |
| Android | Edge | ✅ | ✅ | ✅ |
| Windows | Chrome | ✅ | ❌ | ✅ |
| Mac | Chrome | ✅ | ❌ | ✅ |
| iOS | Safari | ❌ | ✅ | ❌ |

---

## 🆘 Risoluzione Problemi

### Non Trova Zbike
- Verifica Zbike sia acceso
- Riprova scansione
- Controlla permessi Bluetooth (Android)

### Distanza Non Si Aggiorna
- Verifica velocità venga letta (deve essere > 0)
- Riconnetti dispositivo

### App Non Si Installa
- Verifica sia su HTTPS (non http://)
- GitHub Pages usa HTTPS automaticamente

### Pulsanti Tagliati su Mobile
- Versione 2.0 ha risolto questo problema
- Se persiste, ruota schermo in landscape

---

## 📝 Note Tecniche

- **Protocollo**: FTMS (Fitness Machine Service)
- **UUID Servizio**: 0x1826
- **Resistenza**: 10% - 150% (15 livelli)
- **Calcolo Distanza**: Integrazione velocità/tempo
- **Velocità Media Stimata**: 25 km/h (per fasi a distanza)
- **Audio**: Web Audio API (beep sintetizzati)

---

## 📄 Licenza

Uso personale

---

## 🚴 Buon Allenamento!

**Versione Corrente**: 2.0
**Ultimo Aggiornamento**: Gennaio 2026
**Sviluppato con**: HTML5, JavaScript, Web Bluetooth API
