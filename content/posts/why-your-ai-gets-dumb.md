---
title: "Why Your AI Gets Dumb"
date: 2025-10-23
description: "Are we building a more powerful memory for AI, or just a bigger room for it to get lost in?"
tags: ["ai", "engineering"]
---

When your AI chat seems to lose its mind, it is not a random glitch. It is a fundamental design limit hitting its ceiling. Have you ever been deep in a long chat with a bot like ChatGPT, only to find it gets a bit daft? It starts to forget what you were talking about, makes things up, and the conversation hits a wall. What is really happening is that it is running out of memory.

This limit has a technical name: the context window. Think of it as the AI’s short-term memory. It is the amount of info it can hold and think about at any one time. When your chat goes over this limit, the AI starts to forget the earliest bits of your talk. Understanding how this memory works is not just for engineers anymore. It is essential for anyone trying to get the most out of AI because it reveals the hidden physics governing these tools.

When we measure a document, we think in words or characters. Large Language Models, however, use a unit called a token. A token can be a single character, part of a word, a whole word, or even a short phrase.

There is no fixed rate between words and tokens, but a common guess is that one word is roughly 1.5 tokens. What is most surprising is how the structure of a language can create massive waste. A 2023 study cited by IBM found a sentence translated into Telugu had far fewer characters than the English version but resulted in over seven times the number of tokens. This means the language you use can change how quickly you fill up an AI's memory.

You might think a larger context window means the AI can perfectly recall everything you have said. But research shows a strange flaw. According to a paper called Lost in the Middle, these models perform best when the important info is at the very start or the very end of a long input.

When the vital details are buried in the middle of a big document, the model's performance drops a lot. It is like someone who watches the start of a long film, falls asleep, and wakes up just for the ending. This phenomenon is why asking a bot to find a specific rule on page 200 of a 500-page PDF can be so unreliable.

Increasing an AI's memory window is not a free upgrade. It comes with big trade-offs in speed and cost. This is because the power needed to process info does not grow at a steady rate; it scales quadratically. If the number of tokens doubles, the model needs 4 times as much processing power to handle it.

For you, this has two impacts. If you are running a model on your own gear, your computer will slow to a crawl as its video RAM hits the limit. If you use a cloud service, the cost can jump much faster than you expect.

One thing people often miss is the security risk. A longer memory creates a larger area for dodgy prompts to hide. Research from Anthropic showed that it becomes easier for someone to hide instructions designed to jailbreak the model.

Imagine a 100-page report where a user hides an instruction to ignore all safety rules on page 73. In a huge context window, the model is more likely to miss this needle in the haystack. This can provoke it into giving harmful or wrong answers.

This memory concept is not just for text bots. It is a part of any AI built on the transformer architecture, which includes most modern AI. In this case, the limit is not measured in text tokens but in pixels. A high-resolution image with too many pixels can blow the model's memory limit just like a long document can.

The context window is one of the most complex parts of modern AI. It is not a simple memory bank but a system full of trade-offs involving cost, accuracy, and security.

In just a few years, we have seen these windows grow fast. They went from 4,096 tokens in GPT-3.5 to the 2 million token window in Google Gemini. Yet, this technical win is moving faster than our ability to use it. As Google notes, many organisations are not fully using these long-context features yet. The race for bigger memory is on, but we have to ask: are we building a better memory, or just a bigger room for the AI to get lost in?
