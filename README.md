# AlgoRhythmKPB
import datetime
import random

# Study tips list
study_tips = [
    "Take regular breaks every 25–30 minutes.",
    "Use the Pomodoro Technique to stay focused.",
    "Summarize what you study in your own words.",
    "Teach what you’ve learned to someone else.",
    "Use flashcards for quick revision."
]

# Motivational quotes list
motivation_quotes = [
    "Believe in yourself and all that you are!",
    "Hard work beats talent when talent doesn’t work hard.",
    "Push yourself, because no one else is going to do it for you.",
    "Dream it. Wish it. Do it.",
    "Don’t watch the clock; do what it does. Keep going!"
]

# Main chatbot loop
def study_mate_chatbot():
    print("👋 Hi! I'm your Study Mate. Ask me anything or type 'exit' to quit.\n")

    while True:
        user_input = input("You: ").lower()

        if user_input == "exit":
            print("Study Mate: Goodbye! Keep learning! 💡")
            break

        elif "time" in user_input:
            now = datetime.datetime.now()
            print("Study Mate: Current time is", now.strftime("%I:%M %p"))

        elif "date" in user_input:
            today = datetime.date.today()
            print("Study Mate: Today's date is", today.strftime("%B %d, %Y"))

        elif "tip" in user_input or "study" in user_input:
            print("Study Mate (📘 Tip):", random.choice(study_tips))

        elif "motivate" in user_input or "quote" in user_input:
            print("Study Mate (💬 Quote):", random.choice(motivation_quotes))

        elif "who are you" in user_input:
            print("Study Mate: I'm your friendly study assistant. I'm here to help you stay focused!")

        else:
            print("Study Mate: Hmm, I didn't understand that. Try asking for a tip, time, or quote.")

# Run the chatbot
study_mate_chatbot()
