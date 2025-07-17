# python-quiz-game
A Terminal Based Quiz Game Using Python
# quiz_game.py

def ask_question(question, options, correct_option):
    print("\n" + question)
    for key, value in options.items():
        print(f"{key}. {value}")
    
    answer = input("Your answer (A/B/C/D): ").strip().upper()
    
    if answer == correct_option:
        print("✅ Correct!\n")
        return 1
    else:
        print(f"❌ Wrong! Correct answer is {correct_option}. {options[correct_option]}\n")
        return 0

def main():
    print("🎉 Welcome to the Python Quiz Game!")
    print("Let's test your general knowledge.\n")

    score = 0
    total_questions = 3

    # Questions
    score += ask_question(
        "1. What is the capital of France?",
        {'A': 'Berlin', 'B': 'Madrid', 'C': 'Paris', 'D': 'Rome'},
        'C'
    )

    score += ask_question(
        "2. Who developed Python?",
        {'A': 'Elon Musk', 'B': 'Guido van Rossum', 'C': 'Bill Gates', 'D': 'Dennis Ritchie'},
        'B'
    )

    score += ask_question(
        "3. Which planet is known as the Red Planet?",
        {'A': 'Earth', 'B': 'Jupiter', 'C': 'Mars', 'D': 'Venus'},
        'C'
    )

    print(f"🎯 You got {score} out of {total_questions} correct!")

if __name__ == "__main__":
    main()
