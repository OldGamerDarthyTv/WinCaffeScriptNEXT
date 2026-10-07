# ☕ OGD WINCAFFÈ BOOSTER — CONSOLE ENGINE
### *Suite Professionale PowerShell per Ottimizzazione Kernel, DPC Latency & Gaming*
**Versione Script:** `10.0.2.5` ➔ `10.0.3.0HF1`  
**Autore:** Luigi Sestili Spurio — **#OGD Productions** *(OldGamerDarthy)*  
**Co-sviluppato con:** Antigravity (Google DeepMind)  
**Licenza:** GNU General Public License v3.0  
**Repository Ufficiale:** [https://github.com/OldGamerDarthyTv/WinCaffeNEXT](https://github.com/OldGamerDarthyTv/WinCaffeNEXT)  

---

```
   ( (           +-----------------------------------------------------------+
    ) )          |        OGD WINCAFFÈ BOOSTER — CONSOLE ENGINE              |
  .........      |      "Il motore kernel e tweaking per il tuo PC"          |
  | #OGD  |]     +-----------------------------------------------------------+
  \       /      |       EDIZIONE 10.0.3.0HF1 — MENU 100% NUMERATI           |
   ~~~~~~~       +-----------------------------------------------------------+
```

---

## 🌟 1. IL MOTORE CONSOLE: MASSIMA POTENZA E CONTROLLO DIRETTO

**OGD WinCaffè Console Engine (`10.0.3.0HF1`)** è lo strumento PowerShell avanzato progettato per intervenire in profondità sull'ecosistema **Windows 10 e Windows 11**. 

Nato dall'esperienza di **OldGamerDarthy (#OGD Productions)**, lo script opera a livello di sottosistemi kernel, scheduler multimediale MMCSS, gestione interrupt IRQ/MSI, power plan dinamici, caching filesystem I/O e telemetria, fornendo al gamer e al power user uno strumento chirurgico, affidabile e trasparente.

---

## ⚡ 2. LE GRANDI NOVITÀ DI WINCAFFÈ CONSOLE `10.0.3.0HF1`

Questa nuova versione Hotfix 1 della linea 10.0.3.0 introduce modifiche determinanti nate direttamente dal banco di prova su hardware reale e dai feedback della community:

### 🔢 1. Menu 100% Numerati con Interfaccia e Ordine Intatti
- **Layout Originale Preservato:** Mantenuta fedelmente la celebre interfaccia originale a due colonne (`CORE PROFILES` a sinistra, `TOOLS AND HARDWARE MODULES` a destra, con pannello operativo sotto) senza alcuna alterazione visiva.
- **Ordine Rigorosamente Invariato:** Ogni voce rispetta l'identica posizione originaria.
- **Addio Lettere Sparse:** Le opzioni ora usano una sequenza numerica ordinata e intuitiva da `[1]` a `[31]`, con `[0]` per Uscita/Indietro.
- **Retrocompatibilità Totale:** Il motore accetta in modo trasparente sia i nuovi numeri sia le vecchie lettere (`[A]`, `[F]`, `[U]`, `[W]`, `[J]`, `[O]`, `[G]`, `[R]`, ecc.) per chi è abituato ai comandi storici.

### 🛡️ 2. Sblocco Limite Punti di Ripristino al Primo Avvio
- **Risoluzione Errore Ripristino:** In Windows, una policy di frequenza standard (`SystemRestorePointCreationFrequency` impostata a 1440 minuti / 24 ore) bloccava la creazione di punti di ripristino ravvicinati.
- **Sblocco Automatico & VSS:** WinCaffè imposta silenziosamente il valore a `0`, attiva il servizio Copia Shadow (VSS) e assicura la protezione sul disco di sistema `C:\`.
- **Trasparenza & Notifica:** All'avvio una notifica chiara avvisa dello sblocco del limite. Nel menu `[9] RESET & GESTIONE RIPRISTINO` l'utente ha la facoltà di consultare lo stato e **riattivare il limite predefinito a 24 ore** con un semplice clic se desiderato.

### 🎬 3. Nuovo Splash Screen Veloce, Compatto e Sempre Skippabile
- **Rimossa la vecchia pioggia Matrix:** Rallentava l'avvio della console.
- **Nuovo Box ASCII Veloce (1.5s):** Elegante logo OGD a tazzina con palette Dark Espresso & Caramel Gold.
- **Sempre Skippabile:** Basta premere `INVIO` o qualsiasi tasto per saltare istantaneamente l'animazione ed entrare nel menu.

### 🎮 4. Risoluzione Definitiva Crash su Euro Truck Simulator 2 (ETS2)
- **Paging Executive Elastico:** La chiave `DisablePagingExecutive = 1` viene attivata **SOLO se la RAM è $\ge$ 32 GB**. Su configurazioni con 16 GB di RAM viene forzata a `0` per prevenire la saturazione del non-paged pool e crash Out-Of-Memory durante lo streaming di modelli e texture Prism3D.
- **Salvaguardia Driver NVIDIA GeForce RTX (Serie 30 / 40 / 50):** Rimosse le vecchie chiavi legacy di registro `PowerMizerLevel = 1` e `PerfLevelSrc = 0x2222`. Su schede RTX moderne con GPU Boost 5.0 queste chiavi causavano timeout del driver e l'errore `DXGI_ERROR_DEVICE_REMOVED`.
- **MMCSS Clock Rate Certificato a 10000 (1 ms):** Riportato a `10000` per `Games` e `Pro Audio`, eliminando il tweak non standard `2710` responsabile di micro-stutter con l'engine audio FMOD.
- **Protezione CPU AMD Single-CCD:** Salvaguardia di processori come Ryzen 5 7600 evitando logiche di core parking non idonee.

### 🤫 5. Rilevamento Silenzioso e Trasparente all'Avvio
- Nessun prompt interattivo o domanda bloccante: modello di CPU, GPU, RAM totale, chassis (Desktop vs Laptop) e versione di Windows vengono identificati all'istante in background.

### 🤝 6. Ringraziamento Speciale a Lorenzo
- Un ringraziamento ufficiale a **Lorenzo**, inserito nei crediti della console e dell'applicazione, per il prezioso testing su Ryzen 7600 + RTX 4060 Ti che ha permesso l'identificazione e la risoluzione di questi problemi.

---

## 📋 3. MAPPA COMPLETA DEI 31 MODULI GUIDATI

```
====================================================================================================
                        MENU PRINCIPALE CONSOLE — OGD WINCAFFÈ 10.0.3.0HF1                         
====================================================================================================
   CORE PROFILES (Ottimizzazioni di Sistema)        |  TOOLS AND HARDWARE MODULES                   
---------------------------------------------------+------------------------------------------------
   [1]  WinCaffe 4.3.2 ALL GAMES (Classico)        |  [17] Diagnostic & Performance Test           
   [2]  WinCaffe 25H2 GAMING OPTIMIZER             |  [18] USB Polling & Input Lag Optimizer       
   [3]  WinCaffe ULTIMATE OPTIMIZER                |  [19] GPU Driver Cleaner & Optimizer          
   [4]  WinCaffe BALANCED (Uso Quotidiano)         |  [20] Storage & SSD / NVMe Accelerator        
   [5]  WinCaffe NETWORK & LATENCY BOOST           |  [21] Network Adapter & TCP Optimizer         
   [6]  WinCaffe VISUAL & DESKTOP BOOST            |  [22] Windows Telemetry & Privacy Cleaner     
   [7]  WinCaffe AUDIO & MULTIMEDIA (MMCSS)        |  [23] CPU Affinity & Core Parking Engine      
   [8]  WinCaffe MEMORY (RAM Clean & Standby)      |  [24] Memory Compressor & SuperFetch Manager   
   [9]  WinCaffe RESET & GESTIONE RIPRISTINO       |  [25] Windows Update & Component Repair       
   [10] WinCaffe BENCHMARK & STABILITY CHECK       |  [26] Gaming Services & Background Tasks      
   [11] WinCaffe HARDWARE DETECT & INFO            |  [27] DirectPlay & Legacy Game Support        
   [12] WinCaffe LAPTOP POWER & BATTERY PROFILE    |  [28] Visual Effects & Desktop Responsiveness 
   [13] WinCaffe TIMER RES & SYSTEM CLOCK          |  [29] Security & Exploit Protection Tuning    
   [14] WinCaffe GPU DEDICATED (NVIDIA / AMD)      |  [30] Game Bar & DVR Optimization             
   [15] WinCaffe HYPER THREADING & SMT TUNER       |  [31] MSI Mode & Interrupt Affinity (IRQ)     
   [16] WinCaffe REGISTRY DEFRAG & HEALTH          |                                                
---------------------------------------------------+------------------------------------------------
   PANNELLO OPERATIVO:                                                                             
   [0]  Esci dalla Console                         |  [C] Controlla Aggiornamenti Online GitHub     
====================================================================================================
```

---

## 🚀 4. REQUISITI E AVVIO RAPIDO

### Requisiti di Sistema:
- **Windows 10 (64-bit)** o **Windows 11 (64-bit)** (compatibile fino a 24H2/25H2).
- **PowerShell:** Funziona perfettamente sia su **Windows PowerShell 5.1** integrato sia su **PowerShell 7.x (pwsh)**.
- **Privilegi di Amministratore:** Lo script richiede privilegi elevati per modificare chiavi di registro di sistema e gestire servizi kernel.

### Come Avviare lo Script:
1. **Tramite doppio clic rapido:** Fai doppio clic sul file `AVVIA_WINCAFFE_CONSOLE.cmd` incluso nel pacchetto.
2. **Da terminale PowerShell (come Amministratore):**
   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   .\OGD_WinCaffe_10.0.3.0HF1.ps1
   ```
3. **Se WinCaffè è installato:** Digita semplicemente `wincaffe` in qualsiasi finestra PowerShell per avviare la console.

---

## 🔒 5. SICUREZZA E BACKUP
- **Punto di Ripristino Automatico:** All'inizio di ogni ottimizzazione viene generato un punto di ripristino di sistema completo.
- **Ripristino Totale nel Menu [9]:** In caso di necessità, il modulo `[9] RESET` permette di ripristinare i valori predefiniti di Windows per rete, MMCSS, power plan, servizi e frequenza dei ripristini.

---
**OGD Productions — Luigi Sestili Spurio (OldGamerDarthy)**  
*Supporto, guide e community Discord:* [https://discord.gg/9Dvr7wkafC](https://discord.gg/9Dvr7wkafC)  
