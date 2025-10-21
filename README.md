# 🎧 Phondle

**Phondle** is a Golang + Ebiten audio word challenge game — like Wordle, but for your ears.  
The game uses the **Merriam-Webster API** to play a pronunciation clip of a word, and your goal is to **spell it correctly before time runs out!**

Players can select difficulty tiers, replay pronunciations, and race against the clock.  
It’s part spelling bee, part Wordle, and all chaos. 🐝💥

---

## 🕹️ Gameplay Overview

1. **Select a Difficulty**
   - Easy 🟢 — 4–6 letter common words  
   - Medium 🟡 — 7–8 letter moderate words  
   - Hard 🔴 — 9–10 letter challenging words  
   - Obscure ⚫ — 10+ character monsters for word nerds  

2. **Hear the Pronunciation**
   - Phondle fetches a random word and plays its **official Merriam-Webster pronunciation**.

3. **Type the Correct Spelling**
   - You have **20 seconds** to spell the word correctly.  
   - You can replay the pronunciation as many times as you like within that round.  
   - When the timer hits zero — it’s game over! ⏰

4. **Keep Going**
   - New words load automatically when you get one right.  
   - Your score increases with each correct spelling.

---

## 🧠 Features

✅ Tiered difficulty levels (Easy → Obscure)  
✅ Merriam-Webster audio pronunciations  
✅ 20-second per-word timer  
✅ Replay pronunciation button  
✅ Clean Ebiten menu system  
✅ Smooth quitting and exit handling  
✅ Polished UI transitions  

---

## 🗂️ Project Structure

phondle/
├── main.go # Entry point, initializes Ebiten window
├── game.go # Core game loop and rendering logic
├── menu.go # Main menu for difficulty selection
├── audio.go # Handles API calls and audio playback
├── timer.go # Countdown timer logic
├── easy_words.go # Easy word list
├── medium_words.go # Medium word list
├── hard_words.go # Hard word list
├── obscure_words.go # 10+ character word list
├── go.mod
├── go.sum
├── .env # Contains Merriam-Webster API key
└── assets/
└── fonts/
└── arcade.ttf # Optional custom font

yaml
Copy code

---

## ⚙️ Environment Setup

Create a `.env` file in the project root:

```bash
MW_API_KEY=your_merriam_webster_api_key_here
🧩 Installation
bash
Copy code
# Clone this repo
git clone https://github.com/yourusername/phondle.git
cd phondle

# Set up dependencies
go mod tidy

# Run the game
go run .
🧰 Requirements
Go 1.22+

Ebiten v2

Merriam-Webster Dictionary API key (Get it here)

Working audio output device (headphones or speakers)

🪄 Tips
Can’t catch the pronunciation? Hit Replay — but the timer keeps ticking!

Choose Obscure mode only if you’ve eaten your dictionary for breakfast.

You can exit anytime with Esc or the Quit button.

🧑‍💻 Developer Notes
Phondle uses Ebiten’s Update, Draw, and Layout loop pattern.
Audio playback leverages Go’s audio and http libraries to stream .mp3 clips directly from Merriam-Webster’s CDN.

Future enhancements may include:

Leaderboards

Multiplayer mode

"Streak" scoring system

Visual pronunciation hints 👀

🥇 Credits
Created by: Sam Armentrout
Built with: Golang, Ebiten, and pure chaotic energy.
Dictionary Data: Merriam-Webster API

📜 License
MIT License © 2025 Sam Armentrout

You’re free to play, modify, and share Phondle — just keep it classy.
