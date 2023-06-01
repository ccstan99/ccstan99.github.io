---
layout: post
title: "Demystifying ChatGPT + LLMs"
subtitle: "Overview of Language Models"
background: '/img/posts/2023-05-24-llms.jpg'
---

Welcome to the world of ChatGPT and LLMs filled with alphabet soup jargon. We'll look at language models, how they got so large, and think about how to deal with all this AI buzz.

## Background in Natural Language Processing (NLP)

Language models live in the field of natural language processing, The ultimate dream, the holy grail, is to talk with computers just like talking with any other person and have it completely understand you. No need to learn computer languages. They can speak ours. Originally, linguists would painstakingly create "expert" systems, hand-coding  grammar rules and all the vocabulary. Unfortunately, the end results were mediocre, at best.

![Statistics in LLMs](/img/posts/2023-05-24-llms-stats.png)

Towards the late 90s, statistical methods were used. There's a famous quote, "You shall know a word by the company it keeps." That simple idea was profound. If you start counting words and looking at what other words tend to occur with it, you'll end up learning a lot about the language itself. All those relationships make up the language model. Think back to when you were first learning your native language. As a child, you were immersed with sounds, words, and sentences of your language. Now, you have intuition of what sounds right or what's off, even if you don't know why. You've internalized all the statistics for your own language model.

## Rise of Transformers

Transformers are a special kind of neural network introduced by Google in 2017.

Before that, language models were painfully slow and forgetful. Imagine a sweet old granny struggling to understand words one by one and getting confused by long sentences. So, if you had tried to make models bigger, trained on more data, it didn't matter.

![Transformers are Superheroes](/img/posts/2023-05-24-llms-superhero.png)

Things didn't really improve much until Transformers came along with attention superpowers. Now, models could look at everything, all at once. Long-term memory? No problem. Now, we can train on all of Wikipedia and piles and piles of books. The models kept learning and improving. Turns out, neural networks are extremely data hungry. They need tons of it to learn. So people went out and scraped everything they could find on the web: blogs, tweets, code, whatever was out there.

Another innovation: Transformers could process data in parallel. Otherwise, it's like one checkout stand serving 100 customers one at a time, sequentially. Instead, Transformers use 100 checkout stands to serve all 100 customers at the same time in parallel. So models got bigger, running faster, training longer on more data, and performance kept getting better!

Thus began the rise of large language models. Size is measured by the number of parameters or neurons. Today, to be large, a language model must have at least 1 billion neurons. They're not the same, but for reference, the human brain has around 85 billion. And all the large language models today are some variant of Transformers, which completely revolutionized AI beyond just language!

## Generative pre-trained transformers (GPT)

Generative pre-trained transformers or GPT shine at generating text.

They are trained for next word prediction. It's like a play the game. You grab a book, pick a sentence, and show the model the beginning of the sentence. It tries to guess the next word in the sentence. You show it the actual next word. Hmm, if it's wrong, let's update the neurons to do better the next time. Pick another sentence. Guess another word and update. Then repeat until the model gets really good at guessing the next words. Starting with "Twinkle Twinkle Little..." the next word is most likely "Star." Maybe feels like a sophisticated auto-complete. Think about when you're talking with someone and you "complete each other's sentences." It's often a sign of deep mutual understanding. Imagine a computer doing the same.

![Pre-Training LLMs](/img/posts/2023-05-24-llms-training.jpg)

When it comes to P in Pre-training we need to look to the past. A variety of different models would be trained as specialists: one for answering questions, another for classifying things, or for translation. But GPT is a generalist, pre-trained to understand human languages in general, which can be quickly fine-tuned on top of the pre-trained base.

GPT was created by OpenAI. The original, GPT-1, was introduced in 2018, jumping in after Google's transformers. The next year, GPT-2 was 10 times larger. The year after that, GPT-3 was 100 times larger. By then, it was almost impossible to tell what's generated and what's not. As for GPT-4 that just came out? It's a secret. Keep in mind, these models are huge. It costs millions of dollars to train on a slew of computers over a period of months. It's not feasible for individuals or even academic researchers to train anything like this. You need those deep pockets.

## ChatGPT

Then along came ChatGPT. Frankly, many working in the field were baffled, "Why is this going viral now? It's just GPT-3.5, with minor tweaks to the base model released three years ago!"

The secret sauce was reinforcement learning from human feedback. Remember, GPT was trained to predict the next word given the start of a sentence. That's great for learning the language, but really, that's not as helpful for the typical end user. When you talk to people, you rarely begin a sentence and then expect them to complete it. Instead, you're more likely to tell them to do something or maybe ask a question.

So GPT-3 was fine-tuned to respond to instructions. They got lots of sample instructions along with what's expected. If you see "Prepare a report," the output should indicate what a report looks like. For "Give me a summary," the output should indicate what a summary looks like.

![ChatGPT was Fine-tuned on Instructions](/img/posts/2023-05-24-llms-instruct.jpg)

Next, it was also fine-tuned on sample back-and-forth conversations to learn how dialogues work. These extra fine-tuning steps were quick and cheap compared to pre-training the original, which took months and millions. It managed to bring out some innate abilities hidden in the base model. But suddenly, following instructions and carrying conversations made it extremely helpful and eerily "human."

## On the Horizon

That us up to late last year. Now, things are moving even faster since then. Let me point out a few items on the horizon to keep an eye on.

Multi-modality
: Language models deal mainly with text. Multi-modality allows them to use audio, images, and videos to understand the world. And the better to see you, to hear you, and to interact with you.

Open-Source
: Just a few weeks ago, Meta released an open-sourced large language model that can run on personal computers. That led to a flurry of activity. Researchers are now creating much smaller and cheaper models that are still powerful.

Agents
: Language models can generate text for a plan. Now, they can also call agents, which are programs to execute that plan. "Plan a trip to Tokyo." It goes to compare prices, book flights, find lodging. You just show up and enjoy. But if AI automatically connects to agents that can change things in the real world with consequences, we must stop and think, "What could possibly go wrong?!"

## Hype or Reality?

Is this all hype? Or is the world really changing? I started working in tech during the dot-com era. The gold rush euphoria feels suspiciously familiar. But there's definitely a fundamental paradigm shift that's both thrilling but a tad worrying.

Personally, I use large language models every day. They're great for mundane tasks like proofreading documents, drafting emails, or generating code snippets. Search is really handy. Information is synthesized and summarized for your specific case. But I only use AI as a tool to speed up my normal workflow. I still double-check the output since it's not all sunshine and rainbows.

You must understand the limitations. Hallucinations are a big problem. That's a technical term when the output is just flat out wrong but sounds really convincing and confident. A dangerous combination. Essentially, AI is a master B.S.er, but plenty of humans are too. It's just regurgitating what's learned from its training data, which includes lots of toxic and biased stuff too. So what's the key takeaway?

## Conclusion

We're standing at the dawn of this new era shaped by AI. In order to survive, you'll have to embrace AI in some way. No one wants to be the dinosaur. Sometimes, it feels like we're blindly rushing into this awe-inspiring yet potentially treacherous territory. AI is a tool that holds immense power, but it's far from perfect or even safe. As the saying goes, "Trust but verify." We need to keep humans in the loop. My hope is that we can be guided by wisdom, empathy, and a commitment to embrace the power of AI responsibly.

![Embrace AI Responsibly](/img/posts/2023-05-24-llms-embrace.png)
