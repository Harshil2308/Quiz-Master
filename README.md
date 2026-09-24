# 🧠 Quiz Master

A timed 2D quiz game developed using **Unity and C#**.

The game presents randomized multiple-choice questions and challenges the player to answer within a limited amount of time.

The project focuses on **data-driven gameplay, ScriptableObjects, UI systems, timers, randomization, score calculation, and game-state management**.

## 🎮 Gameplay

The player answers a series of multiple-choice questions.

For each question:

1. A question is displayed.
2. Four possible answers are presented.
3. The player has limited time to answer.
4. The selected answer is evaluated.
5. The correct answer is displayed.
6. The score is updated.
7. The next question is loaded.

At the end of the quiz, the player's final percentage score is displayed.

## ✨ Features

### 📝 Data-Driven Questions

Questions are stored using Unity **ScriptableObjects**.

Each question contains:

* Question text
* Four answer choices
* Correct answer index

This separates question data from the main quiz gameplay logic.

New questions can therefore be created and configured through Unity's Inspector without modifying the main quiz script.

### 🔀 Randomized Questions

Questions are selected randomly from the available question pool.

After a question is selected, it is removed from the current list so that the same question does not appear again during the same quiz session.

### ⏱️ Timed Questions

Each question has a countdown timer.

The timer:

* Counts down while the player is answering.
* Stops when an answer is selected.
* Handles unanswered questions when time expires.
* Displays the correct answer.
* Automatically moves to the next question.

### 📊 Score System

The game tracks:

* Number of questions seen
* Number of correct answers
* Final percentage score

The score is calculated as:

```text
Correct Answers / Questions Seen × 100
```

### 📈 Progress Bar

A progress bar tracks the player's progress through the quiz.

The maximum value is automatically set based on the number of questions.

### 🖥️ UI Feedback

The project uses **TextMesh Pro** for UI text.

The interface provides feedback for:

* Correct answers
* Incorrect answers
* Timeouts
* Current score
* Quiz progress
* Final score

### 🔄 Replay System

After completing the quiz, the player can replay the level.

The active scene is reloaded to start a new quiz session.

## 🛠️ Technologies

* **Engine:** Unity
* **Language:** C#
* **UI:** TextMesh Pro / Unity UI
* **Data System:** ScriptableObjects
* **Genre:** Quiz / Educational
* **Version Control:** Git & GitHub

## 🧠 Programming Concepts

This project helped me practice:

* C# scripting
* Unity MonoBehaviour
* ScriptableObjects
* Data-driven game design
* Randomization
* Lists and collections
* Timers
* UI programming
* Game state management
* Scene management
* Event-driven gameplay
* Score calculation
* Component-based architecture

## 📂 Main Scripts

| Script           | Responsibility                                                   |
| ---------------- | ---------------------------------------------------------------- |
| `Quiz.cs`        | Controls question selection, answers, progression and quiz logic |
| `QuestionSO.cs`  | Stores reusable question and answer data                         |
| `Timer.cs`       | Controls question countdown and answer-display timing            |
| `ScoreKeeper.cs` | Tracks correct answers and calculates the final score            |
| `GameManager.cs` | Controls quiz/end-screen state and replay                        |
| `EndScreen.cs`   | Displays the final percentage score                              |

## 🔄 Gameplay Flow

```text
             Start Quiz
                 ↓
          Load Question
                 ↓
        Random Question
                 ↓
       Display 4 Answers
                 ↓
           Start Timer
                 ↓
       ┌─────────┴─────────┐
       ↓                   ↓
  Answer Selected       Time Expires
       ↓                   ↓
 Check Answer        Show Correct Answer
       ↓                   ↓
 Update Score             Wait
       └─────────┬─────────┘
                 ↓
          Load Next Question
                 ↓
          All Questions?
           ┌─────┴─────┐
          No           Yes
          ↓             ↓
    Next Question    End Screen
                        ↓
                  Final Score
```

## 🎯 What I Learned

This project helped me understand how to separate **game data from gameplay logic** using ScriptableObjects.

I also gained practical experience building a complete gameplay loop involving question management, randomization, timers, UI feedback, scoring, game-state transitions, and scene management.

## 🚀 Future Improvements

Possible improvements include:

* Multiple quiz categories
* Difficulty selection
* High-score system
* Local score persistence
* Question difficulty scaling
* Sound effects
* Background music
* Question statistics
* Lifelines such as 50/50
* Main menu
* Category selection
* Leaderboard system

## 📸 Screenshots

Add gameplay screenshots here.

```text
Coming soon
```

## 🎥 Gameplay

Add a gameplay video/GIF here.

```text
Coming soon
```

## 👨‍💻 Author

**Harshil Patel**

Game Programming Student | Unity | C# | Unreal Engine

[GitHub](https://github.com/Harshil2308)
