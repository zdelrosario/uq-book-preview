(02-modeling-process)=
# The Modeling Process

This chapter introduces a general *modeling process*. Much of the real work of modeling does not involve manipulating equations or running simulations, but rather focuses on broader critical inquiry. The modeling process presented here is focused on posing and answering scientific questions within a chosen context.

## Start With a Modeling Question

Scientific modeling is done in support of answering some form of *question*. Some examples of modeling questions include: "How can we make this design safe?" "What will the global mean temperature be in the year 2100?" "Do we need this assumption to explain this observed phenomenon?"

To help steer modelling, it is helpful to first understand what sort of question we are asking. The framework below categorizes such questions based on the *kind* of action we will take based on the model, and the *degree of specificity* in our question. While these axes are in reality continuous, it is useful to sketch some discrete cases, shown in the table below.

```{margin}
We are grateful to colleagues at Olin College, where the faculty developed a three category framework---explanation, prediction, design---which heavily influenced the framework here.
```

| **No Action** | **Indirect Action** | **Direct Action** |              |
|---------------|---------------------|-------------------|--------------|
|               | Prediction          | Detail Design     | **Specific** |
|               | Explanation         | Conceptual Design | **General**  |
| "School"      | "Analysis"          | "Design"          |              |

### Types of Action

*No action* means nothing will be done with the results of the modeling question. This is not common in research or in industry, but is an essential part of the learning process: Students first learning to pose scientific questions and to build models must start with simplified problems, and it is highly unlikely they will take action on these basic modeling efforts.

*Indirect action* refers to the modeler's efforts to influence others' actions. The modeler will not be taking direct action based on the model's results, but will instead attempt to influence the actions of others. This is often done in research, where a researcher publishes a paper explaining a specific phenomenon with the intent of inspiring other researchers to build on their ideas. This is also done in the policy space, where modelers predict the potential outcomes for different policy choices, with the aim of informing and influencing decision makers.

Finally, *direct action* refers to the modeler (or modeling team) taking action on their own. In industry, designers with the power to make decisions use models to inform their decisions. The distinction between detailed and conceptual design then hinges on the specificity of questions designers are posing.

```{admonition} Action and Consequence
Different kinds of action carry with them different consequences. Direct action obviously carries direct culpability; an engineer who makes a faulty design decision carries the responsibility when that system fails. A negligent engineer will face reputational and financial damage as a consequence of their faulty actions.

However, indirect action still carries consequences: Creating a financial model that leads others to make unsound investment decisions may not wreck your own finances, but it can cause suffering for millions of others. Cathy O'Neil {cite}`oniel2016weapons` writes in *Weapons of Math Destruction* about her dillusionment with mathematical modeling in the financial sector, where "people had deliberately wielded formulas to impress rather than clarify." This kind of modeling opacity contributed to the 2008 financial collapse.

When modeling to support direct action, it is important to carry out your work with integrity. When modeling to support indirect action you must do the same, but with the added responsibility to *communicate clearly and effectively*.
```

### Specificity of question

A *specific* question concerns a particular scenario, while a *general* question deliberately neglects these specifics. For instance, a detailed design must include detailed drawings: a style of technical communication that specifies the dimensions and tolerances for all components in a system. Such a task is necessary but extremely laborious; modeling cannot be done at the detailed level throughout the entire design process. Therefore, engineering design first passes through a conceptual design phase: In conceptual design, a far more coarse description of the system is articulated, and consequently the questions posed and models used are far more general {cite}`pahl2007,keane2005computational`.

Specificity is not an absolute, but rather a relative, discipline-specific notion. In engineering design, the highest level of detail is a full geometric and material specification of a system. However, in climate modeling, it is simply not possible to produce a full geometric representation of the Earth (including every tree, every blade of grass, etc.). Furthermore, it is not *necessary* to seek this level of detail in a climate model, as an engineering-level of geometric detail would be wasted effort in a climate modeling context.

