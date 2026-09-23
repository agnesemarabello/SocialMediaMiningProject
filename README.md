# Social Media Mining Project
## Transizione Artistica del Cast di Stranger Things & Sentiment Analysis

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![NetworkX](https://img.shields.io/badge/NetworkX-Graph%20Analysis-orange.svg)](https://networkx.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-f7931e.svg)](https://scikit-learn.org/)
[![Gephi](https://img.shields.io/badge/Gephi-Visualization-4d7c0f.svg)](https://gephi.org/)

Questo repository contiene il codice sorgente, le pipeline di elaborazione dati e gli strumenti di analisi di rete sviluppati per il progetto dell'esame di Social Media Mining. La ricerca analizza la transizione artistica dei membri del cast di *Stranger Things* (concentrandosi su **Djo / Joe Keery**, **Maya Hawke** e **Finn Wolfhard**) verso l'industria musicale, integrando **Network Science** e **Natural Language Processing (NLP)**.
Link alla presentazione : https://canva.link/6ods6tqn26gan6w

---

### 🔍 Obiettivi di Ricerca
1. **Topologia di Rete e Integrazione:** Verificare se i progetti musicali del cast formano cluster di fandom isolati o si integrano organicamente nei rispettivi generi musicali.
2. **Comportamento di Co-ascolto del Pubblico:** Analizzare se il pubblico crea collegamenti strutturati e coerenti con i generi musicali o se si comporta come un'eccezione isolata.
3. **Sovrapposizione delle Community:** Misurare la sovrapposizione strutturale tra il fandom globale della serie TV *Stranger Things* e le fan-base indipendenti degli attori-musicisti.
4. **Inversione di Polarità del Sentiment:** Valutare come il successo di Djo influenzi il sentiment online e il discorso pubblico rispetto al contesto generale della serie TV.

---

### 🛠️ Metodologia e Stack Tecnologico

* **Estrazione Dati:** YouTube Data API v3 (raccolta di commenti, metadati e metriche di engagement) e strutture dati di Last.fm e TMDB.
* **Analisi di Rete:** `NetworkX` per la costruzione dei grafi, proiezioni di reti bipartite (`bipartite.projected_graph`) e metriche topologiche.
* **Sentiment Analysis & Machine Learning:** Pipeline di apprendimento supervisionato con `Scikit-Learn` (`TfidfVectorizer` con n-grammi e `LinearSVC`) per classificare i commenti degli utenti in polarità positiva e negativa.
* **Visualizzazione:** `Gephi` per il rilevamento delle community (algoritmo di Louvain) e layout spaziali delle reti (ForceAtlas 2).

---

### 📂 Struttura del Repository

```text
├── gephi_crossover_music_network.png    # Grafo di co-ascolto con i dati estratti da Last.fm
├── gephi_commenti_youtube_network.png   # Grafo commenti YouTube
├── gephi_music_network_random.png       # Grafo rete random usata per il confronto
├── gephi_tv_cast_network.png            # Grafo cast ottenuto con i dati estratti da TMDB
├── gephi_community_detection.png        # Grafo community detection
├── gephi_proiezione_sui_video.png       # Grafo proiettato contenuto-contenuto (Co-commento video)
└── README.md                            # Documentazione del progetto
