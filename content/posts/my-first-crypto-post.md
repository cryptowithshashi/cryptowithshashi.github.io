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

# Timeline: The Major Breakthroughs

## 1950: Turing's Question - "Can Machines Think?"

The beginning of AI started in the early 1950s when a guy called Alan Turing published "Computing Machinery and Intelligence." In this paper, he proposed an imitation game which is now called the Turing Test.

The test worked like this: imagine three separate rooms where people can't see each other. In one room is an interrogator (the judge), in another room is a human, and in the third room is a machine. The interrogator asks questions to both the human and machine through text only, and from their responses, the interrogator has to figure out which one is human and which one is machine. If the machine can consistently fool the interrogator into thinking it's human, then Turing argued we should be comfortable saying it "behaves like" it's thinking.

This was purely a conceptual idea, not a practical thing, because at that time computers were way harder to get, extremely costly, and nowhere near powerful enough to have human-like conversations.

This guy asked "can machines think?" which was really hard to define, right? Because as humans, we naturally think machines can't think like us. So what Turing did was brilliant - he rephrased the entire question itself. Instead of asking "Can machines think?" he asked "Can machines behave indistinguishably from thinking beings?"

Here the word "behave" plays a huge role because actually machines can't think like us, but what if we feed them enormous amounts of data and we make them behave like they know everything? This might sound good, right? Turing wasn't saying machines are people or have consciousness - he was offering a practical behavioral test for intelligence.

This reframed the entire question about machine intelligence from philosophical speculation into something testable and measurable. It gave researchers a concrete goal to work toward.

This was more conceptual than practical at the time, but it established the fundamental question that still drives AI research today: not whether machines can truly think, but whether they can behave in ways that are indistinguishable from thinking.

## 1956: Dartmouth Workshop - AI Gets Its Name

In the summer of 1956, John McCarthy organized a small workshop at Dartmouth College that became the official founding event of artificial intelligence as a field. McCarthy made a bold proposal: that aspects of learning and intelligence could, in principle, be precisely described and simulated by machines.

The workshop brought together researchers who believed that human intelligence wasn't some magical, unreachable thing - it was a process that could be broken down into logical steps and rules. They thought if you could describe how humans reason (using symbols, logic, and rules), you could program a computer to do the same thing.

McCarthy didn't just organize the workshop - he also developed Lisp, a programming language that was particularly well-suited for symbolic processing. Lisp made it easier to manipulate symbols and implement the kind of logical reasoning that early AI researchers wanted to build.

Intelligence could be precisely described and simulated by machines using symbolic processing. The core idea was that intelligence = symbol manipulation + logical rules + inference procedures.

If I can write down all the rules for how to solve a math problem step-by-step, then I can program a computer to follow those exact same rules and solve similar problems. They believed this approach could eventually handle all kinds of intelligent behavior.

This was where AI moved from Turing's philosophical thought experiment to an actual research program with specific technical approaches. The symbolic approach made sense because it matched how programmers naturally think about problems - give the computer clear rules and let it follow them.

### 1966: ELIZA - The Power of Simple Tricks

Joseph Weizenbaum created ELIZA, a program that simulated a psychotherapist using keyword matching and templates.

Humans readily attribute intelligence to systems that just do clever pattern matching.

Showed that "appearing intelligent" doesn't require actual understanding - important lesson about human psychology and AI.

My questions while reading was how much of modern AI success is still just sophisticated pattern matching?

### The AI Winters: When Reality Met Hype

**What happened:** Repeated cycles where funding dried up because results didn't match promises.

**Why it happened:**

- Symbolic systems needed enormous hand-coded knowledge
- Hardware wasn't powerful enough
- Real-world problems were messier than lab demos

The gap between proof-of-concept and practical application can be enormous.

## The Neural Renaissance: Hinton and Learning from Data

Not everyone was satisfied with the symbolic approach. Some researchers, including Geoffrey Hinton, had a completely different vision: what if instead of hand-coding all the rules, we could build systems that learn patterns from examples, loosely inspired by how the brain works?

Hinton became a central figure in this movement. He helped popularize using backpropagation to train multi-layer neural networks, which became crucial for modern deep learning. The basic idea was revolutionary compared to symbolic AI: instead of a programmer writing explicit rules, you give a network lots of examples and an algorithm that automatically adjusts the network's internal parameters (called weights) to reduce errors. Eventually, the network discovers useful features and patterns without anyone explicitly programming those rules.

Think of it like this: instead of teaching a child to recognize cats by giving them a list of rules ("cats have pointy ears, whiskers, four legs, etc."), you show them thousands of pictures labeled "cat" or "not cat" and let them figure out the patterns themselves. The neural network approach was betting that this kind of learning from examples could be more powerful and flexible than hand-coded rules.
The intuition was simple but powerful: give a network lots of examples and an algorithm to change internal parameters based on errors, and eventually the network will discover useful features automatically. This was a fundamentally different philosophy from symbolic AI - instead of top-down rule writing, it was bottom-up pattern discovery from data.

Hinton and his collaborators kept pushing this approach even during periods when it wasn't popular, and their persistence laid the groundwork for the deep learning revolution that would come decades later. The key insight was that intelligence might emerge from statistical learning rather than logical reasoning.