```{admonition} Specificity and Certainty
By their nature, questions with different levels of specificity require different levels of certainty. Conceptual design of an aircraft explicitly acknowledges that low-level details about the aircraft are not yet available, so a fully-accurate prediction of performance is not feasible. Performance assessments for a detailed design are held to a much higher standard of predicted performance, as these predictions will be used to tune the design to meet performance goals and safety requirements. This difference is one in acceptable *certainty* for the question at hand, with greater specificity enabling greater certainty.

However, high specificity by itself does not imply that the appropriate level of certainty must be strict. The required level of certainty is also affected by the *consequences* of making an incorrect decision, as we will see below.
```

### Example modeling questions

To illustrate the modeling question framework and the diversity of potential modeling questions, we provide a few example modeling questions here.

#### Explanation : Indirect Action, General

In the 1990's, HIV/AIDS was an under-researched disease. Patients with the disease were observed to experience a spike in the number of viral particles in their body, with a subsequent sharp decrease in viral particles as the disease transitioned to an inactive period. It was assumed that this decrease was due to an immune response to the virus. However, in 1996 Andrew Phillips {cite}`phillips1996reduction` presented a model for viral population dynamics that replicated the observed "spike" in viral particles, but that did not include any specific immune response. This questioned the prevailing assumptions in the HIV/AIDS research community, and raised new questions for future research.

Note that the modelling work of Phillips did not attempt to make a patient-specific prediction, and yet this work was published in the journal *Science*. In this case, the modeling question was very general: is it *possible* to explain the reduction in viral particles without a specific immune response? Despite its generality, this question was of great interest to HIV/AIDS researchers.

This work explicitly neglected known details about reality (specific immune responses) as a core feature of the modeling work. This example illustrates that modeling is not simply an exercise in adding complexity, or even an attempt to represent all aspects of reality in the model. Instead, it is process that must be anchored in the modeling question that one seeks to answer.

#### Prediction : Indirect Action, Specific

```{margin} "Prediction question" vs. the general act of prediction
Note that we use "prediction question" to describe a type of modeling question, not to speak of the general act of prediction. Any form of modeling will include some type of prediction, but we use the term *prediction question* to refer to a modeling question that is aimed at a specific scenario, and designed to support indirect action.
```

The National Environmental Policy Act (NEPA) requires Federal agencies to engage in an environmental review process when making decisions {cite}`NEPAguide`. Federal agencies prepare an environmental impact statement (EIS) predicting the specific impacts of proposed actions on the environment. Since these impacts are often stated in quantitative terms, such as tons of emissions, quantitative modeling is often used to answer questions such as "How much will this action reduce annual emissions?"

As a specific example, we consider the final EIS of the Vineyard Wind 1 Offshore Wind Energy Project {cite}`eis20210028`. This study considered the various environmental impacts of a proposed offshore wind energy farm, attending to the specific geographic layout of the proposed generators. This EIS includes numerical predictions of the reduction in annual pollutants, such as carbon dioxide. These analyses were carried out across different proposed configurations, in order to support other decision-makers in choosing the final wind farm design.

Notably, an analysis of incomplete or unavailable information is required when conducting an environmental review: The Vineyard Wind 1 EIS details this in Appendix H {cite}`eis20210028`. For instance; this EIS acknowledges that a detailed emissions inventory over a 30 year period was not conducted. This lack of analysis leads to increased uncertainty about the project outcomes; however, the authors note that such uncertainty is tolerable for decision-making, as all of the proposed project options would work to *improve* air quality. Since this source of uncertainty would not affect the decision process, a more detailed analysis was not necessary.

#### Conceptual Design : Direct Action, General

Engineering design passes through multiple phases, progressing from greater to lesser uncertainty in the design. Theorists of design commonly define at least two distinct phases of *conceptual design* and *detail design* {cite}`pahl2007,keane2005computational,torenbeek1982synthesis`. These phases are distinct in their goals, hence distinct in their tools and fidelity of modeling. Engineering firms will take direct action on these design activities.

Within aircraft design, the conceptual design phase is aimed at answering a single question, "Is there a business case for this proposed aircraft?" {cite}`keane2005computational`. All major subsystems of the aircraft are considered in conceptual design {cite}`torenbeek1982synthesis`, but at a low-level of fidelity. For instance, while a real aircraft will include millions of parts, conceptual designers may use a quantitative model for the wing system with as few as $11$ variables {cite}`keane2005computational`. In this sense, the modeling of the aircraft is more general than specific.

