# 🎮 Tic-Tac-Toe Futuristic

> An interactive Tic-Tac-Toe game with a futuristic UI, multiple themes, AI opponents, visual effects, and many more cool features!

<div align="center">
  <a href="https://aditiaangga.github.io/tictactoe/" target="_blank">
    <img src="https://img.shields.io/badge/🎮-Play%20Now-brightgreen?style=for-the-badge&logo=github&logoColor=white&color=#8B5CF6" alt="Play Now">
  </a>
</div>

> 🌐 **Live Demo:** [https://aditiaangga.github.io/tictactoe/](https://aditiaangga.github.io/tictactoe/)

![Status](https://img.shields.io/badge/Status-Live%20%26%20Ready-brightgreen)
![Tech](https://img.shields.io/badge/Tech-HTML%20%7C%20CSS%20%7C%20Vanilla%20JS-blue)
![AI](https://img.shields.io/badge/AI-Minimax%20Algorithm-purple)

---

## ✨ **Features**

### 🎯 **Game Modes**
| Mode | Description |
|------|-------------|
| 👥 **2 Players** | Play with a friend, taking turns |
| 🤖 **AI Easy** | Play against a random-move AI |
| 🧠 **AI Hard** | Play against an unbeatable **Minimax** AI! |

### 🎨 **5 Beautiful Themes**
| Theme | Description |
|-------|-------------|
| 🌈 **Gemini** (default) | Blue-purple-pink gradient inspired by Google Gemini |
| 💎 **Light Crystal** | Light theme with crystal vibes |
| 🌃 **Neon Cyberpunk** | Green-pink neon on a dark background |
| 🎀 **Pastel Dream** | Soft pastel tones |
| 🌙 **Midnight Gold** | Elegant gold accents at midnight |

### 🖥️ **Visual Features**
- **Glass-morphism UI** — Modern frosted-glass design (backdrop-filter blur)
- **Animated Gradient** — Living, moving gradient on the heading
- **Particle Background** — Animated canvas particles in the background
- **Confetti 🎊** — Confetti explosion when someone wins
- **Winning Line** — Smooth SVG animated winning line
- **Pop-in Animation** — X/O symbols appear with a bouncing animation
- **Hover Preview** — See your symbol before placing it
- **Responsive Design** — Perfect layout on phones, tablets, and desktops

### 🔊 **Audio**
- Synthetic sound effects using **Web Audio API** (no external audio files)
- Distinct sounds for: cell click, victory, and draw
- Mute/unmute toggle button

### 🏆 **Score & Persistence**
- Live scoreboard (X — Draw — O)
- **LocalStorage** — Scores persist even after closing the page
- **URL Sharing** — Share scores via link! Example: `?x=3&o=2&d=1`
- Custom player names (saved to localStorage)

### 🎨 **Extras**
- ✅ **Custom Player Names** — Rename Player X and Player O
- 🔗 **Share Score Link** — Copy score link to clipboard
- 🍞 **Toast Notifications** — Lightweight notifications at the bottom of the screen
- 📱 **Fully Responsive** — From 360px screens to desktop

---

## 🚀 **How to Run**

This project is **100% client-side** — just open the HTML file in your browser!

### Option 1 — Direct Open
```bash
# Clone the repository
git clone https://github.com/aditiaanggaperdana/tictactoe.git

# Open in browser
cd tictactoe
start index.html
```

### Option 2 — Via Live Server (recommended)
```bash
# Install VS Code Live Server extension
# Right-click index.html → "Open with Live Server"
```

### 🎯 **Play Online Now**
The game is live on **GitHub Pages**! No installation needed:

👉 **[https://aditiaangga.github.io/tictactoe/](https://aditiaangga.github.io/tictactoe/)**

### Option 3 — Host Your Own
Upload this folder to any static hosting service:
- [Vercel](https://vercel.com) ⚡
- [Netlify](https://netlify.com)
- [GitHub Pages](https://pages.github.com)
- [Cloudflare Pages](https://pages.cloudflare.com)

---

## 🧠 **Tech Stack**

| Technology | Usage |
|------------|-------|
| **HTML5** | Page structure |
| **CSS3** | Styling with CSS Variables, Flexbox, Grid, Animations |
| **Vanilla JavaScript (ES6+)** | All game logic — no frameworks |
| **Web Audio API** | Real-time sound synthesis |
| **Canvas API** | Background particles & confetti |
| **SVG** | Winning line animation |
| **localStorage** | Score & player name persistence |
| **Minimax Algorithm** | Optimal AI opponent |

---

## 🎮 **How to Play**

1. **Select Mode** — Click the mode buttons at the top (2 Players / AI Easy / AI Hard)
2. **Set Names (optional)** — Click "Set Names" to customize player names
3. **Pick a Theme** — Choose your favorite visual theme
4. **Start Playing!** — Click a cell to place your symbol
5. **X goes first** — Symbol X (✕) always starts
6. **Win!** — Get 3 symbols in a row (horizontal, vertical, or diagonal)

### 🎯 AI Tips
- **AI Easy** → Random moves, great for beginners
- **AI Hard** → Uses the Minimax algorithm — the AI is **unbeatable**! Best you can get is a draw.

---

## 📂 **File Structure**

```
📁 tictactoe/
├── 📄 index.html       # Single complete file (HTML + CSS + JS) — single-page app
└── 📄 README.md        # You are here!
```

> This project is intentionally built as a **single file** (`index.html`) for maximum simplicity and portability. All styles and logic are self-contained.

---

## 🔧 **How the AI Works (Minimax)**

The Hard AI uses the **Minimax** algorithm — a decision-making algorithm for zero-sum two-player games.

```
                    MAX (O) — AI's turn
                   /    |    \
          MIN (X)      MIN      MIN
         /  |  \      /  \      /  \
   MAX   MAX MAX   MAX MAX   MAX MAX
   (score +10 if O wins, -10 if X wins, 0 if draw)
```

- AI plays as **O** (maximizing player)
- Human plays as **X** (minimizing player)
- AI picks the move with the highest score at each level
- This algorithm guarantees the AI **never loses** 🛡️

---

## 🤝 **Contributing**

This project is open source! Want to contribute? Here's how:

1. Fork this repository
2. Create a new branch (`git checkout -b cool-feature`)
3. Commit your changes (`git commit -m 'Add cool feature'`)
4. Push to the branch (`git push origin cool-feature`)
5. Open a Pull Request

### Future Ideas
- [ ] Online multiplayer via WebSocket
- [ ] Global leaderboard
- [ ] More varied X/O animations
- [ ] Selectable sound effects
- [ ] Tournament mode (best of 3/5)

---

## 👨‍💻 **Author**

**Aditia Angga Perdana**

- 🌐 Website: [aditiaangga.my.id](https://aditiaangga.my.id)
- 🐙 GitHub: [@aditiaangga](https://github.com/aditiaangga)
- 💼 LinkedIn: [Aditia Angga Perdana](https://linkedin.com/in/aditia-angga-perdana-67a862aa)

---

## 📄 **License**

This project is created for learning and portfolio purposes. Feel free to use, study, and further develop it.

---


