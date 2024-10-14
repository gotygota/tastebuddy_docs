# Tasting protocols

!!! tools "Work in progress"
    This site is still under construction. Please come back later for further
    information and documentation.

## Overview

Last building block of sensory evaluation, the tasting sheet or tasting grid
defines the set of criteria the assessment should focus on. The creation of a
tasting protocols can be divided in two steps (plus one extra optional):

1. Creation of **tasting criteria**: these are the characteristics to which the
   tasters will assign a score;
2. Creation of the **tasting sheet** or **tasting grid**: combining the previsouly
   created criteria, a tasting grid will be available for both one-off tastings
   and tasting sessions;
3. (optional) Creation of a **tasting session**: by combining [the products to
   be tasted](products.md), a tasting sheet and assigning users, it allows for
   the comparative tasting of a series of products.

Note that `Regular Users` cannot create their own tasting criteria, sheets or 
sessions.
## Tasting criteria

### Definition
Tasting criteria are the characteristics that the tasters will score when
evaluating samples. They are usually grouped by category, such as nose or
palate, but any category can be created to suit specific applications. Tasting
criteria can be used in multiple tasting grids. They are not independant of the
product type and can be used for both wine and spirits (see [the tasting grid
section below](protocols.md#tasting-grid).

<div class="grid cards" markdown>

-   :material-file-edit:{ .lg .middle} __Criterion__{ .xl .middle }

    ---

    A criterion takes the following attributes:
    
    :octicons-triangle-right-24: **Name**

    :octicons-triangle-right-24: **Category**: _used to group criteria according to a common characteristic, such as nose or palate for example_;

    :octicons-triangle-right-24: **Description** (optional): used to provide a help text on the tasting sheet regarding the definition of the criterion.

    :octicons-triangle-right-24: **Scoring scale**: takes a minimum score, a maximum score, and steps between the two extremes which will build the scores available to the tasters. For
example, a scale from 1 to 10 by steps of 1 will allow tasters to chose any
score in the range 1, 2, 3, 4... 10.

</div>

### Adding a criterion
To create a new tasting criterion, go to [https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/)
 or click on `Protocols` in the left side bar or top right menu, and click on 
`+ Add criterion` above the top-most table.

<figure markdown="span">
![Criterion creation](images/criteria_creation.png#only-light){ loading=lazy }
![Criterion creation](images/criteria_creation_dark.png#only-dark){ loading=lazy }
</figure>

<figure markdown="span">
![Criterion creation](images/criteria_creation_2.png#only-light){ loading=lazy, width="80%" }
![Criterion creation](images/criteria_creation_2_dark.png#only-dark){ loading=lazy, width="80%" }
</figure>

For example, a criterion defined as:

```
- Category: Nose
- Name: Expressiveness
- Description:
    Does the spirit clearly show identifiable characteristics for the individual
    category? Are the raw materials, production techniques and product provenance
    easily recognizable?
- Lowest score: 1
- Highest score: 10
- Steps: 1
```

will render on the tasting sheet as:
<figure markdown="span">
![Criterion example](images/criterion_example.png#only-light){ loading=lazy }
![Criterion example](images/criterion_example_dark.png#only-dark){ loading=lazy }
</figure>

### Notes
!!! warning "Updating criteria"
    While criteria can be updated at any time, it is good practice to avoid changing
    the scoring scale and instead create a new criterion if it has already been used
    in a sensory evaluation to avoid comparing products that have not been evaluated
    with exactly the same protocol.

    In the backend, even though the score relative to the scale and the scale itself
    are stored in the database at the moment the sensory analysis results are
    submitted, if the criterion is changed, the system will allow the comparison of
    products that may have used different scales.

!!! info "Defining the scoring scale"
    By setting different maximum and minimum scores for different criteria, the
    importance of the criteria can be weighted. Higher available scores for a given
    criterion result in a greater influence on the total score for that criterion.
    However, some of the analyses (in particular the Principal Component Analysis on
    criteria) are performed on the value of the scores relative to their maximum,
    and for easier reading of some of the charts (such as the radar charts) they are
    also sometimes normalised to a scale from 0 to 1.

!!! tip "Avoid middle ground"
    A usual recommandation when defining a scoring scale for sensory evaluation is
    to not allow for the selection of the exact center. Avoid leaving the
    possibility to assign a score exactly in the middle of the maximum and minimum,
    to force the assessors to chose a side. For example, avoid fixing scoring scales
    like `[1, 2, 3, 4, 5]` (where 3 is the exact center). Instead, set the scale such
    as `[1, 2, 3, 4]` or `[1, 2, 3, 4, 5, 6]`. This way assessors will have to chose
    either below or above the mean of the scale.

## Tasting grid
### Definition
Tasting grids or tasting sheets are the combination of tasting criteria use to
evaluate a sample. Tasting sheets can be created specifically for wine or
spirits, or be used for both.

A tasting grid can then be used by all the users in your organisation for
one-off or punctual tastings (with direct creation of a product in the database)
or assiciated with an ordered list of samples for comparative tastings.

<div class="grid cards" markdown>

-   :material-form-select:{ .lg .middle} __Tasting grid__{ .xl .middle }

    ---

    A tasting grid takes the following attributes:
    
    :octicons-triangle-right-24: **Name**

    :octicons-triangle-right-24: **Product type**: _whether the tasting sheet can be used to assess wines, spirits or both (default to both)_;

    :octicons-triangle-right-24: **Comments**: _whether tasters can add comments (i.e. tasting notes) per criterion, per category of criteria, a single overall tasting note only or none at all (default to per category)._;

    :octicons-triangle-right-24: **Description** (optional): used to provide a help text at the top of the tasting sheet.

    :octicons-triangle-right-24: **Ordered list of criteria**: _the list of criteria to be combined for full evaluation of sample_.

</div>

### Adding a tasting sheet

To create a new tasting sheet, go to [https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/)
 or click on `Protocols` in the left side bar or top right menu, and click on 
`+ Add tasting sheet` above the second table.

<figure markdown="span">
![Sheet creation](images/sheet_creation.png#only-light){ loading=lazy }
![Sheet creation](images/sheet_creation_dark.png#only-dark){ loading=lazy }
</figure>

<figure markdown="span">
![Sheet creation](images/sheet_creation_2.png#only-light){ loading=lazy, width="80%" }
![Sheet creation](images/sheet_creation_2_dark.png#only-dark){ loading=lazy, width="80%" }
</figure>

