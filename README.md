# SEVEN — Daily Word Grid

**SEVEN** is a minimalist, single-file daily word puzzle game[cite: 1]. Players are challenged to guess a randomly selected 7-letter word within 7 attempts. 

Designed to be exceptionally lightweight, the game is built entirely with vanilla JavaScript, CSS, and HTML. It requires no external assets, frameworks, or database backends, making it perfectly suited for easy self-hosting or dropping into any web environment.

I built this game for my mum, who loves word games and said she wished there were more. Here you go mum! The games inspiration of seven comes from "The Seven" episode of Seinfeld (Season 7, Episode 13).

## 🎯 Features

*   **The Rule of Seven:** 7 letters to guess, 7 attempts to get it right.
*   **Daily Challenges:** A new word is generated every day at midnight (UK time), utilising a deterministic random number generator to ensure all players get the same word on the same day.
*   **Second-Chance Bonus Round:** If a player loses the daily game, they are offered one extra chance to play a unique "Bonus Word" to save their daily win streak.
*   **Hint System:** A built-in hint button allows players to reveal the exact position and identity of one letter from the target word.
*   **Offline Stat Tracking:** Win rates, games played, current streaks, and max streaks are saved securely to the browser's `localStorage`.
*   **Dictionary Validation:** Uses a curated list of exactly 7-letter words valid in Collins Scrabble Words (CSW). Invalid or duplicate guesses flash red/orange and are rejected without penalising the player's turn count.
*   **Responsive UI:** A dynamic board grid automatically scales to fit any screen size, complete with smooth CSS animations (flip, pop, shake, and dance) and touch-friendly mobile keyboards.

## 🕹️ How to Play

1. Type a valid 7-letter word and press **ENTER**.
2. The colour of the tiles will change to show how close your guess was to the word:
   * **Green:** The letter is in the word and in the correct spot.
   * **Orange:** The letter is in the word but in the wrong spot.
   * **Grey:** The letter is not in the word in any spot.
3. Guess the word before you run out of all 7 attempts. 

## 🚀 Installation & Deployment

Because SEVEN is completely self-contained, deployment is as simple as it gets.

1. Clone or download the repository.
2. Upload it to any static web host, local server environment (like Nginx/Apache/Caddy), or simply open the file directly in a modern web browser.

No build steps, no package managers, and no API keys required.

## 🛠️ Tech Stack

*   **HTML5** (Structure)
*   **CSS3** (Custom properties, grid, flexbox, keyframe animations)
*   **Vanilla JavaScript** (ES5/ES6 concepts, DOM manipulation, `Intl.DateTimeFormat` for time zone handling)
*   **Storage:** Window `localStorage` API
