# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- [ ] Detail which bugs you found.
- [ ] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. Player enters a guess of 65
2. Game returns "Go LOWER"
3. Player enters a guess of 30, Game returns "Go HIGHER"
4. The player's score is updated after each guess
5. The game ends when the player guesses the right number
or when the player has no more guesses. 

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```

tests/test_game_logic.py::test_winning_guess PASSED                                                                                   [ 16%]
tests/test_game_logic.py::test_guess_too_high PASSED                                                                                  [ 33%]
tests/test_game_logic.py::test_guess_too_low PASSED                                                                                   [ 50%]
tests/test_game_logic.py::test_too_high_guess_tells_player_to_go_lower PASSED                                                         [ 66%]
tests/test_game_logic.py::test_too_low_guess_tells_player_to_go_higher PASSED                                                         [ 83%]
tests/test_game_logic.py::test_hint_direction_with_string_secret PASSED                                                               [100%]

============================================================ 6 passed in 0.08s =============================================================

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
