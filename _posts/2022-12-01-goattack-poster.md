---
layout: post
title: "Go Attack"
subtitle: "Adversarial Policies Beat Superhuman Go AIs"
background: '/img/posts/2022-12-01-goattack.jpg'
---

I am thrilled to share my recent experience helping FAR.AI creating the NeurIPS poster the paper ["Adversarial Policies Beat Superhuman Go AIs."](https://goattack.far.ai/)

## Research Overview

The project, fondly nicknamed "Go Attack", aimed to challenge the state-of-the-art Go-playing AI system KataGo. Researchers developed adversarial policies designed to play against KataGo. The adversarial policies achieved an astounding win rate of over 99% when KataGo used no tree search, and over 97% when it utilized enough search to be considered superhuman.

What's even more surprising is that the adversaries did not win by playing Go better than KataGo. In fact, they were easily beaten by human amateurs. Instead, the adversaries won by exploiting weaknesses in KataGo, tricking it into making serious blunders. This attack strategy transferred effortlessly to other superhuman Go-playing AIs, showcasing the surprising failure modes even in the most advanced AI systems.

## Reworked Figures

To better communicate the research findings, I reworked images from previous presentations and figures, particularly focusing on clarifying the **threat model** and the concept of **non-transitivity** where even amateurs players could beat a super-human adversary. Unexpected Result: If play were transitive, Human players would not beat Adversary! I added other visual cues by changing the clothing color and adjusting the direction of the cap, in response to a comment that characters looked like a cop and thug. Furthermore, I incorporated images generated from different Go board configurations to showcase various strategies we employed during testing.

| after | before |
| :---: | :----: |
| <img src="/img/posts/2022-12-01-goattack-model.svg" width="400px" /><br>Threat Model | <img src="/img/posts/2022-12-01-goattack-model-before.png" width="400px" /> |
| <img src="/img/posts/2022-12-01-goattack-nontransitivity.svg" width="400px" /><br>Non-Transitivity | <img src="/img/posts/2022-12-01-goattack-nontransitivity-before.png" width="400px" /> |

## NeurIPS Poster

The figures were crafted into narrative that summarized the research journey, highlighting the significant achievements and implications of the findings. In addition to creating the digital poster, I also designed a template for the organization that will be used for future conference presentations.

<img src="/img/posts/2022-12-01-goattack.png" width="100%" style="border:1px solid #eee; display: block; margin: 0 auto;" />

## Conclusion

Congrats to the team for winning a best paper award and an x-risk analysis award for the NeurIPS 2022 ML Safety Workshop! It was an honor to make a small contribution to the field of AI safety. Learn more about the project from the resources by visiting the [website](https://goattack.far.ai/), reading the [paper](https://arxiv.org/abs/2211.00241), or exploring the [code](https://github.com/AlignmentResearch/go_attack).
