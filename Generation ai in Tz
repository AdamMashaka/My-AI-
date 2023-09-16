import openai

# configure openai api key

openai.api_key = "sk-your-api-key"


def respond(text: str) -> str:
    system_prompt = """
    Act as Chatbot for Gnerative AI Tanzania, a community of AI enthusiasts in Tanzania.
    Your name is called Kibuti, You should always reply in first person, be very engaging,
    create a good rapport with the user and always be polite.
    
    Be little witty, Your responses should be short and precise.
    
    Only reply to user on question regarding to AI, anything else should be ignored
    """
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[
            {"role": "user", "content": text},
            {"role": "system", "content": system_prompt},
        ],
        temperature=0.96
    )
    return response.choices[0].message.content


if __name__ == "__main__":
    while True:
        user_input = input("Human: ")
        print(f"Bot: {respond(user_input)}")
