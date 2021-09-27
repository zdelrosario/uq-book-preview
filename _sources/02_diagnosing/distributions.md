(02-distributions)=
# Distributions

This chapter is on *distributions*, a quantitative way to represent uncertainty. 

## Two Contexts

To ground this chapter, we will compare and contrast two case studies:

### Context One: Materials Selection

- Objective: Choose one material among several for a structural application (design question)
- Consequences:
  - A poor early choice will lead to an underperforming design
  - Early decisions will lead to future investments, sinking cost into the given choice
  - Hard-to-quantify factors (such as manufacturability) may cause future economic headaches
  
| Materials  |
|------------|
| Al 2024-T3 |
| Al 7075-T6 |
| Al 6061-T6 |
| Fe 1040    |
| Ti 6Al 4V  |

### Context Two: Structural Sizing

- Objective: Choose a size for a structural component (design question)
- Consequences:
  - An oversized component will be too heavy, leading to a non-competitive design
  - An undersized component will be unsafe, leading to dangerous failures
  
A lower *realized* strength value is *more unsafe*; the part in question can handle less of a load.

A lower *assumed* strength value is *more safe*; we will offset a lower strength by building a larger structure, leading to a generally safer design.

To illustrate doing analysis and making decisions in this context, we will use the [cast steel dataset](app-steel).
