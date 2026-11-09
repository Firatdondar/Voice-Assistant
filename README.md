# 🎙️ Desktop Voice Assistant (Tkinter & Google Speech API)

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![GUI](https://img.shields.io/badge/GUI-Tkinter%20%26%20Pillow-blue)
![Speech](https://img.shields.io/badge/Speech-Google%20STT%20%26%20gTTS-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

A multi-threaded **Python Desktop Voice Assistant** featuring an interactive **Tkinter GUI**, real-time speech-to-text recognition via **Google Speech Recognition (`SpeechRecognition`)**, and natural text-to-speech audio synthesis powered by **gTTS** and **Pygame Mixer**.

---

## ✨ Key Features

- **Hands-Free Voice Command Recognition:** Continuously listens in a background daemon thread using ambient noise calibration (`adjust_for_ambient_noise`) without freezing the Tkinter GUI.
- **Natural Text-to-Speech (TTS) Feedback:** Synthesizes spoken responses via `gTTS` and plays them asynchronously through `pygame.mixer`.
- **Voice-Controlled GUI Selection:** Supports selecting color buttons (`Red`, `Blue`, `Green`, `Yellow`, `Purple`) and visual object cards (`Apple`, `Pear`, `Car`, `Bicycle`) either by voice command or mouse click.
- **Voice Note Dictation & Time Queries:** Responds to conversational prompts (*"What time is it?"*, *"How are you?"*) and records timestamped voice notes (`note_YYYY-MM-DD_HH-MM-SS.txt`).

---

## 🗂️ Project Structure

```text
Voice-Assistant/
├── assets/
│   ├── apple.jpeg           # Apple button icon
│   ├── bicycle.jpeg         # Bicycle button icon
│   ├── car.jpg              # Car button icon
│   └── pear.jpeg            # Pear button icon
├── main.py                  # Tkinter GUI & background voice recognition loop
├── requirements.txt         # Python dependencies
├── LICENSE                  # MIT License
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Firatdondar/Voice-Assistant.git
cd Voice-Assistant
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch the Assistant
```bash
python main.py
```

---

## 🗣️ Supported Voice Commands

| Category | Example Voice Command | Action |
| :--- | :--- | :--- |
| **General** | `"How are you?"` | Assistant replies with status |
| **Time** | `"What time is it?"` | Speaks current local time (`HH:MM`) |
| **Notes** | `"Take note"` / `"Note this"` | Records speech and saves `note_<timestamp>.txt` |
| **Colors** | `"Red"` / `"Blue"` / `"Green"` / `"Yellow"` / `"Purple"` | Triggers corresponding color action |
| **Objects** | `"Apple"` / `"Pear"` / `"Car"` / `"Bicycle"` | Triggers corresponding object card |
| **System** | `"Exit"` / `"Close"` / `"Stop"` | Gracefully terminates voice loop |

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.