## 2012: The ImageNet Moment - AlexNet Changes Everything

This is where everything changed. Krizhevsky, Sutskever, and Hinton created AlexNet, a deep convolutional neural network that absolutely crushed all previous results on image classification using the ImageNet dataset. We're talking about a massive improvement - not just a small percentage better, but dramatically better performance that made everyone in the field take notice.

But here's the key thing I learned: this wasn't just about having a better algorithm. Three critical pieces came together at exactly the right time, and that convergence is what made the breakthrough possible.

First was large datasets. Fei-Fei Li had been working on the ImageNet project, which used Amazon Mechanical Turk to collect and label millions of images across thousands of categories. Before this, researchers were working with tiny datasets that weren't sufficient to train large neural networks. ImageNet provided the massive amount of labeled training data that neural networks needed to learn complex visual patterns.

Second was computational power. GPUs (graphics processing units) that were originally designed for rendering video game graphics turned out to be perfect for the parallel mathematical operations needed to train neural networks. This meant researchers could finally train much larger and deeper networks than ever before.

Third was the deep neural network architecture itself - specifically convolutional neural networks that were designed to recognize visual patterns by learning filters and features at multiple levels of abstraction.

When these three things converged, the results were undeniable. AlexNet proved that the neural approach could deliver dramatic practical improvements on real problems, not just toy examples. This launched what many people call the modern AI boom and showed that the "learn from data" approach could outperform carefully hand-engineered traditional computer vision methods.

The lesson was clear: it wasn't just about having better algorithms - it was about having enough data and compute to make neural networks actually work at scale.

## 2014: GANs - Making Fake Data Look Real

In 2014, Ian Goodfellow introduced something really clever called Generative Adversarial Networks (GANs). The idea was inspired by game theory and competition: what if you train two neural networks against each other in a kind of arms race?

Here's how it works: you have two networks - a generator and a discriminator. The generator's job is to create fake data (like fake images), and the discriminator's job is to tell the difference between real data and fake data. They're trained together in opposition - the generator tries to fool the discriminator, while the discriminator tries to get better at detecting fakes.

It's like having a counterfeiter trying to make fake money and a detective trying to spot fakes. As the detective gets better at spotting fakes, the counterfeiter has to get more sophisticated. As the counterfeiter gets better, the detective has to develop more refined detection skills. Eventually, the counterfeiter becomes so good that even expert detectives can't tell the difference between real and fake money.

In the case of GANs, when this adversarial training process works well, the generator becomes incredibly good at creating synthetic data that looks completely real. The discriminator pushes the generator to capture finer and finer details until the generated data is virtually indistinguishable from real examples.

This unlocked high-quality image synthesis and opened up tons of creative applications - generating realistic faces of people who don't exist, creating art, style transfer, and many other generative tasks. The adversarial training idea became a powerful tool for generative modeling and showed that competition between networks could lead to much better results than training a single network alone.

What struck me about GANs is how they turned machine learning into a kind of creative process - the generator wasn't just learning to classify or predict, but to create entirely new content that captured the essence of what it had learned from real data.

## 2017: Transformers - "Attention Is All You Need"

This was another one of those moments where everything changed. Before 2017, if you wanted to process sequences of text, you typically used RNNs (Recurrent Neural Networks) or LSTMs (Long Short-Term Memory networks). These architectures processed sequences step-by-step - like reading a sentence word by word from left to right. But this created problems: they were slow to train because you couldn't parallelize the processing, and they struggled with very long-range dependencies in the sequence.

Then came the Transformer architecture with a paper literally titled "Attention Is All You Need." The revolutionary idea was to throw out recurrence entirely and replace it with something called self-attention. Instead of processing a sequence step-by-step, the Transformer looks at the whole sequence at once and learns which parts should pay attention to which other parts.

Imagine you're reading the sentence "The animal didn't cross the street because it was too tired." A human immediately knows that "it" refers to "the animal," not "the street." The self-attention mechanism allows the model to directly connect "it" with "animal" regardless of how far apart they are in the sequence. It can look at all words simultaneously and figure out these relationships.

This attention mechanism was incredibly powerful because it could capture long-range dependencies much better than RNNs, and because all the attention computations could be done in parallel, it was much faster to train on GPUs. The model could process entire sequences simultaneously rather than one word at a time.

Transformers became highly scalable with data and compute, which enabled the creation of huge pre-trained models that could be fine-tuned for many different tasks. This essentially changed how we build and deploy AI systems - instead of training a model from scratch for each task, you could take a massive pre-trained Transformer and adapt it to specific problems.

This architecture change enabled the massive scale-up that led to modern large language models like GPT, BERT, and eventually ChatGPT. The Transformer became the backbone of almost all modern natural language processing and many other domains too.

{{< info "Important" >}}

**Moore's Law:** Transistor density doubling roughly every 2 years since the 1960s gave us exponentially more computational power.

Many AI breakthroughs weren't just algorithmic - they became practical because the hardware finally caught up.

## Questions I'm Still Exploring

1. How much of current AI success is still sophisticated pattern matching vs. genuine reasoning?
2. Will we see another "AI winter" if current approaches hit fundamental limits?
3. How will symbolic and neural approaches continue to merge?
4. What's the next hardware breakthrough that will enable the next AI leap?

