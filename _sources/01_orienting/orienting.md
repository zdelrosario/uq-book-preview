(01-orienting)=
# Orienting

## What is a Model?

This book is about models, but what is a model? For our purposes, a **model** is a representation of something in the real world. As a model is only a representation, it is necessarily a *simplification* of the real world thing it represents. This leads to many limitations associated with the model, a fact captured in the famous quote:

```{epigraph}
All models are wrong, but some are useful.

-- George E.P. Box
```

This quote is the inspiration for this book's title: If all models are wrong, then all models are definitely uncertain. Box's adage is profound, but often misunderstood. While quantitative tools in science and engineering are often treated as a source of truth, *all* mathematics applied to describe the physical world are *only* models. Taking Box seriously means that we must directly confront the uncertainties in our models.

```{admonition} Conversations with a Model: What Is a Model?
To provide some additional perspective throughout this book, we've included some "conversations with a model"---lightly-edited conversations with a large-language model (LLM)-based chatbot.

Gianluca: "What is a model?"

Bot: "A model is a simplified representation of a system or process, often used to make predictions or understand the underlying mechanics of the system. Models can take many forms, such as mathematical equations, computer simulations, or physical prototypes. They are often used in fields such as science, engineering, and economics to better understand complex systems and make informed decisions."

Gianluca: "Give me a couple of examples."

Bot: "Sure, here are a few examples of different types of models:

1. In weather forecasting, meteorologists use mathematical models to simulate the Earth's atmosphere and predict future weather patterns.
2. In finance, economists use economic models to predict changes in interest rates and the stock market.
3. In engineering, a physical model of a car is often built to test its aerodynamics and fuel efficiency.
4. In machine learning, a model is a set of algorithms that take in data, learn from it and make predictions or classifications.
5. In the field of biology, researchers use models of cells and organisms to study their functions and interactions with other living things.
6. In physics, theoretical models are used to explain the behavior of subatomic particles and the behavior of the universe as a whole."
```

This book aims to give you both *tools* and *understanding* to handle the uncertainty in models. The tools will come in the form of a *grammar of model analysis*, implemented in the Python package Grama. Understanding comes in many forms, including domain-specific knowledge and more general modeling ideas. In this book, we synthesize ideas from across disciplines to learn how to handle uncertainty in physical models. We will focus less on mathematical details and more on integrating ideas into a practical perspective.

``` {admonition} Conversations with a Model: A Philosopher's Take on Uncertainty
Zach: "Socrates, what is uncertainty?"

Bot: "Uncertainty is a natural aspect of the human condition. We can never truly know everything, and there will always be gaps in our understanding. However, this does not mean that we cannot strive for knowledge and understanding. I believe that the pursuit of knowledge is a lifelong endeavor and that the more we question and reflect on our beliefs, the more certain we can become in our understanding of the world. Through my method of questioning (the Socratic method) I would encourage individuals to question their own beliefs and to seek out the truth through critical thinking and self-reflection. In this way, we can move closer to certainty and understanding, even if we will never reach a state of complete understanding."
```

This first part of the book---Orienting---provides a high-level overview of both components: tools in the form of Grama, and understanding in the form of mindset.

## Intended Audience

This book is intended for students of science and engineering who are focused on mathematical and computational analysis. We have designed the book accordingly:

- **Students**
  - This book is intended for early graduate students and advanced undergraduates in a scientific or engineering discipline. It is intended primarily as a volume for learning but may serve secondarily as a volume for reference.

- **Scientists and engineers**
  - We assume that you know how to carry out a mathematical analysis of physical systems but do not yet know how to quantify uncertainties in those systems.

- **Those focused on analysis rather than experimentation**
  - This book is written from the perspective of computational science. While we will discuss some considerations of experimentation (particularly as it pertains to data), our focus is on computational modeling and analysis.

## Required Skills

We are expecting that you have a few basic skills. To get the most out of this book, you should have:

- Basic proficiency with the Python computing language. You should be familiar with basic datatypes (strings, lists, dictionaries, objects, and methods), control flow (loops), comments, and functions.
  - This book uses the `py-grama` software package to minimize your required coding knowledge. You should be able to use this book if you have taken a first course in Python or have a few months of experience with the language.
- Fundamental understanding of probability, and possibly some knowledge of statistics. You should know what a (continuous) random variable is, and how mathematical objects such as distributions and densities relate to random variables.
  - This book makes *thorough* use of probability. We assume a fundamental knowledge of probability, so this should not be your introduction to probability theory.
  - This book also uses some ideas from statistics. We will use ideas such as estimation and statistical intervals but will provide a gentle introduction to these concepts and will explain them in context.
  - This book is about applying probability and statistics to science and engineering topics, so if you have taken a first course in probability, this book will enable you to put those skills to productive use!
- Fundamental understanding of mechanical physics. You should be familiar with calculus, Newton's laws of motion, and differential equations.
  - This book is organized around case studies: detailed investigations of particular topics. To follow these case studies, you will need some basic background knowledge. However, we will introduce more domain-specific concepts when necessary.
- Domain-specific knowledge from your discipline.
  - You should have the skills to build and implement domain-specific physical models. Your models should be able to map between known input quantities to predict output quantities.
  - This book is intended to inspire you with ideas on how to use uncertainty quantification techniques in practice and to enable you to put those ideas into practice quickly using the `py-grama` programming package. This book will give you new ideas on how to solve problems... and new kinds of problems to solve!

(01-starting)=
## Where to Start / How to Use This Book

This book is divided into three parts (plus appendices):

1. Orienting: High-level ideas for reasoning about uncertainty in models
2. Developing: More detailed ideas for building models and quantifying uncertainty
3. Answering: Case studies applying the aforementioned ideas to complex problems
4. Appendices: Supplemental materials

You can certainly read this book from cover to cover! However, we recommend the following reading strategy.

- Read Orienting of this book in full.
- Skim the case studies in Part 3 to find topics that interest you. Pick one to study further.
- Each case study has a list of "dependency" chapters from Part 2: Developing. Read the appropriate dependency chapters to help understand each chosen case study.

```{admonition} **Exercise: Exercise Ideas.**
To get the most out of this book, you should copy the code examples into your own coding environment and try adapting them. Throughout the book we will mark these exercise ideas with similar "Exercise" blocks.
```