# Quiz Game

This repository contains a simple quiz game implemented in Python. The quiz consists of multiple questions, each with a `True` or `False` answer. The user is prompted to answer each question, and their score is displayed at the end of the quiz.

## Project Structure

- `question_model.py`: Contains the `Question` class.
- `data.py`: Contains the list of questions (`question_data`).
- `quiz_brain.py`: Contains the `QuizBrain` class which manages the quiz logic.
- `main.py`: The main script that runs the quiz game.

## Classes

### Question
A class to represent a single question.

#### Attributes:
- `text`: The text of the question.
- `answer`: The correct answer to the question.

#### Methods:
- `__init__(self, q_text, q_answer)`: Initializes the question with the provided text and answer.

### QuizBrain
A class to control the flow of the quiz.

#### Attributes:
- `question_number`: The current question number.
- `question_list`: A list of all the questions.
- `score`: The user's current score.

#### Methods:
- `__init__(self, q_list)`: Initializes the quiz with a list of questions.
- `still_has_question(self)`: Checks if there are more questions in the quiz.
- `next_question(self)`: Prompts the user for an answer to the current question and checks if it's correct.
- `check_answer(self, user_answer, correct_answer)`: Checks the user's answer and updates the score.

## Usage

1. Ensure you have Python installed on your system.
2. Clone this repository.
3. Navigate to the repository directory.
4. Run the main script:

```bash
python main.py
```

You will be prompted with a series of `True` or `False` questions. Enter your answer for each question and your score will be displayed at the end.

## Example Questions

The `data.py` file contains the following example questions:

```python
question_data = [
    {
        "category": "Science: Computers",
        "type": "boolean",
        "difficulty": "medium",
        "question": "The HTML5 standard was published in 2014.",
        "correct_answer": "True",
        "incorrect_answers": [
            "False"
        ]
    },
    {
        "category": "Science: Computers",
        "type": "boolean",
        "difficulty": "medium",
        "question": "The first computer bug was formed by faulty wires.",
        "correct_answer": "False",
        "incorrect_answers": [
            "True"
        ]
    },
    # More questions...
]
```

## License

This project is licensed under the MIT License.

## Contact

For any questions or suggestions, feel free to open an issue or contact me directly.
