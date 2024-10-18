# Tasting protocols

## Overview

Last building block of sensory evaluation, the tasting sheet or tasting grid
defines the set of criteria the assessment should focus on. The creation of a
tasting protocol can be divided in two steps (plus one extra optional):

1. Creation of **tasting criteria**: these are the characteristics to which the
   tasters will assign a score;
2. Creation of the **tasting sheet** or **tasting grid**: combining the previously
   created criteria, a tasting grid will be available for both one-off tastings
   and tasting sessions;
3. (optional) Creation of a **tasting session**: by combining [the products to
   be tasted](products.md), a tasting sheet and assigning users, it allows for
   the comparative tasting of a series of products simultaneously.

Note that `Regular Users` cannot create their own tasting criteria, sheets or 
sessions.
## Tasting criteria

### Definition
Tasting criteria are the characteristics that the tasters will score when
evaluating samples. They are usually grouped by category, such as nose or
palate, but any category can be created to suit specific applications. Tasting
criteria can be used in multiple tasting grids. They are independent of the
product type and can be used for both wine and spirits (see [the tasting grid
section below](protocols.md#tasting-grid)).

<div class="grid cards" markdown>

-   :material-puzzle-plus-outline:{ .lg .middle} __Criterion__{ .xl .middle }

    ---

    A criterion takes the following attributes:
    
    :octicons-triangle-right-24: **Name**

    :octicons-triangle-right-24: **Category**: used to group criteria according to a common characteristic, such as nose or palate for example;

    :octicons-triangle-right-24: **Description** (optional): used to provide a help text on the tasting sheet.

    :octicons-triangle-right-24: **Scoring scale**: takes a minimum score, a
    maximum score, and steps between the two extremes which will build the scores
    available to the tasters. For example, a scale from 1 to 9 by steps of 2 will 
    allow tasters to chose any score in the range 1, 3, 5, 7, and 9.

</div>

!!! info "Just About Right"
    Wines and spirits are usually rated according to a set of selected criteria to
    which a rating scale is assigned. The rating scale is usually not used as an
    {--intensity--} scale, but as a {++"just about right"++} scale. The maximum score therefore
    corresponds to the exact expected expression of the criterion in question.

    For example, you might rate the sweetness of a particular product. In this case,
    a scale of 1 to 10 should not be understood as

     from ```1: not sweet at all``` to ```10: excessively sweet ```

    but as

     from ```1: too sweet or not sweet enough``` to ```10: perfectly sweet ```
### Adding a criterion
To create a new tasting criterion, go to
[https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/) or click on
`Protocols` in the left side bar or top right menu :material-view-grid:, and
click on `#!yaml + Add criterion` above the top-most table.

=== "Access"

    <figure markdown="span">
    ![Criterion creation](images/criteria_creation.png#only-light){ loading=lazy }
    ![Criterion creation](images/criteria_creation_dark.png#only-dark){ loading=lazy }
    </figure>

=== "Creation form"

    <figure markdown="span">
    ![Criterion creation](images/criteria_creation_2.png#only-light){ loading=lazy, width="400", align=left }
    ![Criterion creation](images/criteria_creation_2_dark.png#only-dark){ loading=lazy, width="400", align=left }
    </figure>

For example, a criterion defined as:

``` yaml
- Category: Nose
- Name: Expressiveness
- Description:
    Does the spirit clearly show identifiable characteristics for... # (1)
- Lowest score: 1
- Highest score: 10
- Steps: 1
```

1.  ...the individual category? Are the raw materials, production techniques and product provenance
    easily recognizable?

will render on the tasting sheet as:
<figure markdown="span">
![Criterion example](images/criterion_example.png#only-light){ loading=lazy }
![Criterion example](images/criterion_example_dark.png#only-dark){ loading=lazy }
</figure>

### Notes
!!! warning "Updating criteria"
    While criteria can be updated at any time, it is good practice to avoid changing
    the scoring scale and instead create a new criterion if it has already been used
    in a sensory evaluation, to avoid comparing products that have not been evaluated
    with exactly the same protocol.

    In the backend, although the score relative to the scale and the scale itself
    are stored in the database at the moment the sensory analysis results are
    submitted, if the criterion is changed, the system will allow the comparison of
    products that may have used different scales.

!!! info "Defining the scoring scale"
    By setting different maximum and minimum scores for different criteria, the
    importance of the criteria can be weighted. Higher available scores for a given
    criterion result in a greater influence for that criterion on the overall
    evaluation. However, some of the analyses (in particular the Principal Component
    Analysis of the criteria) are performed on the value of the scores relative to
    their maximum (i.e. without taking into account the importance given to the
    criteria on the overall evaluation), and to make some of the charts (such as
    the radar charts) easier to read, the scores are sometimes normalised to a scale
    of 0-1.

!!! tip "Avoid middle ground"
    A common recommendation when defining a scoring scale for sensory evaluation is
    not to allow the choice of the exact centre. Avoid leaving the possibility of
    assigning a score exactly in the middle of the maximum and minimum to force the
    evaluators to choose a side. For example, avoid setting scoring scales such as
    `[1, 2, 3, 4, 5]` (where 3 is the exact centre). Instead, set the scale like `[1,
    2, 3, 4]` or `[1, 2, 3, 4, 5, 6]`. This way the raters have to choose either below
    or above the mean of the scale.

## Tasting grid
### Definition
Tasting grids or tasting sheets are the combination of tasting criteria used to
evaluate a sample. Tasting grids can be created specifically for wines or
spirits, or can be used for both.

A tasting grid can then be used by all users in your organisation for one-off
or punctual tastings (with direct creation of a product in the database), or
associated with an ordered list of samples for comparative tastings.

<div class="grid cards" markdown>

-   :material-order-bool-descending:{ .lg .middle} __Tasting grid__{ .xl .middle }

    ---

    A tasting grid has the following attributes:
    
    :octicons-triangle-right-24: **Name**

    :octicons-triangle-right-24: **Product type**: _whether the tasting sheet can be used to rate wines, spirits or both (default to both)_;

    :octicons-triangle-right-24: **Comments**: _whether tasters can add comments (i.e. tasting notes) per criterion, per category of criteria, only a single overall tasting note or none at all (default to per category)_;

    :octicons-triangle-right-24: **Description** (optional): used to provide a help text at the top of the tasting sheet.

    :octicons-triangle-right-24: **Ordered list of criteria**: _the list of criteria to be combined for a complete score of the sample_.

</div>

### Adding a tasting sheet

To create a new tasting sheet, go to [https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/)
 or click on `Protocols` in the left sidebar or top right menu, and click on 
`+ Add Tasting Sheet` above the second table.

=== "Access"

    <figure markdown="span">
    ![Sheet creation](images/sheet_creation.png#only-light){ loading=lazy }
    ![Sheet creation](images/sheet_creation_dark.png#only-dark){ loading=lazy }
    </figure>

=== "Creation form"

    <figure markdown="span">
    ![Sheet creation](images/sheet_creation_2.png#only-light){ loading=lazy, width="80%" }
    ![Sheet creation](images/sheet_creation_2_dark.png#only-dark){ loading=lazy, width="80%" }
    </figure>

On the newly opened page, enter the following information:

- **Name**: _note that the name must be **unique**, i.e. if a
tasting sheet with the same name already exists, submitting the form will raise
an error_;
- **Description** (optional): a help text which will appear when selecting the
sheet for tastings;
- **Product type**: wether the tasting grid can be used for both or either of
wines and spirits (_default to both_);
- **Comments**: how often a text box should appear on the tasting sheet to allow
for tasting notes - per tasting criterion, category, only once at the bottom or
never (_default to per criterion category_)
- **Criteria list**: criteria to be assigned to the tasting sheet and
the position (i.e. the order) in which they should appear on the tasting grid.

Any number of criteria can be used (click `+ Add Criterion` to add more
fields). Only previously created criteria can be selected, and
it is not currently possible to create new criteria directly from this page. See
[Adding a criterion section above](protocols.md#adding-a-criterion).

Finally, click `Add` at the bottom right of the page to create the tasting sheet.

!!! info "Regarding tasting notes"

    ![Word cloud example](images/word_cloud.png#only-light){ loading=lazy, width="45%", align=right }
    ![Word cloud example](images/word_cloud_dark.png#only-dark){ loading=lazy, width="45%", align=right }

    The choice of `Comments` will result in a different sorting of the word
    analysis on the results dashboard. The picutre opposite shows an example of the
    resulting word analysis with comments set for each criterion category.

    Note, however, that the **comments are not made mandatory to the
    taster**. In other words, when evaluating a sample, users can leave the Note
    text box blank and still submit results. It is advisable to ask the tasters
    to do their best to be thorough in their tasting notes.


!!! tip "Ordering the criterion"
    The `#!yaml Position` field determines the order in which the criteria
    appear in the tasting grid. This order can therefore be different from the
    one that appears in the tasting sheet creation form.

    This field can take either an integer or a decimal number, positive or
    negative: the criteria can simply be labelled 1, 2, 3, ... but a new criterion
    can also be easily inserted by using a decimal number (based on the example
    above, setting a criterion with `#!yaml Position: 1.5` will give it the second
    position, even if it appears in the last position of the list on the 
    creation form).

    <figure markdown="span">
    ![Criteria order example](images/sheet_criteria_order.png#only-light){ loading=lazy, width="80%" }
    ![Criteria order example](images/sheet_criteria_order_dark.png#only-dark){ loading=lazy, width="80%" }
    </figure>

    The above example will result in the criteria appearing as:

    1. Aspect - Cleanliness
    2. Nose - Aromatic complexity
    3. Palate - Flavour complexity
    4. Overall - Balance

Tasting sheets are available to all users within the organisation for
punctual tasting (see [Using Tastebuddy](../user/tasting.md)). They can also be
combined with a product list for tasting sessions (see [the Tasting Session
section](protocols.md#tasting-session) down below).

### Updating an existing tasting sheet

Existing tasting sheets can be updated by clicking on `Edit` in the
corresponding row of the tasting grid table. Any change will be reflected in
existing results: for example, dashboards of results will show the
current name of the tasting sheet, regardless of whether the name was different 
when the results were saved.

!!! warning "Modifying the criteria"
    It is strongly discouraged to change the list of criteria on an existing grid,
    other than to rearrange them, if the grid has already been used to record the sensory
    analysis of a sample. If you do decide to do so, take extra care when
    comparing samples to ensure that they have been evaluated using the same version of the
    grid.

    In principle, adding or deleting a tasting criterion between two sensory
    evaluations is tantamount to modifying the tasting protocols, and therefore the
    comparison could become irrelevant.

## Tasting session
### Definition

A tasting session is the comparative evaluation of a number of similar products
at the same time by one or more tasters, also known as a jury panel. It allows differences between 
products to be highlighted and a ranking to be established between them.

<div class="grid cards" markdown>

-   :material-order-bool-descending:{ .lg .middle}:material-glass-wine:{ .lg .middle }:material-glass-wine:{ .lg .middle } __Tasting Session__{ .lg .middle }

    ---

    A tasting session has the following attributes:
    
    :octicons-triangle-right-24: **Name**

    :octicons-triangle-right-24: **Tasting sheet**: _the tasting grid used to evaluate each sample_;

    :octicons-triangle-right-24: **Scheduled date**: _the date from which the tasting session will be accessible to the assigned users_;

    :octicons-triangle-right-24: **Accessible for (days)**: _for how long should the session be accessible (default 7 days)_;

    :octicons-triangle-right-24: **Description**: _a description of the tasting session which appears at the top of the form to the jury_;

    :octicons-triangle-right-24: **Hide sample**: _whether the name of the samples are displayed to the tasters or not. If the switch is activated, the name of the products will be replaced by_ "Product _n_";

    :octicons-triangle-right-24: **Assigned tasters**: _the list of tasters invited to the comparative sensory evaluation_;

    :octicons-triangle-right-24: **Sample list**: _the list of sample in the order they are served_;

</div>

### Creating a tasting session

Tasting sessions are associated with product types; to create a new tasting session, go
to [https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/) or click on `#!yaml Protocols` in the left sidebar or
top right menu, and click on either `+ Create Spirits Tasting Session` or `+ Create Wine Tasting Session` above the appropriate table.

=== "Access"

    <figure markdown="span">
    ![Session creation](images/session_creation.png#only-light){ loading=lazy }
    ![Session creation](images/session_creation_dark.png#only-dark){ loading=lazy }
    </figure>

=== "Creation form"

    <figure markdown="span">
    ![Session creation](images/session_creation_2.png#only-light){ loading=lazy, width="80%" }
    ![Session creation](images/session_creation_2_dark.png#only-dark){ loading=lazy, width="80%" }
    </figure>

!!! warning "Wine VS Spirit tasting session"
    Make sure you have selected the correct product type on the Protocol page. Only the products of
    the selected product type [that have been previously created](products.md#product-creation)
    and the tasting sheets that apply to the product type in question will be 
    available in the various drop-down menus.

    In case of error, a direct link to the other product type is available at the top of the page.


<br>
On the newly opened page, enter the following information:

- **Name**;
- **Description** (optional): a description of the tasting session that will be
  displayed at the top of the page when tasters access the tasting. For example,
tips or warnings about the products can be added here;
- **Tasting sheet**: select the tasting grid that will be used to evaluate the samples.
  Only [previously created tasting sheets](protocols.md#adding-a-tasting-sheet)
  corresponding to the selected product type will appear in the drop-down menu;
- **Scheduled date**: the intended date of the tasting session, from which the
session will be accessible to the judges;
- **Accessible for**: how many days after the scheduled date the tasting
  session should be available (see note below).
- **Hide sample names**: check this box to replace the names of the samples
  with the order in which they are served;[^1]
- **Assigned tasters**: select all the users who should participate in the
tasting session;[^2]
- **Samples**: from the drop-down menu, select the samples to be added to the
tasting session and assign an order to them by filling in the `Position` field
Any number of spirits (respectively wines) can be added by clicking `+ Add spirit`
(respectively `+ Add wine`)

!!! info "About scheduled date and availability"
    Each tasting session is only accessible from its scheduled date. Although it
    appears on the home page of the assigned users from the moment it is created, the link will be closed until the scheduled date.
    The results dashboard, whether it's for a taster or for the administrators,
    will also be inaccessible until one of these two conditions is met:

    1. All assigned tasters have completed the session and submitted results;
    2. The delay specified in the `Accessible for (days)` field, calculated from
       the scheduled date, has elapsed.

    Once a taster has completed a tasting session and submitted their results,
    they won't be able to modify their records or access the tasting session anymore.

!!! tip "Ordering the samples"
    The `#!yaml Position` field determines the order in which the samples  
    appear in the tasting grid. This order can therefore be different from the
    one that appears in the tasting session creation form.

    This field can take either an integer or a decimal number, positive or
    negative: the samples can simply be labeled 1, 2, 3, ... but a new sample
    can also be easily inserted by using a decimal number (based on the example
    above, setting a sample with `#!yaml Position: 1.5` will give it the second
    position, even if it appears in the last position of the list on the
    creation form).

    <figure markdown="span">
    ![samples order example](images/sample_order.png#only-light){ loading=lazy, width="80%" }
    ![samples order example](images/sample_order_dark.png#only-dark){ loading=lazy, width="80%" }
    </figure>

    The above example will result in the samples appearing as:

    1. Peated Whisky - Peated Scotch Whisky #1
    2. Peated Whisky - Peated Scotch Whisky #2
    3. Peated Whisky - Peated Scotch Whisky #3
    4. Peated Whisky - Peated Scotch Whisky #4

### Following up the tasters progress

The progress of the assigned tasters can be followed live by the
administrators. From the [home page](https://tastebuddy.io), in the **TASTING
PROGRESS** card, click on the {++Progress++} button next to the corresponding
tasting session to display the status of all the tasters.

<figure markdown="span">
![session progress](images/session_home.png#only-light){ loading=lazy, width="80%" }
![session progress](images/session_home_dark.png#only-dark){ loading=lazy, width="80%" }
</figure>


[^1]: Note: to show the sample names in the
results dashboard, edit the tasting session after all results have been submitted
and uncheck the box;
[^2]: Currently only users with an account can be invited to a tasting session.
    Further development of TasteBuddy will open tasting sessions to _Anonymous
    users_

