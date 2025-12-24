# Sonoran Memory Match (JavaFX)

A themed **memory matching card game** built in **Java + JavaFX** with multiple game modes, user accounts, saved progress, and a leaderboard.  
Designed around Sonoran/Arizona-inspired decks (cacti, cities, mammals, mountains, reptiles).

https://github.com/user-attachments/assets/48b89173-1b1a-4cdb-87f4-134848b7d46c

---

## Features

- **JavaFX GUI** (multiple screens/panes: title, login, gameplay, leaderboard, user stats)
- **5 themed decks**: `cacti`, `cities`, `mammals`, `mountains`, `reptiles`
- **Multiple game modes**
  - **Normal**: classic matching (pairs)
  - **Easy**: more duplicates on the board (easier to find matches)
  - **Timed**: **60-second** countdown
  - **Limited Guess**: **15 guesses** to finish
  - **Match 4**: match **four of a kind**
- **Account system**
  - Create an account + log in
  - Default “mock” accounts exist so the leaderboard isn’t empty
- **Local persistence**
  - Prompts on startup to read saved data
  - Prompts on exit to save
  - Saves to a local file: `objects.ser`
- **Unit tests included** (JUnit 5) under `src/tests/`
- **Documentation**
  - Generated Javadoc in `doc/` (open `doc/index.html`)

---

## How to Play

1. Launch the app.
2. **Log in** (or create an account).
3. From the title screen, pick a mode:
   - Normal / Easy / Timed / Limited Guess / Match 4
4. Choose a theme by clicking a card back (cacti, cities, mammals, mountains, reptiles).
5. Click cards to flip them and try to clear the board.

---

## Tech Stack

- **Java**
- **JavaFX** (GUI + media/audio)
- **JUnit 5** (tests)

Project code is organized into:
- `src/model/` — game logic + data structures (Round, Table, Account, etc.)
- `src/controller_view/` — JavaFX UI panes + event handling

---

## Running the App

**Main entry point:** `src/controller_view/MemoryGameGUI.java`

### IDE (IntelliJ / Eclipse / VS Code)
1. Open the project folder.
2. Make sure **JavaFX** is configured for your IDE (controls + media).
3. Run `controller_view.MemoryGameGUI`.

### Command Line (JavaFX SDK required on Java 11+)
```bash
javac --module-path /path/to/javafx/lib \
  --add-modules javafx.controls,javafx.media \
  -d out $(find src -name "*.java")

java --module-path /path/to/javafx/lib \
  --add-modules javafx.controls,javafx.media \
  -cp out controller_view.MemoryGameGUI
```

---

## Contributors

This was a team project built collaboratively by Brett, Brianna, Maleika, and Ray.
