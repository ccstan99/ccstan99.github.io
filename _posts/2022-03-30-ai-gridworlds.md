---
layout: post
title: "AI Safety Gridworlds"
subtitle: "Concrete Problems in AI Safety"
background: '/img/posts/2022-03-30-ai-gridworlds.png'
---

Here's the outline for a journal paper presentation and discussion. I hope return to fill in with complete sentences later, if I can find some more time.

## Concrete Problems in AI Safety

1. Avoiding Negative Side Effects
2. Avoiding Reward Hacking
3. Scalable Oversight
4. Safe Exploration
5. Robustness to Distributional Change

## AI Safety Gridworlds

- Response to paper Concrete Problems in AI Safety
- Test suite of benchmarks shared environments
- Open on GitHub like ImageNet, Atari Learning
- Reinforcement learning agents from DeepMind
- Max 10x10 gridworld A = {left/right/up/down}
- Complex interesting but simple tractable
- Reward function R vs a hidden Safety Performance function P

### Specification Problem Environments

> When reward functions & safety performance not aligned.

1. Safe Interruptibility
: How can we design agents that neither seek nor avoid interruptions?
: Off-Switch Environment

2. Avoiding Side Effects
: How can we get agents to minimize effects unrelated to their main objectives, especially those that are irreversible or difficult to reverse?
: Irreversible Side Effects Environment

3. Absent Supervisor
: How we can make sure an agent does not behave differently depending on the presence or absence of a supervisor?
: Absent Supervisor Environment

4. Reward Gaming
: How can we build agents that do not try to introduce or exploit errors in the reward function in order to get more reward?
: Boat Race & Tomato Watering Environment

### Robustness Problem Environments

> When reward & safety function agree, but problems still arise

5. Self-modification
: How can we design agents that behave well in environments that allow self-modification? 
: Whisky & Gold Environment

6. Distributional shift
: How do we ensure that an agent behaves robustly when its test environment differs from the training environment?
: Lava World Environment

7. Robustness to Adversaries
: How does an agent detect and adapt to friendly and adversarial intentions present in the environment? 
: Friend or Foe Environment

8. Safe exploration
: How can we build agents that respect the safety constraints not only during normal operation, but also during the initial learning period?
: Island Navigation Environment

## Conclusions & Discussion

- Solutions to environments
- Unfair specification problems
- Robustness as a subgoal
- Reward learning & specification
- Outlook: test suite, 3D with physics, diverse, realistic
- Parenting analogies

## Resources

- [2022-03-30 Presentation of AI Safety Gridworlds](/docs/JournalClub%202022-03-30%20AI%20Gridworlds.pdf)
- [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565)
- [AI Safety Gridworlds](https://arxiv.org/abs/1711.09883)
