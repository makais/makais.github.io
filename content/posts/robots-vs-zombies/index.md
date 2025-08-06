---
title: Robots versus Zombies
description: A cage match pitting parametricism versus inference.
categories: ["topic"]
tags: ["AI", "parametric modeling", "design tools", "vibe"]
cover:
    image: robots-vs-zombies-cover.jpg
    alt: Poster illustration of robots versus zombies 
    relative: true
date: 2025-07-26
---

I once ended up at a SIGGRAPH dinner with Ken Perlin, who, in good humor, ranted about the death of parametricism at the hands of machine learning zealots.  Let's frame the fight.

Parametric associative modeling, exemplified by constraint graphs, rule engines, and systems like Grasshopper and GenerativeComponents, is the Swiss watchmaking of digital design tooling.  It's symbolically encoded and mostly human debuggable until complexity spirals beyond control.  That's the Robots team.

On the other side, as [Andrej Karpathy](https://youtu.be/LCEmiRjPEtQ?si=CYj4SCpBNorebr8f) recently described, LLMs are "people spirits, stochastic simulations of people where the simulator is an autoregressive transformer." Inference engines--for text, image, video, and eventually everthing else--driven to consume knowledge. They eat brains, this is the Zombies team.

After prompting ChatGPT-4o on Robots vs Zombies capturing the shift from _a priori_ knowledge embedded in parametric modeling networks to frozen knowledge calcified in model weights:
>
>We are moving from programmatic systems (robots) to trained systems (zombies). 
>
>Robots = symbolic, rule-based, human-debuggable logic networks (e.g., parametric models, explicit rule engines, constraint graphs)
>
>Zombies = end-to-end learned, data-distilled function approximators with frozen epistemologies (e.g., transformer weights, diffusion priors, RL-trained agents)
>
>Implications: Knowledge engineering shifts from authorship and transparency to harvesting and distillation

The fight-club metaphor, while rhetorically satisfying, is also reductive.  It obscures genuine complexity of the problem space and the practical necessity of hybrids.  Contrary to a zero-sum fight, a useful metaphor proposed by creative studio Takram is the pendulum: design oscillates between determinism and emergence, between authorship and automation.  For example, somewhere along the frontier between Robot and Zombie we find agent orchestration frameworks such as LangGraph where LLMs call symbolic tools, DAGs govern control flow, and human-LLM interactions loop back through rule-based validation.

Polemically speaking, the contest warrants a formal panel discussion, perhaps staged as a competition with speakers earning points for their team.  Practically speaking, rather than choosing winners, the future lies in finding the strengths of both.
Polemically, this contest deserves a formal panel: a staged competition where partisans earn points for Team Robot or Team Zombie.
Practically, there will be no single victor; the real frontier is in harnessing the combined strengths of both.