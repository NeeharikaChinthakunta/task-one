# task-one: chatbot with rule based responses
import re
def simple_chatbot(user_input):
    # Define rules and responses
    rules_responses = {
        r'hello|hi|hey': 'Hello! How can I help you?',
        r'how are you': 'I am just a computer program, but I am functioning well. Thank you for asking!',
        r'bye|goodbye': 'Goodbye! Have a great day!'
    }
    # Search for a matching pattern and provide a response
    for pattern, response in rules_responses.items():
        if re.search(pattern, user_input, re.IGNORECASE):
            return response
    # If no match is found, provide a default response
    return "I'm sorry, I didn't understand that. Can you please rephrase?"
# Example usage
user_input = input("You: ")
response = simple_chatbot(user_input)
print("Chatbot:", response)
