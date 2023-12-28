(01-modeling-process)=
# The Modeling Process
```{index} single: modeling ; process
```

This chapter introduces a general *modeling process*. Much of the real work of modeling does not involve manipulating equations or running simulations but rather focuses on broader critical inquiry. The modeling process presented here is focused on posing and answering scientific questions within a chosen context.

**Learning Objectives** In this chapter, you will learn:

- the importance of a question to guide modeling,
- model fundamentals: the system boundary and quantities of interest (QOI), and
- key steps to modeling: gathering information and building and assessing the model.

## Start with a Modeling Question
```{index} single: modeling ; questions
```

Scientific modeling is done to answer some form of question, which we will call a **modeling question**. Some examples of modeling questions include "How can we make this bridge design safe?" "What will the global mean temperature be in the year 2100?" "Do we need this assumption to explain this observed phenomenon?"

To help steer modeling, we need to first understand what sort of question we are asking. The framework in **{numref}`Figure %s <fig-modeling-specificity-action>`** categorizes such questions based on the *kind of action* we will take and the *degree of specificity* in our question. We list four examples on these axes, which will be described in detail later in the chapter.

:::{figure-md} fig-modeling-specificity-action
<img src="../images/specificity-action-axes.png" alt="Specificity and Action axes" width="75%">

The four modeling examples in this chapter, plotted on two axes. The *specificity* axis refers to the generality of the modeled scenario. The *action* axis refers to how directly the modeling work will influence a decision.
:::

### Action: Rhetorical or Direct
```{index} single: modeling ; action
```

The action axis ({numref}`Figure %s <fig-modeling-specificity-action>`) ranges from *direct* to *rhetorical*. **Direct action** implies the modeler (or modeling team) will take action on their own. In industry, designers use models to inform their decisions. The distinction between detailed and conceptual design then hinges on the specificity of the questions that the designers are posing. Note that *truly* direct action is rare in practice; most organizations diffuse decision power to some degree. However, direct action is a useful contrast to *rhetorical action*.

**Rhetorical action** refers to the modeler's efforts to influence others' actions. The modeler will not be taking direct action based on the model's results. This is often done in research, where a researcher publishes a paper explaining a specific phenomenon with the intent of inspiring other researchers to build on their ideas. This is also done in the policy space, where modelers predict the potential outcomes for different policy choices, with the aim of informing and influencing decision makers. While it is always important to be effective when communicating the results of a study, such communication is even more crucial when one's goals are rhetorical.

Note that the distinction between direct and rhetorical action is a continuum rather than a binary. Research on organizations has shown that formal analysis (modeling being one form) serves as both a decision aid and a rhetorical tool {cite}`langley1995between`. Structural factors such as the concentration of power, the level of participation of individuals, and divergence of opinions will affect the prevalence and efficacy of formal analysis in an organization.

```{tip} **Action and Consequence.**
Different kinds of action carry with them different consequences. Direct action obviously carries direct culpability: An engineer who makes a faulty design decision carries the responsibility when that system fails. A negligent engineer will face reputational and financial damage as a consequence of their faulty actions.

However, rhetorical action still carries consequences: Creating a financial model that leads others to make unsound investment decisions may not wreck your own finances, but it can cause suffering for millions of others. {cite:t}`oniel2016weapons` writes in *Weapons of Math Destruction* about her disillusionment with mathematical modeling in the financial sector, where "people had deliberately wielded formulas to impress rather than clarify." This kind of modeling opacity contributed to the 2008 financial collapse.

When modeling to support direct action, make sure to carry out your work with integrity. When modeling to support rhetorical action you must do the same, but with the added responsibility to communicate clearly and effectively.
```

### Specificity: General or specific questions
```{index} single: modeling ; specificity
```
```{index} single: design ; detailed design
```
```{index} single: design ; conceptual design
```

The *specificity axis* ranges from general to specific. A **specific question** concerns a particular scenario, while a **general question** deliberately seeks to transcend these specifics. For instance, a detailed design must include detailed drawings: a style of technical communication that specifies the dimensions and tolerances for all components in a system. Such a task is necessary but extremely laborious; modeling cannot be done at the detailed level throughout the entire design process. Therefore, engineering design first passes through a conceptual design phase. In conceptual design, a far more coarse description of the system is articulated, and consequently the questions posed and models used are far more general {cite}`pahl2007,keane2005computational`.

