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

-   :material-puzzle-plus-outline:{ .lg .middle} __Criterion__{ .xl .middle }

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
`#!yaml + Add criterion` above the top-most table.

<figure markdown="span">
![Criterion creation](images/criteria_creation.png#only-light){ loading=lazy }
![Criterion creation](images/criteria_creation_dark.png#only-dark){ loading=lazy }
</figure>

![Criterion creation](images/criteria_creation_2.png#only-light){ loading=lazy, width="400", align=left }
![Criterion creation](images/criteria_creation_2_dark.png#only-dark){ loading=lazy, width="400", align=left }

For example, a criterion defined as:

``` yaml
- Category: Nose
- Name: Expressiveness
- Description:
    Does the spirit clearly show
    identifiable characteristics
    for... # (1)
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
Tasting grids or tasting sheets are the combination of tasting criteria used to
evaluate a sample. Tasting grids can be created specifically for wines or
spirits, or can be used for both.

A tasting grid can then be used by all users in your organization for one-time
or occasional tastings (with direct creation of a product in the database), or
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

<figure markdown="span">
![Sheet creation](images/sheet_creation.png#only-light){ loading=lazy }
![Sheet creation](images/sheet_creation_dark.png#only-dark){ loading=lazy }
</figure>

![Sheet creation](images/sheet_creation_2.png#only-light){ loading=lazy, width="52%", align=left }
![Sheet creation](images/sheet_creation_2_dark.png#only-dark){ loading=lazy, width="52%", align=left }

On the new page, enter a name (_note that the name must be **unique**, i.e. if a
tasting sheet with the same name already exists, submitting the form will raise
an error_), optionally a description, select the type of product the tasting
sheet can be used for, as well as the characteristics the comments should refer
to, if any. Finally select the criteria to be assigned to the tasting sheet and
the position or order in which they should appear on the tasting grid.

Any number of criteria can be used (click `+ Add Criterion` to add more
fields). Only previously created criteria can be selected, and
it is not currently possible to create new criteria directly from this page. See
[Adding a criterion section above](protocols.md#adding-a-criterion).

Finally, click `Add` at the bottom right of the page to create the tasting sheet.


!!! tip "Ordering the criterion"
    The `#!yaml Position` field determines the order in which the criteria  
    appear in the tasting grid. This order can therefore be different from the
    one that appears in the tasting sheet creation form.

    This field can take either an integer or a decimal number, positive or
    negative: the criteria can simply be labeled 1, 2, 3, ... but a new criterion
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

Tasting sheets are available to all users within the organization for
punctual tasting (see [Using Tastebuddy](../user/tasting.md)). They can also be
combined with a product list for tasting sessions (see [the Tasting Session
section](protocols.md#tasting-session) down below).

### Updating an existing tasting sheet

Existing tasting sheets can be updated by clicking on `Edit` in the
corresponding row of the tasting grid table. Any change will be reflected in
existing results: for example, dashboards of existing results will show the
current name of the tasting sheet, regardless of whether the name was different 
when the results were saved.

!!! warning "Modifying the criteria"
    It is strongly discouraged to change the list of criteria on an existing sheet,
    other then rearrange them, if the sheet has already been used to record the sensory
    analysis of a sample. If you do decide to do so, take extra care when
    comparing samples to ensure that they have been evaluated using the same version of the
    grid.

    Fundamentally, adding or deleting a tasting criterion between two sensory
    evaluations is tantamount to modifying the tasting protocols, and therefore the
    comparison could become irrelevant.

## Tasting session
### Definition

A tasting session is the comparative evaluation of a number of similar products
by a group of tasters, also known as a jury panel. It allows differences between 
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

Tasting sessions are linked to product types: To create a new tasting session, go
to [https://tastebuddy.io/protocols/](https://tastebuddy.io/protocols/) or click on `#!yaml Protocols` in the left sidebar or
top right menu, and click on either `+ Create Spirit Tasting Session` or `+ Create Wine Tasting Session` above the appropriate table.

<figure markdown="span">
![Session creation](images/session_creation.png#only-light){ loading=lazy }
![Session creation](images/session_creation_dark.png#only-dark){ loading=lazy }
</figure>

![Session creation](images/session_creation_2.png#only-light){ loading=lazy, width="390", align=left }
![Session creation](images/session_creation_2_dark.png#only-dark){ loading=lazy, width="390", align=left }

!!! warning "Wine VS Spirit tasting session"
    Make sure you have selected the correct product type from the Protocol page. Only the products of
    the selected product type [that have been previously created](products.md#product-creation)
    and the tasting sheets that apply to the considered product type will be 
    available in the various drop down menus.

    A direct link to the other product type is available at the top of the page
    in case of error.


<br>
On the newly opened page, enter the following information:

- **Name**;
- **Description** (optional): a description of the tasting session which will be
  displayed at the top of the page when tasters access the tasting. For example,
tips or warnings regarding the products can be added here;
- **Tasting sheet**: select the tasting grid to be used to evaluate the samples.
  Only [previously created tasting sheets](protocols.md#adding-a-tasting-sheet)
  corresponding to the selected product type will appear in the drop down menu;
- **Scheduled date**: the planned date of the tasting session, from which the
session will be accessible to assessors;
- **Accessible for**: how many days after the scheduled date should the tasting
  session be available (see note below).
- **Hide sample names**: activate the switch to replace the name of the samples
  by their serving order. Note: to display the name of the samples on the
results dashboard, edit the tasting session once all results have been submitted
and deactivate the switch
- **Assigned tasters**: select all the users who should participate in the
tasting session[^1]
- **Samples**: from the drop down menu, select the samples to be added to the
tasting session and assign them an order by filling the `Position` field next to
them. Any number of spirits (respectively wines) can be added by clicking `+ Add spirit`
(respectively `+ Add wine`)

!!! info "About scheduled date and availability"
    Any tasting session is accessible only from its scheduled date. It will not
    appear on any user's homepage before that specified date. The dashboard
    displaying the results, whether for a taster or for the admin themselves, won't
    be accessible either before either of these two conditions is fulfilled:

    1. All assigned tasters have completed the session and submitted results
    2. The delay specified in the field `Accessible for (days)`, calculated from
       the scheduled date, has passed.

    Once a taster has completed a tasting session and submitted their results,
    they won't be able to make any modification to their results, nor will they be
    able to access the tasting session anymore.

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

!!! tip "Following up the tasters progress"
    The progress of the assigned tasters can be followed live by the
    administrators. From the [homepage](https://tastebuddy.io), in the **TASTING
    PROGRESS** card, click the {++Progress++} button next to the corresponding
    tasting session to display all the tasters progress.

    <figure markdown="span">
    ![session progress](images/session_home.png#only-light){ loading=lazy, width="80%" }
    ![session progress](images/session_home_dark.png#only-dark){ loading=lazy, width="80%" }
    </figure>


[^1]: Currently only users with an account can be invited to a tasting session.
    Further development of TasteBuddy will open tasting sessions to _Anonymous
    users_
