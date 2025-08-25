### **Welcome to the Pac-Man Challenge!**

We aim to develop the Pac-Man game enhanced with AI and cloud features that connect all players.

1. **Objective:** Your goal is to navigate the maze to eat all the pellets while avoiding the ghosts.
2. **Game Elements:**  pellets, each pallet 10 points, power pellets, and four colorful ghosts who will chase you.
3. **Controls:** Use the arrow keys to move Pac-Man.
4. **Power Pellets:** Grab the power pellets in the corners to temporarily turn the tables on those annoying ghosts!


### **The Global Leaderboard**

See how you stack up against all other players in real-time, this isn't just your personal high score.

1. **Set Your Name:** When you start, you'll be prompted for a name that is saved in your browser for the event.
3. **Instant Updates:** Your score and remaining lives are sent to the shared database the moment they change.
4. **Platform:** The live leaderboard uses _Google's Firebase Realtime Database_.
5. **Database URL:** All data is sent to the following URL: https://pacman-game-8c8bc-default-rtdb.firebaseio.com/
6. **Data Path:** Player scores are stored under the /leaderboard path in the database.
7. **Data Format:** The game sends an object with the following structure for each player: { name: "PlayerName", score: 150, lives: 3 }.


### **Your AI Assistant**

Get instant help by clicking the _"ASK AI"_ button to send your game state to an AI model for a strategic recommendation 😉

The game sends the current positions of Pac-Man, the maze structure, and the ghosts to an LLM, which analyzes the situation to find the best escape route.

1. **AI Model:** You should use the _qwen/qwen3-coder_ model.
2. **API Endpoint:** Requests are sent to _https://openrouter.ai/api/v1/chat/completions_
3. **API Key:** An example key is sk-or-v1-b73a98f37d0e2de9eb9d63245ed98b8e6fec47e466521da4ce24565d7
4. **Escape Route:** The AI will identify the most immediate threat and suggest the best direction to move to get out of a tight spot.


### Dynamic Weather Themes

1. **select a city:** the selected city affects the game’s visual theme (background, color, or speed of pac man) to match the real-time weather of the chosen location.


### **Real-Time Chat**

On the right side of the screen is the **live chat box**, which connects you with every other player. 

1. **Set Your Name:** When you start, you'll be prompted for a name that is saved in your browser for the event.
2. **Platform:** The live chat uses _Google's Firebase Realtime Database_.
3. **Database URL:** All data is sent to the following URL: https://pacman-game-8c8bc-default-rtdb.firebaseio.com/
4. **Data Path:** All messages are stored under the /messages path.
5. **Data Format:** Messages are sent as an object: { name: "PlayerName", text: "Translated text", timestamp: ... }