Specificity is not an absolute, but rather a relative, discipline-specific concept. In engineering design, the highest level of detail is a full geometric and material specification of a system. However, in climate modeling, producing a full geometric representation of the Earth (including every tree, every blade of grass, etc.) is simply not possible. Furthermore, seeking this level of detail in a climate model is not necessary, as an engineering level of geometric detail would be wasted effort in this context.

```{tip} **Specificity and Certainty.**
By their nature, questions with different levels of specificity require different levels of certainty. For example, the conceptual design of an aircraft explicitly acknowledges that low-level details about the aircraft are not yet available, so a fully accurate prediction of performance is not feasible. Performance assessments for a detailed design are held to a much higher standard of predictive accuracy, as these predictions will be used to tune the design to meet performance goals and safety requirements. This difference is one of *acceptable certainty* for the question at hand, with greater specificity enabling greater certainty.

However, a high level of specificity by itself does not imply that the appropriate level of certainty must be strict. The required level of certainty is also affected by the *consequences* of making an incorrect decision, as we will see in {numref}`Chapter %s <02-vnv>`.
```

### Examples of modeling questions

To illustrate the modeling question framework and the diversity of potential modeling questions, we provide a few examples of modeling questions here.

#### HIV infection modeling: Proof-of-concept explanation

In the 1990's, AIDS (acquired immunodeficiency syndrome), caused by HIV (human immunodeficiency virus), was an under-researched disease. Patients with the disease were observed to experience a spike in the number of viral particles in their body, with a subsequent sharp decrease in viral particles as the disease transitioned to an inactive period. This decrease was assumed to be due to an immune response to the virus. However, {cite:t}`phillips1996reduction` presented a model for viral population dynamics that replicated the observed spike in viral particles but did not include any specific immune response. This questioned the prevailing assumptions in the HIV/AIDS research community and raised new questions for future research.

Note that the modeling work of Phillips did not attempt to make a patient-specific prediction, and yet this work was published in the journal *Science*. In this case, the modeling question was very general: Can the reduction in viral particles be explained without a specific immune response? Despite its generality, this question was of great interest to HIV/AIDS researchers.

```{index} single: assumptions ; being explicit
```

This work explicitly neglected known details about reality (specific immune responses) as a core feature of the modeling work. This example illustrates that modeling is not simply an exercise in adding complexity, or even an attempt to represent all aspects of reality in the model. Instead, it is a process that must be anchored in the modeling question that one seeks to answer.

#### Environmental impact of a wind farm: Project evaluation

The National Environmental Policy Act (NEPA) requires federal agencies to engage in an environmental review process when making decisions {cite}`NEPAguide`. Federal agencies prepare an environmental impact statement (EIS) predicting the specific impacts of proposed actions on the environment. Because these impacts are often stated in quantitative terms, such as tons of emissions, quantitative modeling is often used to answer questions such as "How much will this action reduce annual emissions?"

As a concrete example, consider the final EIS of the Vineyard Wind 1 Offshore Wind Energy Project in Massachusetts {cite}`eis20210028`. This study looked at the various environmental impacts of a proposed offshore wind energy farm, attending to the specific geographic layout of the proposed generators. This EIS included numerical predictions of the reduction in annual pollutants, such as carbon dioxide. This analysis was *highly* specific---it did not consider wind farms in the abstract but rather the particulars of this proposed wind farm.

These analyses were carried out across different proposed configurations to support other decision-makers in choosing the final wind farm design. While these results certainly supported making design decisions, the scientists carrying out the analysis were *not* directly responsible for making decisions about the wind farm layout. For this reason, the action in this study was more indirect or *rhetorical*. This kind of indirect action is of key importance to protecting the environment: The organization designing and building the wind farm is incentivized to maximize profits, possibly by building a wind farm that generates a lot of energy but disrupts the local ecosystem. Having an independent group of scientists conduct the EIS---engaged in indirect action---helps to ensure any negative impacts are minimized or offset by mitigation measures.

Notably, an analysis of incomplete or unavailable information is required when conducting an environmental review: The Vineyard Wind 1 EIS details this in Appendix H {cite}`eis20210028`. For instance, this EIS acknowledged that a detailed emissions inventory over a 30-year period was not conducted. This lack of analysis leads to increased uncertainty about the project outcomes; however, the authors note that such uncertainty is tolerable for decision-making, as all of the proposed project options would work to *improve* air quality. Since this source of uncertainty would not affect the decision process, this particular detailed analysis was deemed unnecessary.

