<p align="center">
<img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/animated-logo.svg" alt="logo animato" width="50%"> <br>
<i width="80%">Progetto scolastico di gruppo per il riconoscimento di cifre e lettere attraverso Machine Learning, con backend Java, frontend PHP, app Android e server Python.</i>
</p>
<br>

> [!NOTE]
> **Archivio personale del progetto scolastico di gruppo.** Questo repository (`anItalianGeek/digitML`) è conservato come riferimento del lavoro svolto per gli open-day scolastici, senza sviluppo o manutenzione attivi da parte mia. Sorgenti e documentazione del gruppo sono disponibili anche su [`paolomalgarin/DigitML`](https://github.com/paolomalgarin/DigitML).
> Il mio ruolo, riportato nella tabella dei contributori, è **Project manager**. La tabella attribuisce ai rispettivi compagni di squadra Machine Learning, API, app Android e web-app.

# 🤝 Contributors

<i>Un grazie speciale a tutte le persone che hanno contribuito alla realizzazione del progetto:</i>
<br>
<p>
  <a href="https://github.com/paolomalgarin/DigitML/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=paolomalgarin/DigitML" alt="Contributors" />
  </a>
</p>

| Profilo | Ruolo | Area |
|---|---|:---:|
| [@paolomalgarin](https://github.com/paolomalgarin) | Design e web-app | ✨ |
| [@anItalianGeek](https://github.com/anItalianGeek) | Project manager | 💼 |
| [@michelecortiana](https://github.com/michelecortiana) | Machine learning | 🧠 |
| [@Phoeyuh](https://github.com/Phoeyuh) | API | 🐝 |
| [@Benti06](https://github.com/Benti06) | Android app | 📱 |

<br>
<br>

# 📖 INDICE
* 📥 [Installation guide](https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/Documentation/INSTALLATION-OPTIONS.md)
* 📌 [Panoramica](#-panoramica)
* 🏗️ [Architettura & Flusso dei Dati](#%EF%B8%8F-architettura--flusso-dei-dati)
* 🛠️ [Tecnologie Utilizzate](#%EF%B8%8F-tecnologie-utilizzate)
* 📷 [Esempi d’Uso](#-esempi-duso)
* 📊 [Dati](#-dati)
* 📄 [Licenza](#-licenza)

<br>
<br>

# 📌 Panoramica

Il progetto DigitML ci è stato assegnato come attività didattica con l’obiettivo di realizzare un’applicazione distribuita per il riconoscimento di cifre manoscritte.
La consegna prevedeva la creazione di un sistema capace di identificare numeri scritti a mano, da utilizzare durante gli open‑day scolastici per mostrare le competenze acquisite nel triennio di Informatica.
Spinti dalla nostra curiosità e dalla voglia di sperimentare, abbiamo esteso il progetto aggiungendo il riconoscimento delle lettere dell’alfabeto.

> [!TIP]
> Per la configurazione e i prerequisiti dei vari ambienti, consultare la [Guida all'installazione upstream](https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/Documentation/INSTALLATION-OPTIONS.md).

<br>

---
<br>

# 🏗️ Architettura & Flusso dei Dati

Le applicazioni front-end (web-app in PHP e app Android nativa) inviano le richieste all'API Java Servlet, che autentica le chiamate e comunica con il server Python/TensorFlow tramite firma HMAC con chiave condivisa.

<p align="center">
  <img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/data-flow.svg" alt="Flusso dei dati DigitML" width="70%">
</p>
<br>

---
<br>

# 🛠️ Tecnologie Utilizzate

<img src="https://skillicons.dev/icons?i=php,html,css,js,python,tensorflow,java" alt="Icone tecnologie" /> <br>

- **Java Servlet**: API middleware di comunicazione tra i client e il motore di inferenza
- **PHP 8+**: interfaccia web, pannello di controllo e gestione sessioni
- **Android (*Java*)**: client mobile per l'acquisizione del tratto su schermo touch
- **Python 3.8+ (Flask / Waitress)**: microservizio di inferenza
- **TensorFlow / Keras**: reti neurali convoluzionali (CNN) per cifre e lettere

<br>

---
<br>

# 📷 Esempi d’Uso
> *Esempi di funzionamento dell'interfaccia web e dell'app Android sviluppate dal team:*

<p align="center">
  <img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/guessing.gif" alt="Web-app GUI" width="75%">
  <img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/Android-gui.jpg" alt="Android GUI" width="23%">
</p>

> [!WARNING]
> Per istruzioni dettagliate su come eseguire i diversi componenti (API, server Flask, web-app o APK Android), fare riferimento alla [guida di installazione upstream](https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/Documentation/INSTALLATION-OPTIONS.md).

<br>

---
<br>

# 📊 Dati

Dataset utilizzati dal modulo di Machine Learning e metriche di accuratezza riportate dal progetto scolastico:

| NOME | MNIST | A-Z Handwritten Alphabets |
|---|:---:|:---:|
| **Esempio** | <img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/MNIST.png" alt="mnist" width="160"> | <img src="https://github.com/paolomalgarin/DigitML/blob/main/docs/README%20-%20Stuff/A-Z%20Handwritten%20Alphabets.png" alt="A-Z Handwritten Alphabets" width="160"> |
| **Tipo di rete** | CNN _(Convolutional Neural Network)_ | CNN _(Convolutional Neural Network)_ |
| **Validation Accuracy** | **98.6%** | **98.8%** |
| **Training Accuracy** | 99.3% | 99.5% |

<br>

---
<br>

# 📄 Licenza

Il codice presente in questo repository è distribuito sotto licenza MIT — consultare il file [LICENSE](LICENSE) locale e la [licenza upstream del progetto](https://github.com/paolomalgarin/DigitML/blob/main/LICENSE.txt).