Aircraft conceptual design does not typically use first-principles (physics-based) models to guide decisions; rather, empirical models are typically used {cite}`keane2005computational`. This is sensible, based on the driving question. The level of fidelity necessary to use the appropriate physics-based models would require an enormous investment of engineering time. Rather than seek model complexity for its own sake, aircraft designers at the conceptual phase deliberately work with lower-fidelity models to make the business case for a conceptual design. If the proposed concept is promising, the next action is to proceed to detail design.

#### Detail Design : Direct Action, Specific

The detail design phase is the last of the engineering design process {cite}`pahl2007`. At this stage, the goal is a completely-specified product {cite}`keane2005computational`; this will involve thousands of sub-questions, such as "What is an appropriate thickness for this structural member?"

Within aircraft design, the detail design phase involves heavy use of computer-aided design (CAD) tools and physics-based simulations of physical performance {cite}`keane2005computational`. Subsystems such as the airplane wing must be fully defined: While in conceptual design the wing may have been defined in terms of a dozen variables (e.g. span, mean thickness, taper ratio), the wing detail design must specify the precise dimensions of every part. In this sense, the detail design is far more specific than the conceptual design.

At the detail design phase, uncertainties such as the variability in material properties or the uncertainties in external loads must be properly factored into design. Variability in material properties is treated in aerospace engineering through the use of *allowable values* {cite}`zdr2021allowables`; *usually* conservative values for material properties that have some affect on adverse failure modes, such as the yield of structural members. Uncertainties in external loads are treated using factors of safety; however, these factors are often based on historical decisions and have no rational basis {cite}`meyer-jens1978agard661`.

## Choose Quantities of Interest (QOI)

After formulating our modeling question, we must pick *quantities of interest* (QOI) to help operationalize our question. A QOI should be some quantity that has relevance to the question we are trying to solve: Some examples include the trajectory of a projectile, the percent yield of a manufacturing process, the count of some cell in a body. Sometimes a QOI will be quite complicated; note that the a trajectory of a projectile is a curve through space and time. Often we need to define *metrics* to reduce a complicated QOI to a simpler quantity. For instance, we can summarize a projectile trajectory by considering its range; that is, the horizontal distance at which the projectile hits the ground.

Sometimes the appropriate QOI will seem clear; the HIV/AIDS explanation question above is obviously concerned with a count of viral particles. However, even in such "obvious" cases there are important decisions to be made; are we talking about the total count of viral particles in the entire body? Or will a small representative volume of tissue suffice? You can only make this kind of decision by carefully considering your modeling question.

More subtly, assumptions about human values are encoded in your choice of quantities of interest {cite}`saltelli2020five`. For instance, profit is often taken as the sole QOI for businesses, but this neglects other factors we would want to promote in society, such as the well-being of people and the sustainability of the planet. Alternatives to a profit-only quantification of business success include the *triple bottom line* concept {cite}`slaper2011triple`, which quantifies social and environmental impact along with profit.

```{admonition} The dangers of quantification
:class: warning
In their modeling manifesto, Andrea Saltelli and others {cite}`saltelli2020five` warn that "Once a number takes centre-stage with a crisp narrative, other possible explanations and estimates can disappear from view." While modeling quantities of interest and computing metrics are useful for addressing a question, keep in mind that important factors in any situation can be difficult to quantify, and thus include in a model. Make sure when you model to keep in mind the limitations of your approach; particularly what is *not* represented in your model.

As we'll see below, model assessment can help to surface the limitations of your model.
```

## Gather Appropriate Information

Physical principles can be used to build a mathematical model to predict quantities of interest. For instance, principles from Newtonian mechanics can be used to study the motion of a projectile. To support building the model, we could build an inventory of forces that act on our projectile, and search for existing models that other researchers have used for similar problems.

Through searching for relevant physical principles, we are likely to come across *model parameters* whose numerical values we will need to set in our model. For instance, a projectile will be affected by its mass, initial velocity, and aerodynamic drag characteristics. Depending on the projectile and the specificity of our modeling question, we may need to consider additional factors, such as the spin of a baseball or its surface geometry.

