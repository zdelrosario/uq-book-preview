# Types of Modeling Questions

---

Scientific modeling is done in support of answering some form of *question*. To help steer this process, it is helpful to organize modeling questions into three broad categories: *explanation*, *prediction*, and *design*[^modsim].

## Explanation

- Can we provide a plausible explanation for some observed phenomenon?
- Uncertainty matters because: Any model requires a set of assumptions, and a reasonable peer review will question those assumptions. Explicitly accounting for uncertainty helps build confidence that the author did not cherry-pick assumptions to match their desired conclusion.
- Example: Explanation of the "crash" in count of a particular cell during HIV infection counter to the prevailing explanation at the time {cite}`phillips1996reduction`.

## Prediction

- Can we predict an unobserved phenomenon?
- Uncertainty matters because: No prediction will be 100% accurate; providing uncertainties associated predicted quantities will allow decision makers to plan accordingly. Furthermore, quantitatively attributing uncertainty in the output to the various inputs will guide the collection of future data, allowing for systematic and principled reduction of uncertainty.
- Example: Climate change (includes both bounds and different scenarios)

## Design

- Can we interfere with a scenario to produce a desired outcome?
- Example: Aircraft design; manufacturing variability and high-consequence failures means uncertainties cannot be ignored

## Check the context

What are the consequences to making an incorrect conclusion?
- If the consequences are innocuous, then a relatively simple model may be sufficient.
  - Explanation tends to be provisional, as it merely aims to provide a plausible answer.
  - A first-pass prediction or proof-of-concept prediction will tend to be rough in nature. If future modeling efforts are assumed to follow---and the rough prediction will not used for critical decisions---then a simple model may suffice. Note that the general public does not tend to appreciate this nuance!
  
- If there are important consequences, then you need to be appropriately cautious in your methods.
  - Early comparative design decisions will be followed up with more detailed analysis. Modeling should be detailed enough to factor in the relevant aspects and support comparison, but not so detailed as to lead to "analysis paralysis." *TODO* citation needed
  - Predictions that will be released to the public should be treated as high-consequence: *TODO* {cite}`oniel2016weapons`.
  - Design of a safety-critical system should be designed using the accepted best-practices in your field. For instance: Determination of allowable properties for aerospace materials follows a very formal distribution testing procedure {cite}`MMPDS`.

[^modsim]: I am indebted to my colleagues at Olin College, where the faculty have developed this three category framework in the first year course *Modeling and Simulation of the Physical World*.