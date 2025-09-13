# A Discord Chatbot

A Simple Discord chatbot that connects to a local LLM.

## Prerequisites

* You have set up a Discord bot account. If you are not sure, check [Discord Development Resource](https://discord.com/developers/docs/intro) and go through the necessary steps to [set up a bot account](https://discordpy.readthedocs.io/en/stable/discord.html).
* You have obtained a working Discord token and have the bot account joined a default Discord Guild/Channel.

## Configure Lurawi Discord bot

1. `git clone https://github.com/kunle12/lurawi.git`[1].

1. Copy files under this directory into the `lurawi` directory.

1. Update [`discord_bot_knowledge.json`](discord_bot_knowledge.json) with the Discord bot account access token, setting up its default guild and channel. Map your the discord users who can interact with the bot.

1. Update `invoke_llm` custom in the workflow to point to your LLM provider(s).

1. Set up the environment variables:  

```bash
export PROJECT_NAME=discord_bot
export PROJECT_ACCESS_KEY=can_be_anything
```

6. Run `bin/lurawi run`

**NOTE**  
[1] To deploy this discord bot into a cloud environment, you should modify [`Dockerfile.new`](https://github.com/kunle12/lurawi/blob/main/Dockerfile.new) file to build a dedicate docker image for the bot.

[2] The current workflow uses one LLM for general QnA bot and one VLM if a Discord message contains (one) image attachment.