```{margin}
Note that the term "parameter" is used differently across disciplines. "Parameter" to a scientist or engineer follows the definition of "model parameter" we see above; a quantity that enters a model. However a "parameter" to a statistician refers more specifically to a deterministic quantity that describes the properties of a random variable. We will see this statistical definition in the [chapter on distributions](02-distributions).
```

Model Parameter
: A *model parameter* is a quantity (numerical, categorical, or otherwise) in a model that must be set to some value in order to use that model.

Note that we are likely to find a range of possible parameter values, or possibly repeat measurements that point to variability in the parameter values. This information is important to collect, as we will use this information to build a [distribution](02-distributions) representation of uncertainty.

In some cases, there will not be sufficient physical theory to describe all of the physical phenomena using a first-principles approach. In these cases, one can use a particular form of data to build an *empirical* model: Repeated observations on parameters and output quantities can enable statistical modeling of the observed phenomena. If an empirical approach is necessary, then it will be necessary to obtain and curate such a dataset before moving on to building the model.

## Build the Model

With the principles and data gathered above, we can then build the model. As noted in the [Orientation Chapter](01-orienting), we assume that you have the skills to implement domain-specific *deterministic* models from your own discipline: This will involve using physical principles to write down a mathematical model, then using a programming language to implement that model as computer code. Your deterministic models should be able to map between some input model parameters and the output quantities of interest that you seek to study. The remainder of this book is about a set of tools and understanding to complement your existing domain-specific modeling skills with rigorous tools to handle uncertainty. We will use the [py-grama](01-grama-intro) package to implement these ideas.

As noted in the [introduction to Grama](01-grama-intro), a Grama model contains information about the inputs and the map between inputs and outputs. We will use *distributions* in our models to represent uncertainty in model parameters. We will also fit *empirical* (data-driven) models to "fill the gaps" when physical principles alone are insufficient to predict our desired quantities of interest. The next part of this book---[Developing](02-developing)---will cover these ideas in detail.

```{admonition} "Everything must be made as simple as possible, but no simpler."
:class: warning
This famous quote by Albert Einstein is a central tenet in modeling: Resist the urge to add complexity for complexity's sake. All complexity in a model must be justified as necessary to answer the modeling question.
```

## Assess the Model

While we make use of curiosity and skepticism throughout the modeling process, assessing the model is where we formally deploy mathematical techniques to put skepticism into practice. Model assessment should include two key steps: *verification* and *validation*. We use the AIAA definitions of verification and validation, stated below {cite}`aiaa1998vnv`:

Verification
: The process of determining that a model implementation accurately represents the developer's conceptual description of the model and the solution to the model.

In order to check that we have implemented the model in code correctly, it is important to "stress test" the code to check for correctness. The specific mechanics of verification vary based on the type of model and implementation, thus a comprehensive treatment of all verification approaches is beyond the scope of this book. However, some general principles apply: When carrying out a verification study, it is important to check *emergent* behavior of the model, rather than manually-enforced properties of the model. For instance, in a trajectory prediction code, it would *not* be a rigorous verification exercise to simply check that the parameter values of the model are set to the correct values. Instead, it would be a useful verification step to check that the code-generated solution to the model matches a hand-calculated trajectory. A more general approach to this form of correct-solution generation is the *method of manufactured solutions* {cite}`roache2002code`, often used for testing simulation codes for partial differential equations.

While verification checks that the model is implemented correctly, it is also key to check that the model is an accurate representation of reality.

Validation
: The process of determining the degree to which a model is an accurate representation of the real world from the perspective of the intended uses of the model.

Note that the definition of validation explicitly references the "intended uses of the model"; it is commonly accepted that the accuracy of a model can only be assessed *in the context of an intended use*. This means we must have our modeling question in mind when designing and executing a validation study. A modeling question requiring specific, detailed predictions should involve a validation exercise that tests for the necessary level of accuracy. For instance, when designing a bridge, it is clear that a high level of confidence is needed in the specific numerical predictions of load capacity and resilience of the structure.

