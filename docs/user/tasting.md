# Sensory evaluation in practice
Now we come to the heart of Tastebuddy: the sensory evaluation of wines and
spirits.

## Categories of tastings
Tastebuddy distinguishes between two different types of sensory evaluation,
designed to meet two different broad use cases:

1. :material-liquor: **Punctual or one-off tasting**: evaluation of a single
   product by a single taster _{==on the move==}_;
2. :material-glass-tulip::material-glass-tulip::material-glass-tulip: **Tasting
   session**: comparative sensory evaluation of two or more products _{==at the
same time==}_, which share common characteristics, by one or more assessors, in
order to highlight the differences between these products and to establish a
ranking between them;

One of the main differences between the two situations is that the former allows
the _"unprepared"_ evaluation of samples (i.e. the evaluation of a sample that
is unknown and unplanned before the tasting itself), while the latter requires
preparation work and usually fulfils a precise objective as to what the
comparative evaluation of the samples should highlight.

You can read examples of use [on this page](../results/use-cases.md).
## Punctual tasting
To evaluate a sample _on the go_, from your home page, click `Taste a spirit` or
`Taste a wine` at the bottom of the card corresponding to the tasting sheet you
want to use.

<figure markdown="span">
    ![Tasting sheet selection](images/tasting_sheet_selection.png#only-light){ loading=lazy }
    ![Tasting sheet selection](images/tasting_sheet_selection_dark.png#only-dark){ loading=lazy }
    <figcaption>Example tasting grid displayed on a user's home page</figcaption>
</figure>

### Product information

You will be taken to the tasting form. At the top of the form, you can enter
information about the product. The name and category will be suggested if any
records are found in the database. Click `Additional information` to add
more product related fields. 

<figure markdown="span">
    ![sample identification](images/sample_identification.png#only-light){ loading=lazy }
    ![sample identification](images/sample_identification_dark.png#only-dark){ loading=lazy }
</figure>

At this stage, only the product name is required. The product information
can always be updated later (see [Updating Product information](../admin/products.md#updating-product-information)).
It is strongly recommended to fill in all available information for
possible further analysis. 

!!! warning "Filling in product information"
    Although product names and categories are suggested when filling in the
    information in the appropriate field, there is currently no link between the
    two, so it is possible to create a new product record in the database
    by associating the wrong category with the product name.

    If two different products have been created and you would like to merge them
    into one, please contact your administrator to get in touch with us.

!!! tip "Naming convention"
    When naming products and categories, try to follow your organisation's
    guidelines to make it easier to find and compare products in the long term.

### Product evaluation

The second part of the form concerns the evaluation of the product itself.
Depending on the tasting grid, different characteristics must be rated according
to a pre-defined scale.

<figure markdown="span">
    ![sample evaluation](images/sample_evaluation.png#only-light){ loading=lazy }
    ![sample evaluation](images/sample_evaluation_dark.png#only-dark){ loading=lazy }
</figure>

For each criterion, choose the score you think the product deserves. Depending
on how the tasting grid has been designed, you may also be asked to add comments
or tasting notes to justify your scores.

Once you have completed all the criteria, click Submit to save your results. If
some criteria are missing, they will be highlighted in red when you submit your
results. If all the information is correct, you will be returned to the home
page with a confirmation message.

!!! info "Just About Right"
    Wines and spirits are usually rated according to a set of selected criteria to
    which a rating scale is assigned. The rating scale is usually not used as an
    intensity scale, but as a "just about right" scale. The maximum score therefore
    corresponds to the exact expected expression of the criterion in question.

    For example, you might rate the sweetness of a particular product. In this case,
    a scale of 1 to 10 should not be understood as

    from ```not sweet at all``` to ```excessively sweet ```

    but as

    from ```too sweet or not sweet enough``` to ```perfectly sweet ```

Remember to update the product information as soon as it becomes available
if you were unable to do so at the time of tasting.

You can visualise the result of the sensory evaluation by accessing the corresponding dashboard
on [https://tastebuddy.io/dashboards/](https://tastebuddy.io/dashboards/),
accessible from the left side bar or from the top right menu :material-view-grid:.

## Tasting sessions

### Entering a tasting session

Each tasting session you are assigned to will appear on your home page in
the `NEXT TASTING SESSIONS` section. Once open, click on `Access` to join the
tasting.

<figure markdown="span">
    ![tasting session access](images/tasting_session_access.png#only-light){ loading=lazy }
    ![tasting session access](images/tasting_session_access_dark.png#only-dark){ loading=lazy }
    <figcaption>Tasting session access on home page</figcaption>
</figure>

Note that you will not be able to access the tasting session before the
scheduled date. It will also expire after a delay set when the session was
created, and you won't be able to access it unless an administrator reopens it.

### Evaluating samples and submitting results

In this case, no product information is required as this information has been
specified by the administrator when the session was first created.

Depending on whether the session has been made anonymous, the names of the
samples may or may not be displayed.

{==

**Be careful with the order of the samples you rate, as each form on this page
relates to a specific sample!**

==}

At the top of the page you can switch between samples by clicking on the
appropriate tab, which will show the name of the sample or its order. As in the
case of [punctual tasting](#product-evaluation), fill in the scores per
criterion for each individual sample and justify your scores in the text box if
necessary.

<figure markdown="span">
    ![Tab navigation](images/tab_navigation.png#only-light){ loading=lazy }
    ![Tab navigation](images/tab_navigation_dark.png#only-dark){ loading=lazy }
    <figcaption>Tab navigation between samples</figcaption>
</figure>

At the bottom of each page, click `Validate Sample` to check that all the
required information has been completed for that particular sample. You can
always return to a sample after you have validated it.

!!! info "About Sample Validation and Submission"
    The Sample Validation is simply a check to ensure that all the required
    information has been filled in on the relevant form. It provides a visual
    validation by highlighting in red any field that has not been filled in, and
    also your progress through the tasting session by displaying your progress on
    the [Session progress administrator
    page](../admin/protocols.md#following-up-the-tasters-progress).

    However, it does not submit any results to the database. Clicking on {++Submit
    all results :material-check-all:++} will save your results and return you to the
    home page. However, if you are missing information in any field, you will not
    leave the page, the missing field will also be highlighted in red, but you will
    not automatically be taken to the Missing Information tab.

    **Don't leave the page manually as your results will not be saved!** If
    everything is correct, you will be **automatically redirected** after clicking
    on {++Submit all results :material-check-all:++}

    <div class="grid cards" markdown>

    -   <figure markdown="span">
            ![Sample validation](images/validate_sample.png#only-light){ loading=lazy }
            ![Sample validation](images/validate_sample_dark.png#only-dark){ loading=lazy }
            <figcaption>The Validate sample only confirms all fields are correct</figcaption>
        </figure>

    -   <figure markdown="span">
            ![Results submission](images/submit_results_dark.png#only-light){ loading=lazy }
            ![Results submission](images/submit_results.png#only-dark){ loading=lazy }
            <figcaption>The Submit all results button save the results and redirect
            to the home page</figcaption>
        </figure>

    </div>

You can view the results of the tasting session by accessing the corresponding dashboard
on [https://tastebuddy.io/dashboards/](https://tastebuddy.io/dashboards/),
accessible from the left side bar or from the top right menu :material-view-grid:.
Note that the dashboard will only be available once all the assigned tasters
have submitted their results or after the delay set by the administrator has
elapsed. The following section explains how to read the dashboards and what
conclusions to draw from them.