#### Structural engineering safety factors: Code calibration

Buildings are never deliberately loaded to failure. However, structural engineers need to make modeling assumptions to analyze and design buildings to prevent failure. Thus, it is rare for the assumptions made in structural design to be directly tested {cite}`gainsburg2007mathematical`. This raises a natural question: "How do structural engineers design safe buildings?" In practice, Structural Engineers use highly-regulated analysis procedures called *design codes*.

The development of design codes leans heavily on physical modeling: The developers of these codes essentially codify modeling assumptions that practicing engineers will use to design real buildings. This is action is highly direct, in the sense that the decisions in design codes will be required for structural engineers (not merely a suggestion). However, this is not *fully* direct, as practicing engineers will still need to exercise engineering judgment to handle cases not covered by the codes {cite}`gainsburg2007mathematical`.

Setting design codes involves the calibration of safety factors that help to ensure building safety despite modeling assumptions. This calibration process is more specific than a typical scientific study: Code designers must consider the particulars of structural engineering, e.g., the statistics of different kinds of loads, different kinds of joints, and even variability across different construction crews {cite}`galambos1981load`. However, this kind of calibration necessarily maintains generality: The factors are designed to be used across multiple design projects.

We will discuss the calibration of safety factors in the case study in {numref}`Section %s <03s-design-codes>`.

#### Early design decisions: Aircraft material selection
```{index} single: design ; conceptual design
```

Designing a modern aircraft is an enormously complex task. Commonly, an interdisciplinary team of ~30 experts will work for a year just to establish the business case for a new aircraft concept, after which more detailed design work can begin {cite}`keane2005computational`. Decisions made at this stage are important, as they can lock in choices that cannot be changed without considerable expense. However, decisions at this stage must also be made with limited information---quantities such as the precise weight of the aircraft simply cannot be known in the early stages of design.

One important consideration in the early stages of design is to select what materials to use for the various components of the aircraft. Important business factors such as the cost and performance of the aircraft will depend on the materials used in construction. This leads to the modeling question "What aircraft construction materials should we choose?"

This kind of question is the most direct form of action one can take: The design team will ultimately be responsible for making this decision. However, the specificity of the modeling is necessarily limited at the early design stage. Often, simplified physical models are used to support materials selection; these leave out the undetermined factors of the design but allow for principled comparisons across different material choices {cite}`ashby2005`.

Once we have determined our modeling question, we can proceed with building the model.

## Define the System by Its Boundary
```{index} single: modeling ; system boundary
```

The first step in building a model is to define the *system*: the set of things that are explicitly tracked inside the model. A system is defined by a **system boundary**, an imaginary line that separates what is inside the system from what is considered part of the outside world. **{numref}`Figure %s <fig-modeling-system-gen>`** shows a generic example of a system boundary.

:::{figure-md} fig-modeling-system-gen
<img src="../images/system-diagram-general.png" alt="Generic system boundary" width="75%">

A generic system boundary.
:::

Slicing the world apart like this necessarily leaves out some details. In response, we model the internals of the system along with *interactions* across the system boundary with the rest of the world. Then the modeler must account for all of the important interactions between the system and the surrounding world to build an accurate model. Part of the skill in modeling is to make sound choices about where to draw one's system boundary and what interactions to include. These choices are extremely discipline-specific; however, there are some general principles to consider.

If the system boundary is drawn close to what we care about, then fewer physical phenomena are included in the model. This will mean that fewer components are inside the model, reducing internal complexity. However, the many phenomena kept outside the model may cross the system boundary, necessitating modeling their interactions with the system. Conversely, if the system boundary is drawn far from what we care about, then more physical phenomena are included in the model. This requires detailed modeling of the phenomena that now live inside the system boundary, but may result in fewer interactions across the boundary. Navigating this concept of "boundary distance" should be done in part by considering what to model as an internal component of the model and what to consider as an interaction across the boundary.

As a more concrete example, the HIV infection model considered not the entire human body but rather a representative bit of tissue containing infective viral particles {cite}`phillips1996reduction`. Cells and viral particles can move into and out of the region described by the system; therefore, these interactions are depicted in the system boundary (**{numref}`Figure %s <fig-modeling-system-hiv>`**).

