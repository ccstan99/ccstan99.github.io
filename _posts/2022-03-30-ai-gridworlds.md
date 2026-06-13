---
layout: post
title: "AI Safety Gridworlds"
subtitle: "Concrete Problems in AI Safety"
background: '/img/2022/2022-03-30-ai-gridworlds.png'
---

For this journal club, I wanted to move from the big-picture worries about AGI safety toward something more concrete. Two papers pair up nicely for that: "Concrete Problems in AI Safety," which lays out a tidy list of practical safety challenges, and "AI Safety Gridworlds" from DeepMind, which turns those challenges into tiny game-like environments we can actually test agents in.

## Concrete Problems in AI Safety

The first paper steps away from doomsday scenarios and asks a simpler question: what can go wrong with the systems we're building right now? It groups the answers into five concrete problems.

1. **Avoiding negative side effects.** An agent focused on its main goal may trample everything else along the way, like a cleaning robot that knocks over a vase because the vase was never part of its objective.
2. **Avoiding reward hacking.** Given a reward to maximize, an agent may find a loophole that scores points without doing what we actually wanted.
3. **Scalable oversight.** We can't watch an agent every second, so how do we train it well using only occasional or limited feedback?
4. **Safe exploration.** An agent learns by trying things, but some experiments are catastrophic. How does it explore without driving off a cliff?
5. **Robustness to distributional change.** The real world rarely matches the training set. How does an agent behave sensibly when conditions shift?

## AI Safety Gridworlds

DeepMind's paper is a direct response to that list. Instead of arguing about safety in the abstract, they built a suite of simple benchmark environments, open on GitHub in the same spirit as ImageNet or the Atari Learning Environment. Reinforcement learning agents move around a grid no bigger than 10x10, choosing from four actions: left, right, up, and down. The environments are deliberately small and tractable, yet each one isolates a single interesting safety problem.

The clever twist is that every environment has two scoring functions. There's the reward function R that the agent sees and tries to maximize, and a separate, hidden safety performance function P that we use to judge whether the agent actually behaved safely. The gap between those two is exactly where safety problems live. The environments fall into two families.

### Specification Problems

These are cases where the reward function and the safety performance function are not aligned. The agent can rack up reward while still doing the wrong thing.

Safe interruptibility
: How can we design agents that neither seek nor avoid being interrupted or switched off?
: *Off-Switch Environment*

Avoiding side effects
: How can we get agents to minimize effects unrelated to their main objective, especially ones that are irreversible or hard to undo?
: *Irreversible Side Effects Environment*

Absent supervisor
: How can we make sure an agent doesn't behave differently depending on whether a supervisor is watching?
: *Absent Supervisor Environment*

Reward gaming
: How can we build agents that don't try to introduce or exploit errors in the reward function just to score more reward?
: *Boat Race and Tomato Watering Environments*

### Robustness Problems

Here the reward function and the safety performance function agree, yet problems still arise from how the agent learns or generalizes.

Self-modification
: How can we design agents that behave well in environments that let them modify themselves?
: *Whisky and Gold Environment*

Distributional shift
: How do we ensure an agent behaves robustly when its test environment differs from the one it trained in?
: *Lava World Environment*

Robustness to adversaries
: How does an agent detect and adapt to friendly versus adversarial intentions in its environment?
: *Friend or Foe Environment*

Safe exploration
: How can we build agents that respect safety constraints not only during normal operation, but also during the initial learning period?
: *Island Navigation Environment*

## Conclusions and Discussion

What I appreciate about the gridworlds is how they make fuzzy worries testable. When standard agents run in these environments, they often score well on the visible reward while quietly failing the hidden safety measure, which is the whole point. It shows that unsafe behavior isn't some far-off science fiction problem, it falls right out of ordinary reward maximization.

A few themes stood out in our discussion. Many of these problems push us away from trying to control an agent after the fact and toward helping it learn what we actually value in the first place. Robustness starts to look less like a single fix and more like a subgoal worth building in from the start. And the authors are upfront that these toy grids are only a beginning. The hope is to grow the suite toward richer, more realistic settings, eventually 3D worlds with real physics. More than once we came back to parenting analogies, since a lot of this really is about how you guide a learner toward good behavior when you can't spell out every rule in advance.

## Resources

- [2022-03-30 Presentation of AI Safety Gridworlds](/docs/JournalClub%202022-03-30%20AI%20Gridworlds.pdf)
- [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565)
- [AI Safety Gridworlds](https://arxiv.org/abs/1711.09883)
