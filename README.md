Kindly refer to the [Google Drive link](https://drive.google.com/drive/folders/1UDaI8kAzwYDs0BdxYMK6umG73e0rhl06?usp=sharing) for the video demonstration and the release APK.

---

# Quiz Game App

This is a mobile application built using **Flutter** for Android and iOS that provides an interactive quiz game experience. The app allows users to take quizzes, see their answers, check their results, and receive feedback in real-time. 

---

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Installation](#installation)
5. [Folder Structure](#folder-structure)
6. [App Overview](#app-overview)
7. [Code Explanation](#code-explanation)
8. [Contributing](#contributing)
9. [License](#license)

---

## Introduction

The **Quiz Game App** allows users to engage in interactive quizzes. The app presents questions, tracks user progress, and provides a countdown timer for each question. The app also keeps track of the user's selected answers and evaluates them based on correct/incorrect responses. At the end of the quiz, the app displays a result screen showing the user's score and correct answers.

---

## Features

- **Interactive Quiz Interface:** Users can take a quiz with multiple choice questions.
- **Timer:** Each question has a countdown timer, which moves the user to the next question once the time runs out.
- **Real-Time Answer Selection:** Users can select their answers in real time.
- **Question Progress:** Shows the current question number and the total number of questions.
- **Results Page:** Displays the user’s performance at the end of the quiz, with selected answers and correct answers.
- **Color-Coded Options:** Selected answers are highlighted with different colors depending on whether they are correct or incorrect.

---

## Tech Stack

- **Flutter**: The cross-platform framework used for building the mobile app.
- **Dart**: The programming language used in Flutter.
- **Android & iOS**: The app is designed to run on both Android and iOS platforms.

---

## Installation

Follow the steps below to set up the Quiz Game app locally on your machine:

### Prerequisites

Make sure you have the following installed:
- **Flutter SDK**: [Flutter Install Guide](https://flutter.dev/docs/get-started/install)
- **Dart SDK** (comes bundled with Flutter)
- **Android Studio** or **Visual Studio Code** (with Flutter and Dart plugins)
- **Xcode** (for iOS development on macOS)

### Steps to Install

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/quiz_game_app.git
   ```
2. Navigate to the project directory:
   ```bash
   cd quiz_game_app
   ```
3. Install the dependencies:
   ```bash
   flutter pub get
   ```
4. Run the app on an Android or iOS emulator, or connect a physical device:
   ```bash
   flutter run
   ```

---

## Folder Structure

Here’s an overview of the folder structure of the project:

```
quiz_game_app/
├── android/                # Android-specific configurations and code
├── ios/                    # iOS-specific configurations and code
├── lib/                    # Flutter app's source code
│   ├── constant/           # Constants (colors, app configuration)
│   ├── model/              # Models (Quiz, Question, Option)
│   ├── presentation/       # Screens (QuizScreen, ResultScreen)
│   ├── main.dart           # Entry point of the application
├── test/                    # Unit and widget tests
├── pubspec.yaml             # Flutter project configuration (dependencies)
├── pubspec.lock             # Locked versions of dependencies
└── README.md                # Project documentation (this file)
```

---

## App Overview

### 1. **QuizScreen**
The main screen of the app where the user answers the questions. It displays:
- The current question and options.
- A timer for each question.
- The user's selected answer is tracked.

**Key Functions:**
- `startTimer`: Starts the countdown timer for each question.
- `moveToNextQuestion`: Moves the app to the next question after the timer ends or when the user selects an answer.
- `optionSelected`: Tracks the user's selected answer to change the UI color accordingly (correct/incorrect).

### 2. **ResultScreen**
This screen is shown after the quiz ends, displaying the results:
- The answers selected by the user.
- The correct answers.
- The total score achieved.

---

## Code Explanation

### Main Components:
- **QuizScreen**: This is the main screen where the quiz is presented to the user. It manages the display of questions and answers, the countdown timer, and transitions to the next question when time runs out or when the user selects an answer.
- **ResultScreen**: After completing the quiz, this screen displays the results, including the selected answers, correct answers, and the final score.

### Important Variables and Logic:
- **selectedAnswers**: A `Map<int, int?>` that tracks the answers selected by the user for each question.
- **correctAnswers**: A `Map<int, int?>` that tracks the correct answers for each question.
- **currentQuestionIndex**: Keeps track of the index of the current question.
- **remainingTime**: The remaining time for the current question (60 seconds).
- **optionSelected**: Keeps track of the selected options for each question to visually highlight them.

### Timer Implementation:
- A `Timer` is used to update the countdown every second.
- When the timer runs out, the quiz automatically moves to the next question or submits the quiz if it's the last question.

### UI Design:
- The app uses **Material Design** components to create a user-friendly interface.
- The app dynamically updates the UI based on the timer and user interactions.
- Each question is displayed along with the possible answers, and the selected answer is highlighted based on correctness.

---

## Contributing

We welcome contributions to improve this quiz game app. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request to merge the changes.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This README provides all the details you need to understand, set up, and contribute to the **Quiz Game App**. Enjoy building and improving it!