:::{figure-md} fig-modeling-system-hiv
<img src="../images/system-diagram-hiv.png" alt="System boundary diagram, HIV tissue patch" width="75%">

A system diagram for the HIV modeling example.
:::

In the case of the HIV infection model, the region is representative in the sense that the whole body is assumed to be exposed to the virus in equal concentration, and that there is little spatial variation across the body when it comes to immune response. If this were the case, then any small region of the body would be experiencing the same infection dynamics. This seemingly reductive assumption is a useful simplification that is well-aligned with the modeling question that drives this study: Can infection dynamics resembling what is observed in patients be generated *without* including a specific immune response? Complex spatial variability is not at all related to the modeling question, and so a representative patch will do. If this simple model can replicate the observed dynamics, it suggests that there is a very simple explanation for the observed behavior, and that more complex reasons are not necessary.

## Choose Quantities of Interest
```{index} single: modeling ; quantity of interest
```
```{index} seealso: QOI ; modeling ; quantity of interest
```

After formulating our modeling question and defining our system, we must pick **quantities of interest** (QOI) to help turn our modeling question into a measurable test. A QOI should be some quantity that has relevance to the question we are trying to answer: Some examples of QOI include the trajectory of a projectile, the percent yield of a manufacturing process, and the count of some cell in a body. Sometimes a QOI will be quite complicated; for example, the trajectory of a projectile is a curve through space and time. Often we need to define *metrics* to reduce a complicated QOI to a simpler quantity. For instance, we can summarize a projectile trajectory by considering its range, the horizontal distance at which the projectile hits the ground.

Sometimes the appropriate QOI will seem clear. The HIV/AIDS question discussed previously is obviously concerned with a count of viral particles. However, even in such seemingly obvious cases, there are important decisions to be made: Are we talking about the total count of viral particles in the entire body, or will a small representative volume of tissue suffice? Are we interested in a long-term average count of cells, or do we need to consider a more instantaneous count of cells? You can only make these kinds of decisions by carefully considering your modeling question.

More subtly, assumptions about human values are encoded in your choice of QOI {cite}`saltelli2020five`. For instance, profit is often taken as the sole QOI for businesses, but this neglects other factors we would want to promote in society, such as the well-being of people and the sustainability of the planet. Alternatives to a profit-only quantification of business success include the *triple bottom line concept* {cite}`slaper2011triple`, which quantifies social and environmental impact along with profit.

```{warning} **The Dangers of Quantification.**
In their modeling manifesto, Andrea Saltelli and colleagues {cite}`saltelli2020five` warn that "Once a number takes centre-stage with a crisp narrative, other possible explanations and estimates can disappear from view." While modeling quantities of interest and computing metrics are useful for addressing a question, important factors in any situation can be difficult to quantify and thus to include in a model. Make sure to keep in mind the limitations of your approach, particularly what is *not* represented in your model.

As we'll see later in the chapter, model assessment can help to clarify the limitations of your model.
```

## Gather Appropriate Information

Physical principles can be used to build a mathematical model to predict quantities of interest. For instance, principles from Newtonian mechanics can be used to study the motion of a projectile. To support building the projectile model, we could build an inventory of forces that act on our projectile. More generally, when building a model we can search for existing principles (or whole models) that other researchers have used for similar problems.

Through searching for relevant physical principles, we are likely to come across *model inputs* whose numerical values we will need to set in our model. For instance, a projectile will be affected by its mass, initial velocity, and aerodynamic drag characteristics. Depending on the projectile and the specificity of our modeling question, we may need to consider additional factors, such as its spinning motion (as with a baseball) or surface roughness.

```{index} single: modeling ; input vs parameter
```
```{warning} **"Parameter" or "Input"?**
What we call an "input" is similar to what some call a "parameter." However, note that the term parameter is used differently across disciplines. Parameter to a scientist or engineer follows the definition of model input we see here; a quantity that enters a model. However a parameter to a statistician refers to a property of a random variable. We will encounter this statistical definition in {numref}`Chapter %s <02-distributions>`.
```

```{index} single: modeling ; input
```

Model Inputs
: A *model input* is a quantity (numerical, categorical, or otherwise) in a model that must be set to some value in order to use that model.

Note that we are likely to find a range of possible input values, or possibly repeated measurements that point to variability in the input values. This information is important to collect, as we will use this information to build a distribution representation of uncertainty (see {numref}`Chapter %s <02-distributions>`).