However, validation need not involve a direct comparison of model results to data. For instance, note that in the HIV/AIDS example mentioned above {cite}`phillips1996reduction`, the author did not carry out any explicit comparison of simulated viral particle counts against measured clinical data. Instead, the author built upon previously published models---establishing credibility based on starting from accepted models---and compared the results *qualitatively* to observed clinical trends. While this sort of validation would not be appropriate for supporting bridge design, since the author's modeling question was quite general, this style of validation was appropriate for the intended use of the model.

Finally, note that even a properly validated model is not "proven" to be correct! Validation builds confidence in the model for the tested scenario, but there is always danger in extrapolating to an unseen scenario. The problem of induction {cite}`popper2005logic` is an inherent limitation in the practice of science, meaning we should always maintain a bit of healthy skepticism towards any model!

```{admonition} A helpful mnemonic
It is often said that verification is an exercise in mathematics & coding, while validation is an exercise in physics. It can be helpful to note that verifi`c`ation is about the `c`ode used to implement the model, while vali`d`ation often involves comparing model results against physical `d`ata.
```

We will see many examples of validation in the following parts of the book: [Developing](02-developing) and [Answering](03-answering).

### How much certainty is needed?

In discussing validation, we saw that different levels of accuracy are needed for different types of modeling question: Clearly a general question does not need the same level of accuracy as a specific question. Related to accuracy is the concept of *certainty*.

While we will discuss [uncertainty](02-uncertainty) more formally in a later chapter, it is worth noting here that the level of certainty necessary to answer a modeling question depends on more than just the specificy of the question. Here we discuss a few questions to ask yourself to help determine how much certainty is needed.

```{margin}
The idea that certainty ought to vary based on the context is as old as Aristotle, see e.g. 1098a {cite}`rackham1934ne`.
```

**What are the consequences of making an incorrect conclusion?** If the consequences are innocuous---say, yours is a proof-of-concept effort---then a great deal of certainty is not needed. The HIV/AIDS example we saw above sought to provide a potential explanation for observed phenomena, and suggested further work. An incorrect conclusion in that example might mean contradictory evidence would be found that refuted the original study: This would still be a net win for the scientific community. However, a model aimed at making patient-specific predictions for surgical decisions would obviously have greater consequence. These higher consequences would demand a higher level of certainty.

```{admonition} Analogy: The Legal System
:class: tip
In the United States legal system, there exist different "standards of proof"---codified levels of certainty. These standards are used for different types of legal cases, carrying different consequences. For instance; the highest standard "beyond reasonable doubt" is reserved for criminal cases, where the liberty of an individual is at stake {cite}`black1968law`. For civil cases the consequences involve financial damages; these relatively lower-stakes mean a lower standard of certainty is used: "preponderance of the evidence" (colloquially, "more probable than not") {cite}`black1968law`.
```

**What have we learned so far?** It is rare to be able to state a specific, numeric level of required certainty for a given modeling question *a priori*. More frequently, you will discover a lack of certainty through the modeling process. At this point, you will likely need to gather more information (to reduce uncertainty) or change your modeling question (to acknowledge limitations). It is worth keeping in mind that modeling is an iterative process, as we'll discuss further below.

**Do you have an answer?** Sometimes in evaluating the certainty necessary for a particular question, you may find that the present uncertainty is intolerable because you simply do not have the means to answer the question. In these cases, you should be honest with yourself and any stakeholders; as Saltelli et al. {cite}`saltelli2020five` write in their *modeler's manifesto*, "Experts should have the courage to respond that 'there is no number-answer to your question'."

## Use the Model, Iterate as Necessary

Through following the process above, you will define a modeling question along with a relevant model. With all of this work in-place, you should be positioned to answer your question. *However*, it is common to discover previously unknown wrinkles while working through the modeling process. Perhaps you will determine that your original modeling question was ill-posed: that you need to refine your question. Or you may discover during information gathering that there are additional quantities of interest that you should consider.

**You should expect to iterate on any and all pieces of the modeling process.**

The steps in this process are not simply boxes to check in a linear process, but rather broad activity areas that you should expect to visit and revisit. Often, *practical time constraints* will factor into deciding when to stop, but ideally the process ends when your certainty in the model's answer is sufficient for the modeling question.
