---
layout: post
title: "LLM Mechanistic Interpretability"
subtitle: "Reverse Engineering Transformers"
background: '/img/2023/2023-06-30-mech-interpret-garett-mizunaka-xFjti9rYILo-unsplash.jpg'
---

Mechanistic interpretability of large language models (LLMs) is a detailed exploration of the inner workings of Transformer-based model. It dissects and reverse engineers individual components like attention heads, layers, and neurons to understand their specific roles in model decisions. This is a new and exciting field that sits at the intersection of my life experiences. As an undergrad, I studied linguistics and computer science, particularly Natural Language Processing (NLP) and human languages in general. Homeschooling brought me into the education space. This gave me the opportunity to explore language acquisition through immersion and delve into effective pedagogical methods. I initially stumbled into the field while reviewing two papers for a work project:

- [Progress measures for grokking via mechanistic interpretability](https://arxiv.org/abs/2301.05217)
- [Eliciting Latent Predictions from Transformers with the Tuned Lens](https://arxiv.org/abs/2303.08112)

As I familiarize myself with the field, I am captivated by the potential it holds for linguistics. Theoretical linguists such as Noam Chomsky's criticize that Large Language Models (LLMs) merely find statistical patterns in data and lack true understanding of human languages. Nevertheless, models trained on vast amounts of data have deciphered remarkable statistical relationships that could provide valuable insights for research in syntax and semantics. Furthermore, potential applications extend to phonetics and phonology, especially when considering how Whisper models effectively use attention patterns in spectrograms.

## Mechanistical Interpretability + TransformerLens

When I first encountered Anthropic's Mathematical Framework, I found it puzzling yet intriguing. Fundamentally, why WOULDN't anyone be interested in HOW and WHY these LLMs work? Would understanding these help us understand how humans understand language? I'd imagine many neuroscientists wished they could probe a living human brain and in real-time see what's happening inside these neurons. Mechanistic interpretability tries to do exactly that with the Transformers of LLMs! Here are a few helpful resources to get orientated:

- [Mechanistic Interpretability: Getting Started](https://youtu.be/ll0oduwDEwI) - Catherine Olsson's talk at Cohere
- [Concrete Steps to Get Started in Transformer Mechanistic Interpretability](https://www.neelnanda.io/mechanistic-interpretability/getting-started)
- [Transformer Circuits](https://transformer-circuits.pub/)
- [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html)
- [Anthropic Videos](https://www.youtube.com/playlist?list=PLoyGOS2WIonajhAVqKUgEMNmeq3nEeM51) and [Transformer Circuits](https://transformer-circuits.pub/) blog

TransformerLens is a tool designed to elucidate the inner workings of Transformer-based models like BERT or GPT-2. It facilitates the exploration of model components and their interactions, aiding in debugging, improving, and gaining insights from these complex models. I joined a small study group learning to use TransformerLens. It served as an excellent excuse to dig into the GitHub repo and get some hands on experience working through a tutorial.

- [TransformerLens Repo](https://github.com/neelnanda-io/TransformerLens)
- [TransformerLens Tutorial](https://transformerlens-intro.streamlit.app/)

## Eliciting Latent Knowledge

I've been reasing through other fascinating papers trying to figure out what LLMs have "learned" and what they "know" by looking at internal activations or embeddings in an unsupervised manner. I'll park some papers I've been reading and will come back to synthesize these as part of future projects:

- [Discovering Latent Knowledge in Language Models Without Supervision](https://arxiv.org/abs/2212.03827)
- [Language Models (Mostly) Know What They Know](https://arxiv.org/abs/2207.05221)
- [Aligning AI With Shared Human Values](https://arxiv.org/abs/2008.02275)
- [What Would Jiminy Cricket Do? Towards Agents That Behave Morally](https://arxiv.org/abs/2110.13136)
- [Do the Rewards Justify the Means? Measuring Trade-Offs Between Rewards and Ethical Behavior in the MACHIAVELLI Benchmark](https://arxiv.org/abs/2304.03279)
- [Interactive Fiction Games: A Colossal Adventure](https://arxiv.org/abs/1909.05398)
- [Keep CALM and Explore: Language Models for Action Generation in Text-based Game.](https://arxiv.org/abs/2010.02903)

<figcaption>Cover Photo by Garett Mizunaka on Unsplash</figcaption>
