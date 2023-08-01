# Discord AI Chatbot

This is a simple Discord chatbot that uses OpenAI's GPT-3.5-turbo model to answer text inquiries. Here is a simple README on how to use it.

## Setup

1. First, clone the repository to your local environment.

2. Install the necessary dependencies: `discord.py`, `openai`, and `python-dotenv`. You can do so by running:
    ```
    pip install discord.py openai python-dotenv
    ```
3. Setup your .env file in the root of your project directory and replace the placeholders with your actual OpenAI API key and Discord Bot token. The .env file should look something like this:

    ```
    openai_api_key=YOUR_OPENAI_API_KEY
    discord_bot_token=YOUR_DISCORD_BOT_TOKEN
    ```
4. Replace `"YOUR DISCORD BOT TOKEN"` in the `client.run()` function at the bottom of your Discordbot.py file with your actual Discord bot token, or change it to `discord_bot_token` to use the variable you defined in the .env file.

    ```python
    client.run(discord_bot_token)
    ```

## How to run

Once you've setup everything correctly, you can start the bot by running:
  ```python Discordbot.py```

## How it works

The bot will listen to every message in every channel it has access to. If the bot is mentioned in a message, it will take the rest of the message as input and use it to generate a response using OpenAI's GPT-3.5-turbo model.

This behavior can be modified in the `on_message` function of `Discordbot.py`.

The bot's "personality" can be modified by changing the content of the `"system"` role message in the `openai.ChatCompletion.create` call. For example, you might have the bot introduce itself as an all-knowing oracle, a friendly helper, or anything else you can think of.

## Disclaimer

Please be aware that this bot doesn't have any command or message filtering. It will respond to any message where it is mentioned. Be careful where you deploy this bot and who has access to it. Also, the responses from the GPT-3 model are generated and not reviewed, so inappropriate content may be generated.

## License

This project is licensed under the MIT License.

