# 🥁 ChartPlay

**ChartPlay** is an open-source ecosystem for creating, editing, and visualizing frame-based, audio-synchronized music charts. Initially focused on drums and inspired by rhythm games like *Rock Band*, ChartPlay is designed for real-time playback on **Raspberry Pi** with HDMI output and low-latency audio for practice or performance.

---

## 🚀 Features

- 🎧 Chart editor with audio waveform + transient mapping
- ⏱️ Frame-based custom chart file format (`.cplay`)
- 🖥️ Visual playback engine using Pygame or WebGL
- 🎚️ Supports full mix or drumless audio tracks
- 🧠 AI-ready for automatic transient detection
- 🧩 Modular system for future instrument support (guitar, bass, vocals, etc.)
- 🐧 Runs on PC/Linux and optimized for Raspberry Pi

---

## 📁 `.cplay` Chart Format

A JSON-based structure designed for speed, clarity, and cross-platform compatibility.

```json
{
  "version": "1.0",
  "title": "Everlong",
  "artist": "Foo Fighters",
  "author": "ChartPlayUser",
  "framerate": 60,
  "bpm": 146,
  "audio": "everlong_drumless.wav",
  "instruments": {
    "drums": [
      { "frame": 32, "time": 0.533, "part": "kick", "style": "normal" },
      { "frame": 46, "time": 0.767, "part": "snare", "style": "ghost" }
    ]
  }
}
💡 Future updates will include multi-instrument layers, advanced note styles, and MIDI mapping.

🧰 Project Structure
bash
Copy
Edit
ChartPlay/
├── editor/              # Desktop editor (PyQt or Electron-based)
├── player/              # Raspberry Pi playback engine (Pygame or WebGL)
├── tools/               # Audio analyzer & transient detector
├── formats/             # File format specs and docs
├── songs/               # Sample charts and audio
└── README.md
📦 Getting Started
🖥️ Editor (PC/Linux)
Clone the repo:

bash
Copy
Edit
git clone https://github.com/ChartPlay/ChartPlay.git
cd ChartPlay/editor
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt  # or npm install if Electron
Run the editor:

bash
Copy
Edit
python main.py
🐍 Playback (Raspberry Pi)
Install required packages:

bash
Copy
Edit
sudo apt install python3-pygame python3-numpy
Run the player:

bash
Copy
Edit
cd ChartPlay/player
python3 player.py path/to/song.cplay
You can also configure player.py to auto-launch on boot for a kiosk-style setup.

🛠️ Tools
audio_analyzer.py: Extracts transient hits from .wav or .mp3

Optional stem separation via Spleeter or Demucs

🖲️ Recommended Hardware
Device	Description
Raspberry Pi 4/5	Visualizer engine
HDMI display	Scroll-based note highway
USB mouse	Control menu / start & stop playback
IEM or headphones	Low-latency monitoring
Optional GPIO buttons	For hands-free chart control

🧪 Roadmap
 Add full MIDI support for real-time input

 Web-based editor (React + Tone.js)

 Advanced practice mode (loop, tempo scaling)

 Guitar and vocal instrument support

 Custom controller support (USB/MIDI pads)

🤝 Contributing
We welcome contributions! Feel free to:

Submit issues or feature requests

Fork the repo and submit a pull request

Join development discussions

Development Stack
Python (editor, analyzer, player)

Qt / Electron (UI)

Pygame / WebGL (visualizer)

JSON-based .cplay format

📜 License
ChartPlay is licensed under the MIT License.
See LICENSE for more details.

🎓 Credits & Inspiration
Inspired by the musical clarity of Rock Band and the educational value of real-time musical feedback systems.
Special thanks to open-source tools like librosa, Pygame, and Spleeter.

🔗 Stay tuned at github.com/ChartPlay
