# Orienting

```{epigraph}
A detective investigating a crime needs both tools and understanding. If he has no fingerprint powder, he will fail to find fingerprints on most surfaces. If he does not understand where the criminal is likely to have put his fingers, he will not look in the right places. Equally, the analyst of data needs both tools and understanding. It is the purpose of this book to provide some of each.

-- John Tukey (1977)
```

Our opening quote comes from Tukey's classic text *Exploratory Data Analysis*
{cite}`tukey1977eda`. Like his work, this book aims to give you both tools and
understanding. The tools will come in the form of a *grammar of model analysis*,
implemented in the Python package Grama. Understanding comes in many forms,
including domain-specific knowledge and more general modeling ideas.
This book will elaborate on many ideas about modeling and uncertainty, as well
as higher-level skills on an investigative mindset.

This first part of the book---*Orienting*---gives a high-level overview of
both components: tools in the form of Grama, and understanding in the form of
mindset.

## Who is this book for

This book is intended for early graduate students and advanced undergraduates in a scientific or engineering discipline. As a result, we are expecting that you have a few basic skills:

- Basic proficiency with the Python computing language. You should be familiar with basic datatypes (strings, lists, dictionaries, objects and methods), control flow (loops), comments, and functions.
  - This book makes use of the `py-grama` software package to minimize your required coding knowledge. You should be able to use this book if you have taken a first course in Python, or have a few months of experience with the language.
- Fundamental understanding of probability, and possibly some knowledge of statistics. You should know what a (continuous) random variable is, and how mathematical objects such as distributions and densities relate to random variables.
  - This book makes *thorough* use of probability. We assume fundamental knowledge of probability, so this should *not* be your introduction to probability theory.
  - This book also uses some ideas from statistics. We will use ideas such as (maximum likelihood) estimation and statistical intervals, but provide a gentle introduction to these concepts and will explain them in-context.
  - This book is about *applying* probability and statistics to science and engineering topics, so if you have taken a first course in probability, this book will enable you to put those skills to productive use!
- Fundamental understanding of introductory mechanical physics. You should be familiar with calculus, Newton's laws of motion, and differential equations.
  - This book is organized around *case studies*: detailed investigations of particular topics. In order to follow these case studies, you will need some basic background knowledge. However, we will introduce the more domain-specific concepts when necessary.
- Domain-specific knowledge from your own discipline.
  - This book is intended to *inspire* you with ideas on how to use uncertainty quantification techniques in-practice, and to *enable* you to put those ideas into practice quickly using the `py-grama` programming package. We hope you have your own scientific problems to solve, and that this book gives you new ideas on how to solve them!

<!-- ## How to use this book -->

<!-- TODO -->
