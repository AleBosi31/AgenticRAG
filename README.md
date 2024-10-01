# 🤖 Agentic RAG - Sistema di Risposta Intelligente

Benvenuto nel progetto Agentic RAG! 🎉 Questo sistema combina la potenza del Retrieval-Augmented Generation (RAG) con la ricerca online per fornire risposte accurate e informative alle tue domande.

## 📚 Panoramica

Agentic RAG è un sistema di risposta alle domande che:

1. 🔍 Cerca informazioni rilevanti in un database locale (Qdrant)
2. 🧠 Decide se le informazioni locali sono sufficienti per rispondere alla domanda
3. 🌐 Se necessario, cerca informazioni aggiuntive online 🔜
4. ✍️ Genera una risposta dettagliata basata sul contesto più appropriato

## 🚀 Caratteristiche Principali

- **Ricerca Locale**: Utilizza Qdrant per una ricerca veloce ed efficiente nel database locale
- **Embedding AI**: Sfrutta il modello "text-embedding-ada-002" di OpenAI per generare embeddings semantici
- **Decisione Intelligente**: Usa GPT-4 per decidere se il contesto locale è sufficiente
- **Ricerca Online**: Integra DuckDuckGo per la ricerca di informazioni aggiornate dal web 🔜
- **Generazione di Risposte**: Utilizza GPT-4 per formulare risposte informative e concise

## 🛠️ Installazione

1. Clona il repository:
   ```
   git clone https://github.com/tuousername/agentic-rag.git
   ```
2. Installa le dipendenze:
   ```
   pip install -r requirements.txt
   ```
3. Configura la tua chiave API di OpenAI nel file di configurazione .env

4. Clona il repository di qdrant:
   ```
   git clone https://github.com/qdrant/qdrant?tab=readme-ov-file
   ```
5. Accedere alla cartella qdrant e eseguire l'immagine docker sulla porta 6333:
   ```
   PS: è necessario eseguire Docker Desktop prima
   
   cd qdrant
   docker run -p 6333:6333 qdrant/qdrant
   ```

## 💻 Utilizzo

Per utilizzare Agentic RAG, caricaricare i propri documenti all'interno della cartella data ed esegui lo script principale e poni la tua domanda:

```python
question = "una domanda relativa ai documenti personali caricati"
answer_question(question)
```

## 📋 Requisiti

- Python 3.8+
- OpenAI API key
- Qdrant (installato localmente o accessibile tramite URL)
- Librerie Python: qdrant-client, openai, duckduckgo_search, IPython

## 🤝 Contribuire

Siamo sempre alla ricerca di contributi per migliorare Agentic RAG! Se hai idee o migliorie, non esitare a:

1. 🍴 Forkare il repository
2. 🔧 Creare un nuovo branch per le tue modifiche
3. 🚀 Inviare una pull request

## 📜 Licenza

Questo progetto è distribuito sotto la licenza MIT. Vedi il file `LICENSE` per maggiori dettagli.