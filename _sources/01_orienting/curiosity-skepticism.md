# Curiosity and Skepticism: A Healthy Mindset

---

This opening chapter is focused on helping you develop a *healthy mindset* for
scientific investigation. This mindset is composed of two opposing *modes* of
operation: curiosity and skepticism.

**Learning Objectives** In this chapter, you will learn

- the dual "modes" of *curiosity* and *skepticism* [^bill]

```{admonition} Running Example: Detective Enola
Examples are helpful! This book is full of examples of curiosity and skepticism
in-action. But before we introduce any of the detailed scientific case studies,
let's use the context of a detective story for this chapter: The owner of a
large fortune has just been found in his manor with a knife in his back, and our
detective Enola suspects one of his kin is responsible. As we'll see below, the
protagonist of a murder-mystery exemplifies the dual mindset of curiosity and
skepticism.
```

## Not a Procedure, but Rather a Mindset

Upfront, it is important to note that curiosity and skepticism are not a fixed
*procedure*, but rather two modes of a *mindset*. The items below are not so
much a checklist to go through sequentially, but rather a set of "moves" we can
employ during the scientific investigative process.

An analogy: The U.S. legal system is based on the idea that truth can be found
by pitting two rational opposing forces against each other. Through defense and
prosecution teams working against each other, presenting evidence and finding
holes in each others' arguments, society can come closer to the truth and hence
justice.

The back-and-forth between curiosity and skepticism is similar: two modes we
should switch between during scientific investigations. By engaging in curious
behavior, we can ask questions and pose answers. By engaging in skepticism, we
can identify flaws and improve our analysis. Let's look at the two modes in
greater detail.

## Curiosity

The mode of curiosity is characterized by openness: to exploration, to new
questions, to approaches, and to possible answers. Some of the "moves" in the
curious mode include:

### Asking questions

The very notion of curiosity is closely associated with asking questions; we
describe a child as "curious" if they tend to ask a lot of questions. Most
scientific investigations start with some sort of "global question" that kicks
off a research effort. However, the process of asking questions doesn't stop
there.

As Tukey {cite}`tukey1977eda` writes in the context of exploratory data
analysis, TODO...

```{admonition} Running Example: Detective Enola
:class: tip
In a murder-mystery, a detective will generally have one overarching question:
"whodunnit?" But to answer this driving question, Enola will have to pose and
answer a variety of sub-questions: Who are the suspects? What facts do I know?
Why is the eldest son being cagey? These questions can help the detective decide
what data to gather next.
```

### Gathering data

Questions are useful in part because they focus our efforts. One of the main
ways we make progress in answering our questions is to gather data.

In scientific modeling, we can gather both *experimental* data (from a physical
experiment) and *synthetic* data (from a simulation). Experimental data requires
running a physical experiment, necessitating time and hardware but serving as
the ground-truth for reality. Lightweight computational models can be run far
more quickly to suggest possible trends, which can aid in planning physical
experiments.

Note that we can gather data in a curious *exploratory* way, or in a more
skeptical *testing* fashion. The data collection we plan in the curious mode
will tend to be more ad hoc. Perhaps we plan out a quick pilot study, or get our
hands on some archival data that is only somewhat associated with our question.
The point of gathering data in the curious mode is not to be comprehensively
formal; rather, it is to move quickly and refine our questions so we can move
towards the greater clarity of a formal hypothsis.

```{admonition} Running Example: Detective Enola
:class: tip
Even before our detective formulates an answer to a question, she will try a
variety of "moves" to advance her investigation. Enola might try dusting for
prints at the scene of the crime, interview eyewitnesses to search for plausible
motives, or send the murder weapon out to the lab for a forensic test. For
Enola, the coroner's examination of the body provides a time of death, blunt
trauma on the face, and a knife-wound as the cause of death, all of which narrow
the set of possible hypotheses.
```

### Posing hypotheses

The primary output of the curious mode is a *testable hypothesis*. This is a
synthesis of the available data and initial questions, one which ideally
addresses our original global question. Arriving at a hypothesis is often the
departure point from the curious mode to the skeptical one.

Posing a hypothesis requires *interpreting* the data. This is where
domain-specific knowledge of our problem is **essential**: Only a specialist in
your field can interpret the data in terms of your discipline's accepted
conventions. However, regardless of one's discipline, there is one criterion
that all hypotheses *must* meet---a scientific hypothesis must be *testable*.

As Popper {cite}`popper2005logic` wrote on the philosophy of science, a
scientific hypotheses should be specific enough to be *falsifiable*; that is,
able to be shown to be false. Falsifiability is a reasonable criteria for
determining what is a testable hypothesis. If our hypotheses is too flexible or
too vague to be testable, this is a sign that the hypothesis needs refinement!
Usually, a falsifiable hypothesis makes predictions about what would happen
under a certain experimental setting; in this case, the hypothesis would be
falsified if the prediction failed to hold.

```{admonition} Running Example: Detective Enola
:class: tip
Enola wants to know "whodunnit," so her hypothesis should include a suspect,
motive, and opportunity. Enola suspects the eldest son is responsible, as the
household staff intimated that he is greedy and impatient to inherit. She makes
sure to incorporate all the data she has gathered in formulating her hypothesis;
she thinks the son stabbed the victim in the back with a knife around the time
of death, causing the victim to fall forward onto their face.
```

## Skepticism

