# GenAI

 Status:  Work in Progress (2025-08-01)
Purpose:  exploring code assistants and chat clients

Primarily exploring:

* Amazon Bedrock (for Nova and Claude access)
* Anthropic Claude / Claude Code (possibly API based subscription)
* Perplexity.AI (WebUI and CLI)
* Using both CLI and VS Code

I use perplexity.ai for "general search or guidance" - essentially for things that I could have found with a Google Search.  I have a pro subscription.


# Retrieve a modelId and the configure chat-cli to use it by default
```bash
aws bedrock list-foundation-models --query 'modelSummaries[*].[modelArn, modelId, modelName]' --output text | grep novak
chat-cli config set model-id amazon.nova-lite-v1:0
```

# Test a query
```
glados:~ jradtke$ chat-cli config set model-id amazon.nova-lite-v1:0
Configuration set: model-id = amazon.nova-lite-v1:0
glados:~ jradtke$ chat-cli prompt "what is the distance between the Sun and the Earth?"
The distance between the Sun and the Earth is not constant due to the elliptical shape of Earth's orbit. However, the average distance, often referred to as 1 Astronomical Unit (AU), is approximately 93 million miles (about 150 million kilometers).

To provide more detail:
- The closest approach, called perihelion, occurs around early January and is about 91.4 million miles (147.1 million kilometers).
- The farthest distance, called aphelion, occurs around early July and is about 94.5 million miles (152.1 million kilometers).

These variations are due to the elliptical orbit of the Earth around the Sun.
```

ProTip:  While I figured out how to query the AWS billing API, I am not going to explain it here and will not be using it.  There is a per-use charge to run the queries (I'll mention this to Corey Quinn the next time I see him as it is pretty dumb that they do this)

# Amazon Bedrock Chat CLI client (created by old coworkers and I contributed to)
https://github.com/chat-cli/chat-cli

# Perplexity.AI CLI client (created by me)
https://github.com/cloudxabide/perplexity-cli

# Amazon Q CLI

# Anthropic Claude Code

# Visual Studio Code - VS Code