In some cases, physical theory will not be sufficient to describe all of the physical phenomena using a first-principles approach. In these cases, one can use a particular form of data to build an *empirical model*: Repeated observations on input and output quantities can enable statistical (data-driven) modeling of the observed phenomena. If an empirical approach is necessary, then it will be necessary to obtain and curate such a dataset before building the model. {numref}`Section %s <02s-modeling-functions>` will discuss both physical and empirical models.

## Build the Model

With the principles and data gathered as we've discussed, we can then build the model. As noted in {numref}`Chapter %s <01-orienting>`, we assume that you have the skills to implement domain-specific *deterministic models* from your own discipline. This will involve using physical principles to write down a mathematical model, then using a programming language to implement that model as computer code. Your deterministic models should be able to map from inputs to the output quantities of interest that you seek to study. The remainder of this book is about a set of tools and understanding to complement your existing domain-specific modeling skills with rigorous tools to handle uncertainty. We will use the `py-grama` package (see {numref}`Chapter %s <01-grama-intro>`) to implement these ideas.

As we'll see in {numref}`Chapter %s <01-grama-intro>`, a Grama model contains information about the inputs and the map between inputs and outputs. We will use *distributions* in our models to represent uncertainty in model inputs. We will also fit empirical (data-driven) models to "fill the gaps" when physical principles alone are insufficient to predict our desired quantities of interest. The following chapters of this book will cover these ideas in detail.

```{warning} **"Everything must be made as simple as possible, but no simpler."**
This famous quote by Albert Einstein is a central tenet in modeling: Resist the urge to add complexity for complexity's sake. All complexity in a model must be justified as necessary to answer the modeling question.
```

(02-vnv)=
## Assess the Model
```{index} single: modeling ; verification and validation
```

Once we have built our model we must assess it relative to our modeling question. The concepts of verification and validation are used by physical scientists to build confidence in their models. We must also consider the level of certainty that is necessary for our context.

### Verification and validation

While we make use of curiosity and skepticism throughout the modeling process, assessing the model is where we formally deploy mathematical techniques to put skepticism into practice. Model assessment should include two key steps: *verification* and *validation*. Here we use the AIAA definitions of these terms {cite}`aiaa1998vnv`.

Verification
: The process of determining that a model implementation accurately represents the developer's conceptual description of the model and the solution to the model.

To check that we have implemented the model in code correctly, the code should be "stress tested." The specific mechanics of verification vary based on the type of model and implementation; thus, a comprehensive treatment of all verification approaches is beyond the scope of this book. However, some general principles apply: When carrying out a verification study, make sure to check *emergent behavior* of the model, rather than manually-enforced properties of the model.

For instance, in a trajectory prediction code, it would *not* be a rigorous verification exercise to simply check that the input values of the model are set to the correct values. Instead, one should check that the output results satisfy known physical principles; for instance, that the range of the projectile increases with increased initial velocity.

When feasible, a useful verification step is to check that the code-generated solution matches a hand-calculated result. This can be done by generating a solution expression that holds at multiple input values, such as a trajectory across time. However, it can also be helpful to check the solution against an asymptotic value, such as the behavior as time marches toward infinity. A more general approach to this form of correct-solution generation is the *method of manufactured solutions* {cite}`roache2002code`, which is often used for testing simulation codes for partial differential equations.

While verification checks that the model is implemented correctly, it is also key to check that the model is a faithful representation of reality.

Validation
: The process of determining the degree to which a model is an accurate representation of the real world from the perspective of the intended uses of the model.

Note that the definition of validation explicitly references the "intended uses of the model"; the accuracy of a model can only be assessed *within the context of its intended use*. This means we must have our modeling question in mind when designing and executing a validation study. A modeling question requiring specific, detailed predictions should involve a validation exercise that tests for the necessary level of accuracy. For instance, when designing a bridge, a high level of confidence is needed in the specific numerical predictions of load capacity and resilience of the structure.

However, validation need not involve a direct comparison of model results to data. For instance, in the HIV/AIDS example mentioned previously {cite}`phillips1996reduction`, the author did not carry out any explicit comparison of simulated viral particle counts against measured clinical data. Instead, the author built upon previously published models---establishing credibility based on starting from accepted models---and compared the results *qualitatively* to observed clinical trends. While this sort of validation would not be appropriate for supporting bridge design, as the author's modeling question was quite general, this style of validation was appropriate for the intended use of the model.