The mode of skepticism is characterized by rejection: rejecting hypotheses,
finding flaws in the data and methods, and even probing the importance of
questions. Some of the "moves" in the skeptical mode include:

### Testing hypotheses

Once we have posed a hypothesis, it is important to subject it to testing. As
noted under *Posing hypotheses* above, any scientific hypotheses must be
*testable*, usually by being *falsifiable*. If the hypothesis is untestable, you
need to go back and refine your hypothesis! However, you might not recognize
your hypothesis as untestable until you switch over to the skeptical mode.

Remember, a skeptic would not use a "gentle" test. Try to formulate a strenuous
test of your hypothesis. What would a worst-case look like for your hypothesis?
What would be a convincing argument, even to your toughest critic?

We'll see more about this in Chapter TODO, but as a preview, you should use data
that are independent of your exploratory data to test a hypothesis. In the
parlance of machine learning, testing a model on the same data used to train is
a biased, foolish way to assess a model {cite}`james2013introduction`. If your
hypothesis is true, then your findings should hold for an independently-gathered
dataset.

```{admonition} Running Example: Detective Enola
:class: warning
Enola is confident in her hypothesis, so she makes an accusation of the son.
However, he denies the accusation and produces a compelling alibi: He was with
the Butler all through the time of death, and the Butler is beyond reproach.
Clearly something about Enola's hypothesis does not hold up.
```

If your hypothesis does *not* hold, then you need to trace back your reasoning.
This includes both your data and your interpretation of the facts.

### Questioning the data

Sometimes, the *data themselves* are in error. Experiments can have confounding
variables, simulations can be misconfigured or unconverged, and even simple
matters of updated inputs without re-evaluated outputs can cause great confusion
[^mismatch]. When your hypothesis does not hold, it is important to hunt down
and eliminate these kinds of issues.

As we will see in Chapter TODO, *variability* in measurements can be either
*real* or *induced*. Real variability affects the quantity we aim to study,
while induced variability affects our measurement only. Determining whether the
variability we see is due to real or induced sources helps us narrow our search
to either before or after the phenomenon we seek to study. If there is an
explanation for induced variability, then our measurement is subject to a
*mistake*. Collecting new data while eliminating such sources of induced
variability will help us more accurately understanding our object of scientific
study.

```{admonition} Running Example: Detective Enola
:class: warning
Enola thinks there is something fishy about the time of death, and has a longer
conversation with the coroner. A closer inspection of the body confirms the time
of death, so the data do not seem to be in error....
```

### Questioning the interpretation

Sometimes the data are not in error, but rather our *interpretation* is
incorrect. This can mean we made an error in our reasoning, or that we were
missing some key facts about the scenario at hand.

Real variability with an assignable cause is called an *anomaly*: If we see
unexpected variability in our measurements that seems to arise from some
consistent phenomena, we might find that a previously unknown phenomenon can
explain this behavior [^lurking]. Such anomalous variability can lead to a
scientific discovery. However, a *lack* of variability can also lead to
scientific advancement.

Before Einstein formulated his theory of relativity (TODO circa 19XX), all waves
had been observed to travel within some medium. Hence, scientists at the time
believed that light, exhibiting wave-like properties, must travel within a
medium called the *lumineferous aether*. Scientists like Albert Michelson (TODO
citation needed) carried out experiments to detect the "aether wind" due to the
motion of Earth through this aether, but failed to detect any change in the
speed of light. Einstein's contribution overturned this understanding of
physics, and our modern understanding is that light travels through a vacuum at
a speed constant to all observers.

```{admonition} Running Example: Detective Enola
:class: tip
In conversation with the coroner, Enola realizes that the knife wound and face
trauma could have occurred at very different times. If the victim were killed at
one time and their body clumsily moved later, this could account for both
wounds. Upon further investigation, Enola finds a cunning mechanism hidden in
the victim's chair: The father died by a deadly trap while the son was with the
Butler, and the son returned much later to rearrange the scene to make it appear
to be a much simpler murder. By employing both curiosity and skepticism, Enola
solved the case.
```

## Uncertainty and Mindset

This book is focused on modeling in the presence of *uncertainty*. TODO

(Modeling is iterative; moving between the modes of curiosity and skepticism to reduce uncertainty to a level sufficient to answer your modeling question)

## Learning the Mindset

These ideas about curiosity and skepticism are important, but if they remain
ideas *only* they are useless. It is important for you to go beyond simply
*knowing* about these ideas and start *using* them in your own scientific
practice. However, this is easier said than done!

To help you make use of the curious and skeptical modes, we have a few
suggestions:

### Using this book

The case studies in this book are written to emphasize the modes of curiosity
and skepticism. Keep an eye out for the following boxes, as they will highlight
elements of the case studies that correspond to curiosity- or
skepticism-in-action.

```{admonition} Curiosity
:class: tip
Here's an example of curiosity-in-action.
```

```{admonition} Skepticism
:class: warning
Here's an example of skepticism-in-action.
```

With a bit of imagination, you can generalize these sorts of insights to your
own context. While reading this book, think about ways the same kinds of
observations or issues could show up in your own scientific investigations.
Better yet, try practicing some of the techniques suggested in this book on your
own problems!

[^bill]: I am grateful to Bill Behrman, who first introduced me to the idea of curiosity and skepticism as modes of operation.

[^mismatch]: We will see an example of mismatched inputs and outputs in Chapter TODO.

[^lurking]: We will see an example of *lurking variables* and techniques to detect them in Chapter TODO.
