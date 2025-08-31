---
title: "A Short History of AI - How it began and why it exploded"
date: 2024-08-31T12:00:00+05:30
draft: false
author: "Shashi"
categories: ["AI"]
tags: ["AI","deep-learning"]
description: "My notes on how AI started from Turing’s imitation game to symbolic AI, ELIZA, neural networks, ImageNet/AlexNet, GANs and Transformers and why compute & data changed everything."
---

I read a bunch of old papers and remembered fragments of the story, Turing’s imitation game, McCarthy’s Dartmouth proposal, ELIZA’s keyword tricks — and wanted to collect a readable timeline so my future self can quickly recall how AI evolved. Below I put the history in plain words, added technical notes where it helps, and suggested why each era mattered to what we see today.

<!--more-->

# Turing and the imitation game: the first "can machines think?"

The AI story often starts with Alan Turing. In 1950 he asked a practical reframing of “Can machines think?” in his paper Computing Machinery and Intelligence, and he described the thought experiment we now call the Turing Test or the “imitation game.” In that setup an interrogator asks questions (via text) to two hidden players — a human and a machine — and tries to tell which is which. If the machine can consistently fool the interrogator, Turing argued, we should be comfortable saying it “behaves like” thinking. 

Turing wasn’t saying machines are people. He offered a behavioral test: if the answers are indistinguishable, calling it “thinking” is a reasonable linguistic move. At the time (1950) this was mostly conceptual — real hardware and software were nowhere near powerful enough to implement human-like conversation or reasoning.

## Dartmouth and John McCarthy - the formal birth of “AI”

A few years later (summer 1956) John McCarthy organized a small workshop at Dartmouth that is usually credited as the official founding event of the field called artificial intelligence. McCarthy proposed that aspects of learning and intelligence could, in principle, be precisely described and simulated by machines — that was the rallying idea. He also developed Lisp (a language well-suited to symbolic processing) and helped push the symbolic approach to the foreground. 

McCarthy and colleagues focused on symbolic AI — representing knowledge with symbols and rules (if–then logic) and writing programs that manipulated those symbols via explicit logic. People sometimes call this era GOFAI (Good Old-Fashioned AI).

### Quick timeline



## Symbolic AI: rules, symbols, and the limits

Symbolic AI felt powerful because it matched how we write programs: we give the machine symbols (concepts), rules (logic), and inference procedures. Early systems showed surprising results on narrow tasks (planning, theorem proving, simple natural-language programs) but revealed a core fragility: if the system lacked some piece of world knowledge or a rule you hadn’t encoded, it simply failed. These systems didn’t “learn” the way humans do — they relied on handcrafted knowledge and brittle logic.

Over time, people realized purely symbolic systems had huge scaling problems: writing all the required rules and world knowledge by hand is infeasible for the messy, ambiguous real world. That contributed to the first cycles of hype and disappointment (the early "AI winters") when expectations outran practical results.

## ELIZA and the cunning of simple tricks

One famous early demo was ELIZA (1966), a program by Joseph Weizenbaum that simulated a psychotherapist. ELIZA didn’t understand anything — it matched keywords and used scripted reply templates — but users often anthropomorphized it and attributed understanding. ELIZA showed two things: simple pattern-matching could appear conversational, and humans are quick to project intelligence onto interactive systems. 

ELIZA is a useful reminder: sometimes “looks like intelligence” is enough for people to react emotionally, even if the underlying system is just pattern rewriting.

## The symbolic lull and the "AI winters"

Because early systems needed huge amounts of hand-coded knowledge and because hardware/compute was limited, funding and expectations repeatedly fell. These slowdowns (commonly called AI winters) happened when lab results didn’t match bold promises. Still, the core concepts from symbolic AI and early research persisted and informed later work.

## The neural-network re-awakening — Hinton and the “learn from data” approach

Not everyone liked the symbolic way. Some researchers imagined systems that learn from examples, loosely inspired by the brain. Geoffrey Hinton was a central figure here: he helped popularize using backpropagation to train multi-layer neural networks (a crucial idea for modern deep learning), and he later worked on many deep-learning innovations. Instead of hand-coded rules, neural networks learn patterns from large datasets. Hinton and collaborators helped make that approach practical and influential. 

The intuition is simple: give a network lots of examples and an algorithm to change internal parameters (weights) to reduce error — eventually the network discovers useful features without explicit rules.

## Why data + compute mattered: ImageNet and AlexNet

Two practical pieces came together that changed everything: 

- large labeled datasets
- enough compute (GPUs, more transistors per chip). 

Fei-Fei Li’s ImageNet project built a massive, labeled image database, collected (in part) via Amazon Mechanical Turk — millions of images across thousands of categories — which made it possible to train large vision models. 

In 2012 the AlexNet model (Krizhevsky, Sutskever, Hinton) used deep convolutional neural networks trained on ImageNet and achieved dramatically better image classification results than previous methods. AlexNet’s success demonstrated that large networks + lots of data + GPUs could produce huge practical gains — what many call the start of the modern deep learning boom.

## GANs: generating data that looks real

In 2014 Ian Goodfellow introduced Generative Adversarial Networks (GANs) — two neural networks (generator and discriminator) trained in opposition so the generator learns to make data indistinguishable from real examples. GANs unlocked high-quality image synthesis and many creative applications. That adversarial training idea became a powerful tool for generative modeling.

## Transformers and the LLM era



Sequence models used to be dominated by RNNs and LSTMs, which processed sequences step-by-step and could struggle with very long-range dependencies. In 2017 the Transformer architecture (Attention Is All You Need) replaced recurrence with self-attention: the model looks at the whole sequence at once and learns which parts should attend to which other parts. Transformers are highly parallelizable and scale well — they are the backbone of modern large language models (LLMs) and foundation models. 

Because Transformers scale well with data and compute, they enabled huge pre-trained models that can be fine-tuned for many tasks — essentially changing how we build and deploy AI systems.

## Moore’s law, GPUs, and why compute exploded

All this progress required better hardware: exponentially more transistors on chips (Moore’s Law) and the availability of GPUs optimized for parallel workloads made training large neural nets practical. Moore’s Law (the observation that transistor density has roughly doubled every couple of years since the 1960s) and GPU-driven acceleration together fuelled the era where large-scale training is financially and technically feasible. Without those compute gains, many modern breakthroughs (AlexNet, big Transformers) wouldn’t have been practical.

## Symbolic vs neural — two cultures that sometimes meet

To sum up the technical divide:

- Symbolic / GOFAI: human-readable rules, explicit logic, brittle when rules are missing. Good for reasoning that needs interpretable steps.

- Neural / statistical: learns representations from data, robust in many perceptual tasks, hard to inspect. Good for pattern recognition and generation.

Modern AI often mixes them: neural nets for perception+learning, symbolic methods for explicit reasoning, or hybrid approaches that attempt to get the best of both.

## Why this history matters for me (and you)

When I read these papers I see a clear pattern:

- Ideas start what becomes a field (Turing’s thought experiment; McCarthy’s Dartmouth). 

- Proof-of-concept demos (ELIZA, SHRDLU, early planners) show potential and set expectations. 

- Practical scaling (data, compute, engineering) turns potential into industry-changing reality (ImageNet, AlexNet, Transformers). 

If you want to build or experiment, learn both modes: how symbolic logic is specified and how statistical models are trained. Each style teaches different intuition about intelligence.