Finally, remember that even a properly validated model is not proven to be correct! Validation builds confidence in the model for the tested scenario, but there is always danger in extrapolating to an unseen scenario. The *problem of induction* {cite}`popper2005logic` is an inherent limitation in the practice of science, meaning we should always maintain a bit of healthy skepticism toward any model.

```{tip} **A Helpful Mnemonic.**
Verification is often said to be an exercise in mathematics and coding, while validation is an exercise in physics. Verifi**c**ation is about the **c**ode used to implement the model, while vali**d**ation often involves comparing model results against physical **d**ata.
```

We will see many examples of validation in this book, with a particular focus in {numref}`Chapter %s <02-functions>` {numref}`Section %s <02s-practical-fitting>`.

### How much certainty is needed?
```{index} single: certainty
```

In discussing validation, we saw that different levels of accuracy are needed for different types of modeling questions: Clearly a general question does not need the same level of accuracy as a specific question. Related to accuracy is the concept of *certainty*[^aristotle].

[^aristotle]: The idea that certainty ought to vary based on the context is as old as Aristotle, see e.g. 1098a of {cite}`rackham1934ne`.

While we will discuss uncertainty more formally in {numref}`Chapter %s <02-uncertainty>`, note that the level of certainty necessary to answer a modeling question depends on more than just the specificity of the question. Here we discuss a few questions to ask yourself to determine how much certainty is needed.

#### What are the consequences of making an incorrect conclusion? 

If the consequences are innocuous---say, yours is a proof-of-concept effort---then a great deal of certainty is not needed. The HIV/AIDS example we discussed previously sought to provide a potential explanation for observed phenomena, and suggested further work. An incorrect conclusion in that example might mean contradictory evidence would be found that refuted the original study. This would still be a net win for the scientific community. However, a model aimed at making patient-specific predictions for surgical decisions would obviously have greater consequence. These more significant consequences would demand a higher level of certainty.

```{tip} **Analogy to the Legal System.**
In the United States legal system, there exist different "standards of proof"---codified levels of certainty. These standards are used for different types of legal cases that carry different consequences. For instance, the highest standard, "beyond a reasonable doubt," is reserved for criminal cases, where the liberty of an individual is at stake. For civil cases, the consequences involve financial damages; these relatively lower stakes mean a lower standard of certainty is used: "a preponderance of the evidence" (colloquially, "more probable than not") {cite}`black1968law`.
```

#### What have we learned so far? 

It is rare to be able to state a specific, numeric level of required certainty for a given modeling question *a priori*. More frequently, you will discover a lack of certainty through the modeling process. At this point, you will likely need to gather more information (to reduce uncertainty) or change your modeling question (to acknowledge limitations). Keep in mind that modeling is an iterative process, as we'll discuss further in {numref}`Chapter %s <02-model-iterate>`.

#### Do you have an answer?

Sometimes in evaluating the certainty necessary for a particular question, you may find that the present uncertainty is intolerable because you simply do not have the means to answer the question. In these cases, you should be honest with yourself and any stakeholders; as {cite:t}`saltelli2020five` write in their *modeler's manifesto*, "Experts should have the courage to respond that 'there is no number-answer to your question.'"

(02-model-iterate)=
## Use the Model and Iterate as Necessary

By following the process we have discussed, you will define a modeling question and build a relevant model. With all of this work in place, you should be positioned to answer your question. However, previously unknown wrinkles are often discovered while working through the modeling process. Perhaps you will determine that your original modeling question was ill-posed and you need to refine your question. Or you may discover during information gathering that there are additional quantities of interest that you should consider.

**You should expect to iterate on any and all pieces of the modeling process.**

The steps in this process are not simply boxes to check in a linear process but rather broad areas of activity that you should expect to visit and revisit. Often, practical time constraints will factor into deciding when to stop, but ideally the process ends when your certainty in the model's answer is sufficient for the modeling question.

```{tip} **Avoiding "Paralysis by Analysis."**
Analysis is useful for overcoming the limitations of intuitive decision-making, but it can also lead to decision paralysis. It can be helpful to recognize when a lack of analysis is *not* the problem in an organization; instead, a "softer" approach (open dialogue with disagreeing parties) is necessary {cite}`langley1995between`. Langley reviews a variety of ways that organizations can become paralyzed by analysis---and ways to prevent them.
```
