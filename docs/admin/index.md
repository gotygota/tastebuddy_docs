# Administrators documentation

## Overview

In order to collect meaningful data on the sensory profile of spirits or wines
efficiently, Tastebuddy requires administrators to carefully design the tasting
process. There are three key components to this process:

- **Tasters**: they are the direct users of the application and the people who
  provide their expertise on the samples being evaluated;
- **Products**: either wine or spirits, they are the samples on which the sensory
  evaluation is performed;
- **Tasting protocols**: they define the set of criteria (and associated weights)
  on which the evaluation will focus;

!!! tip "Example protocols and products"
On account creation, a tasting protocol and example products are automatically
added for illustrative purposes. They can be safely used as is, modified or
deleted

## Getting started

Tastebuddy has been designed to give users as much freedom as possible to adapt
to a maximum number of practical use cases. Conceptually, a sensory evaluation
is based on three basic building blocks that can be combined and mixed depending
on the scenario: a set of criteria or characteristics that the sensory analysis
should focus on, assessors or tasters to provide the expertise, and of course
the sample(s) to be evaluated.

These fundamental building blocks can be created, edited or combined to achieve
a defined goal.

<figure markdown="span">
  ![Functional diagram](images/functional_diagram_2.png#only-light){ width="90%"}
  ![Functional diagram](images/functional_diagram_2_dark.png#only-dark){ width="90%"}
  <figcaption>Conceptual diagram of TasteBuddy functionning</figcaption>
</figure>

Although products can be created _on the fly_ (i.e. added directly at the time
of evaluation), careful preparation and experimental design should
be performed by the administrators before conducting any sensory evaluation.

## Definitions

The following words will be used along this documentation. Getting familiar with
the concepts will help to understand the next pages.

`Sensory evaluation` or `Tasting`

: Sensory evaluation of a product based on a pre-defined set
of criteria associated with a discrete point scale (e.g. sweet-
ness from 1 to 6, complexity from 1 to 10, etc.). Comments
from the taster can be associated with the criterion.

`Tasting criterion`

: A characteristic of a product to be rated on a discrete scale.
Usually grouped by category (e.g. nose, palate).

`Tasting sheet` or `Tasting grid`

: A set of selected criteria used during a tasting. Any number
of criteria can be used, depending on the application.

`Punctual tasting`

: Sensory evaluation of a single product by a single assessor.

`Tasting session`

: Comparative tasting of a number p of products in a predetermined order by a
number a of evaluators. The ordered list of products is called a flight. The
same tasting sheet is used for each product and by each taster; each taster must
evaluate all the samples in one go, but they do not necessarily perform the
evaluation synchronously. All products are evaluated at the same time, and it is
possible to move back and forth between samples. A tracking page is associated,
showing the progress of each associated user within the product flight.

`Dashboard`

: Collection of graphics illustrating the results of past tastings

`Product`

: Spirit or Wine on which a sensory evaluation is carried out. Sometimes referred to as a sample.

`Flight` or `Product series`

: Ordered series of products to be compared during a tasting session
