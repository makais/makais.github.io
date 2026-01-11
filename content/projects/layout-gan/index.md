---
title: "LayoutGAN Prototype"
description: "AI for sketch-based generative design of floor plans"
categories: ["project"]
weight: 120
tags: ["generative design", "AI", "prototype", "human-in-loop", "product management", "2022"]
cover:
    image: "layout-gan-cover.jpg"
    alt: "diagram of AI floor plans"
    relative: true
---

A model trained on residential floor plans was used to create a sketch-based application for automatically drawing floor plans from building outlines.  Program indicated by color, and the user could specify locations for doors and windows.  The sketch app also had simple orthogonal and snap functionality.  The model created plans in real-time while the user was drawing to give immediate feedback. It was then fed into models used to identify structural elements for downstream use in a building systems design prototype that used the [Concetto](/projects/concetto) platform. I was product manager for Glodon USA, originated the concept, gathered reference research such as House-GAN, and directed the AI research project.

{{<figure src="layout-gan-screenshot.jpg" alt="Screenshot of LayoutGAN interface showing sketch and generated floor plan in Concetto." title="Automated floor plan generation" caption="Vectorization of generated spaces was nontrivial, as shown by the inconsistent results at the boundaries between spaces in this work-in-progress screenshot. Image: © Glodon USA Software.">}}