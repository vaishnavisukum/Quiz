Quiz Application (Python CLI)

This is a command-line based quiz application written in Python.
It allows users to play quizzes, choose categories, and even create their own custom quiz sets.

🚀 Features
Multiple predefined quiz categories
Interactive command-based interface
Score tracking system
Ability to add custom quizzes
Input-based navigation (start, help, options, exit, add-quiz)
🧠 How It Works
1. Question Sets

The program contains multiple quiz sets stored as dictionaries:

Each question has:

4 options
1 correct answer (stored as index)

Example structure:

{
  "question": ["option1", "option2", "option3", "option4", correct_index]
}

All question sets are stored inside:

question_sets = [que_set1, que_set2, que_set3, que_set4]
2. Main Loop

The program runs inside a loop waiting for user commands:

>>> help
>>> start
>>> options
>>> add-quiz
>>> exit
📋 Available Commands
🔹 help

Displays instructions for using the application.

🔹 options

Allows user to select a quiz category:

1 → MYTHOLOGY  
2 → GK  
3 → HISTORY  
4 → COMPUTER  

The selected option determines which question set will be used.

🔹 start

Starts the quiz for the selected category.

Flow:

Each question is displayed
Options are printed (1–4)
User enters an answer
Answer is checked
Score is updated

At the end:

You scored X/5
🔹 add-quiz

Allows the user to create a custom quiz.

Steps:

Enter quiz title
Add 5 questions
For each question:
Enter 4 options
Enter correct answer (1–4)

The new quiz is stored and added to question_sets.

🔹 exit

Ends the program immediately.

🧮 Answer Handling
User inputs answers as numbers (1–4)
Internally converted to index format (0–3)
Compared with stored correct answer
🔁 Program Flow Summary
Program starts
Waits for user command
Based on command:
Shows help
Selects category
Starts quiz
Adds new quiz
Exits
Loop continues until user exits
📌 Entry Point
if __name__ == "__main__":
    main()

This ensures the program runs only when executed directly.

🛠️ Requirements
Python 3.x
Terminal / Command Prompt
▶️ How to Run
python your_file_name.py