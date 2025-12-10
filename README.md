# Kaun Banega Crorepati C Console Game

## Overview
This C program simulates the Indian quiz show *Kaun Banega Crorepati?* (Who Wants to Be a Millionaire?) in a console interface. Players answer 12 multiple-choice questions with escalating prize money up to ₹1,000,000, using lifelines like 50:50, Phone-a-Friend, and Audience Poll, or quit to claim winnings.

## Features
- 12 predefined questions covering general knowledge, science, history, and programming topics.
- Lifelines: 50:50 (hides two wrong options), Phone-a-Friend (70% correct suggestion), Audience Poll (biased toward correct answer).
- Safe input handling with buffer flushing and line reading to prevent crashes.
- Guaranteed money at milestones (₹10,000 after Q5, ₹320,000 after Q10); wrong answers end the game with guaranteed amount.

## Compilation and Usage
Enter A-D for answers, L for lifelines, Q to quit. Options are case-insensitive; invalid inputs are handled gracefully.

## Code Structure
- **Question Struct**: Stores question text, 4 options, correct index (0-3), and prize value.
- **Key Functions**:
  | Function | Purpose |
  |----------|---------|
  | `flushstdin()` | Clears input buffer.  |
  | `getchoiceline()` | Reads and sanitizes single-character input. |
  | `showquestion()` | Displays question with optional hidden options.  |
  | `lifeline5050()` | Randomly hides two wrong answers.  |
  | `lifelinephone()` | Simulates friend suggestion (70% accurate).  |
  | `lifelineaudience()` | Shows biased poll percentages.  |

Main loop iterates questions, tracks lifelines (one use each), updates prizes, and handles game end conditions.

## Author
K. Rupesh (BTech CSE student project).
