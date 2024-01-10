import random
from datetime import datetime

def get_time():
    current_time = datetime.now().strftime("%A, %d %B %Y %H:%M:%S")
    return current_time

def get_weather():
    # In a real-world scenario, you would integrate with a weather API to get accurate information.
    # For simplicity, let's assume the weather is always sunny.
    return "The weather is sunny and pleasant."

def chat():
    user_input = input("You: ").lower()

    if "hello" in user_input or "hi" in user_input:
        print("Bot: Hi there! How can I assist you today?")
    elif "how are you" in user_input:
        print("Bot: I'm just a computer program, but thanks for asking!")
    elif "tell me a joke" in user_input:
        jokes = ["Why don't scientists trust atoms? Because they make up everything!", "What do you call fake spaghetti? An impasta!"]
        print(f"Bot: {random.choice(jokes)}")
    elif "time" in user_input:
        current_time = get_time()
        print(f"Bot: The current time is {current_time}.")
    elif "weather" in user_input:
        weather_info = get_weather()
        print(f"Bot: {weather_info}")
    elif "help" in user_input:
        print("Bot: Available commands:")
        print("* Greetings: Responds to greetings like 'hello' or 'hi'.")
        print("* How are you: Inquires about the bot's well-being.")
        print("* Tell me a joke: Shares a random joke.")
        print("* Time: Provides the current date and time.")
        print("* Weather: Shares information about the weather (simulated).")
        print("* Bye: Ends the conversation.")
    elif "bye" in user_input:
        print("Bot: Goodbye! Have a great day!")
        return
    else:
        print("Bot: I'm sorry, I didn't understand that. Could you please ask something else?")

    chat()

chat()  
