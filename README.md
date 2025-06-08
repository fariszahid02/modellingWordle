# 🧠 Wordle Game Model – Science of Programming Coursework

This project is my **Science of Programming** coursework submission for Newcastle University. The task involved translating the natural language specification of the New York Times' popular word game **Wordle** into a fully functional Python model.

---

## 📌 Project Summary

The goal of this project was to develop a modular and logically sound model of Wordle, extending the base functionality with strategic enhancements and robust testing using assertions, pre-conditions, post-conditions, and data invariants.

---

## 🛠️ Features & Enhancements

### ✅ Core Implementation
- A custom `Game` class manages game state, guesses, and feedback logic.
- All core gameplay rules of Wordle are implemented, including guess limits and word validation.
- Visual representation of guesses using symbols like `+` (correct place) and `-` (correct letter, wrong place).

### 💡 Hint System
- A new `hint()` operation returns a valid unguessed letter from the answer.
- Guards in place using assertions:
  - Hints are only available while the game is in the `PLAYING` state.
  - Only a single letter is returned.
  - The hint does not repeat previously guessed letters.

### 🔁 Repeated Letter Handling
- Refined the `check_guess()` function to handle repeated letters accurately.
- Moved logic from `check_letter()` to `check_guess()` to analyze the full guess in context, ensuring correct coloring for clues.

### 🔒 Hard Mode
- Introduced a new operation: `hard_guess()`.
- Enforces the Hard Mode rule from the original Wordle: **"Any revealed hints must be used in subsequent guesses."**
- Pre-condition checks ensure compliance; violations raise assertion errors.

---

## 🧪 Testing Strategy

- All unit tests are consolidated into a single code block at the bottom of the notebook.
- Grouped tests include:
  - `check_letter()` – letter-level clue accuracy
  - `check_guess()` – full word guess checking with repeated letters
  - `hint()` – unguessed letter delivery and edge cases
  - `hard_guess()` – ensures constraints are enforced when hints are revealed
- Used `print()` statements to simulate user input/output for visual debugging.

---

## 📈 Additional Improvements

- Added pretty printing of the game state for improved readability and debugging.
- Used Python assertions throughout the model to enforce:
  - Game logic correctness
  - Valid game states and transitions
  - Pre-/post-conditions for all major functions
- Followed a formal software modeling approach with attention to **design-by-contract** principles.

---

## 📘 Reflections & Learning

This project has deepened my understanding of:
- Defensive programming with assertions
- Modeling real-world game logic in code
- Designing with modularity and extensibility in mind
- The role of visual feedback in debugging and user experience

Inspired by other implementations (e.g., Pixegami’s Wordle video on YouTube), I took extra steps to improve maintainability, fairness (especially around repeated letters), and feature completeness.

---


