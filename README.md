Memory Check 🧠
A fun, interactive memory card game built with HTML, CSS, and JavaScript.

🎯 Overview
Players flip over two cards per turn to find matching pairs. The game ends when all pairs are matched, with moves and time tracked to measure performance.

📸 Demo  


🚀 Features
Shuffle & Deal: Cards are randomized each game

Match Detection: Flips two cards, checks for matches

Move & Timer Tracking: Displays number of moves taken and total time

Win Popup: Shows performance stats and offers replay

Responsive UI: Works across desktop and mobile browsers

➕ Installation
Option A: Play Locally
Clone the repo:

bash
Copy
Edit
git clone https://github.com/yourusername/memory-check.git
cd memory-check
Open index.html in your browser.

Option B: Use a Local Server (for modules or assets)
bash
Copy
Edit

🎮 How to Play
Click (or tap) a card to flip it over.

Flip a second card:

Match? Cards stay face up.

No match? They flip back after a short delay.

Continue until all pairs are matched.

On winning, a modal shows:

Number of moves

Time taken

Option to restart

⚙️ Game Logic
Core files:

index.html – game markup

style.css – styling and animations

app.js – shuffle, flip logic, matching, and state control

Key Logic Snippets
js
Copy
Edit
// Shuffle cards
cards = cards.sort(() => 0.5 - Math.random());

// On card click:
if (!firstCard) {
  firstCard = clicked;
} else {
  secondCard = clicked;
  checkForMatch();
}

// Check match:
if (firstCard.dataset.name === secondCard.dataset.name) {
  disableCards();
} else {
  unflipCards();
}
🧩 Customization
Change grid size by adjusting cardsArray.

Swap card images by adding assets and updating data attributes.

Modify timer/moves thresholds for difficulty levels.

Add sound on flip or match by integrating audio elements.

🛠️ Tech Stack
Vanilla JavaScript

CSS3 for layout and animations

HTML5 with data-* card tagging

🎯 Goals & Learnings
This project helped with:

DOM manipulation for interactive UIs

Game state management (tracking first/second card, matches)

CSS transitions and delayed actions

Responsive design techniques

📦 Future Enhancements
Local High Scores via localStorage

Animations and more elegant flip effects

Difficulty Levels (e.g., grid sizes like 4×4, 6×6)

Touch input improvements for mobile

Multiplayer mode — turn-based scoring

✍️ Contributing
Fork the repo

Create a feature branch

Submit a PR for review

Contributions toward features, bug fixes, or UI improvements are all welcome!

📄 License
This project is MIT licensed. See the LICENSE file for details.



UI design ideas from susanschen/Memory‑Game 
