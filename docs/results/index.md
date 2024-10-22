# Understanding results
## Preamble

All the steps described and explained in the previous pages have led to the
creation and accumulation of data on the sensory profile of wines and spirits.
The aim now is to be able to understand this data, to separate the valuable
entries from the less relevant ones, and to draw objective conclusions from a
subjective process.

To facilitate this process, all the data gathered from the sensory evaluation
can be visualised in a graphical manner to help understand and interpret the
results.

Before going any further, however, it is important to establish some common
ground about what can be expected from sensory evaluation, the shortcomings
inherent in the practice and how they can be mitigated.

!!! warning "A word of caution"

    When interpreting the results, the charts must be read with a critical eye:
    always take into account the conditions of the tasting, the profile of the
    tasters and the objectives of the tasting before drawing conclusions.

    Although the results may look similar from one dashboard to another, if the
    tastings were carried out under different conditions (time of day, glasses,
    background of the tasters, etc.), their interpretation may be completely
    different.

    Tastebuddy is designed to help you understand the tasting results, reduce the
    differences between tasters as much as possible to highlight product
    differences, and easily display large amounts of data. However, it does not
    pretend to provide a single truth about a product's sensory profile or predict
    its development or success in the marketplace.
## Expected differences between tasters

When wine or spirits are rated by a group of tasters, it is important to
remember that different people can and will use the rating tools in different
ways. This can lead to what may appear to be product differentiation, when in
fact it is simply the result of differences in the tasters' evaluation process.
The main differences are usually categorised as

1. Level difference;
2. Scaling difference;
3. Variability difference;
4. Disagreement.

In order to make a meaningful comparison between products, it is best to focus
on the disagreements. Level and scaling are differences that can be
easily reduced mathematically. Variability can be an indication of a taster's
reliability.

<figure markdown="span">
![Tasters differences](images/tasters_differences.png#only-light){ loading=lazy, width="80%" }
![Tasters differences](images/tasters_differences_dark.png#only-dark){ loading=lazy, width="80%" }
    <figcaption>Illustration of tasters differences</figcaption>
</figure>

### Level discrepancy
The level discrepancy should be understood as the difference between the scores
given by two assessors **with the same ranking between products AND the same
number of points between two products**.

<figure markdown="span">
![Level differences](images/level.png#only-light){ loading=lazy, width="80%" }
![Level differences](images/level_dark.webp#only-dark){ loading=lazy, width="80%" }
    <figcaption>Level differences</figcaption>
</figure>

For example, `Assessor 1` would give samples A, B and C 3, 4 and 6 points
respectively, while `Assessor 2` would give them 6, 7 and 9. Both agree on
the ranking and quality of the products even though their scores are different;
a score of “4” for Assessor 1 has the same value as a score of “7” for Assessor
2.

!!! charts "Data preprocessing"
    The level discrepancy can be completely removed by centering the scores on
    the panel average. This is done automatically on the product dashboards, but not on
    the tasters' self-assessment dashboards, so that they can correct their use of the
    scoring scales.
### Scaling difference
The scaling difference should be understood as the difference in the scores given by
two assessors with **the same ranking between products AND the same average score**.
It can be seen as how confident or shy the evaluator is in being able to clearly
differentiate between products in terms of scores or, on the contrary, to give
all products very similar scores. 

<figure markdown="span">
![scaling differences](images/scaling.png#only-light){ loading=lazy, width="80%" }
![scaling differences](images/scaling_dark.webp#only-dark){ loading=lazy, width="80%" }
    <figcaption>Scaling differences</figcaption>
</figure>

For example, `Assessor 1` would give Samples A,
B and C 2, 5 and 8 points respectively, while `Assessor 2` would give 4,
5 and 6 points; both would then give an average of 5 points and rank the
products equally;

!!! charts "Data preprocessing"
    The scaling difference can be reduced by normalizing the individual scores
    with feature scaling (either Min-Max or Standard deviation). This is done
    automatically on the product dashboards, but not on the tasters' self-assessment dashboards
    so that they can correct their use of the scoring scales.
### Variability
The variability can be understood as how consistent an assessor is in the scores
they give and is best illustrated by looking at the scores given to a single
sample in two different cases. Here the variability of `Assessor 2` is much higher
than that of `Assessor 1`.

<figure markdown="span">
![variability differences](images/variability.png#only-light){ loading=lazy, width="80%" }
![variability differences](images/variability_dark.webp#only-dark){ loading=lazy, width="80%" }
    <figcaption>Variability differences</figcaption>
</figure>

!!! tip "Measuring variability"
    The best way to measure a taster's variability is by serving twice the same
    sample in one sample flight during a tasting session. However, allow for some
    variability, as the order of a sample in a series has been shown to influence
    the scoring.
    [Calibretion](index.md#good-practices-in-sensory-analysis-calibration) helps in
    lessening this influence

### Disagreement
The disagreement (sometimes referred to simply as agreement) is a fairly
self-explanatory measure: it is the difference in the ranking of
the product. In this case, `Assessor 1` ranks B quite low, while `Assessor 2` ranks
it quite high. They show a clear disagreement about product B.

<figure markdown="span">
![disagreement differences](images/disagreement.png#only-light){ loading=lazy, width="80%" }
![disagreement differences](images/disagreement_dark.webp#only-dark){ loading=lazy, width="80%" }
    <figcaption>Disagreement</figcaption>
</figure>

## Product or taster differences?

Given the differences explained above, how can the evaluated products be
differentiated? Prior to the evaluation itself, precautions can be taken
directly to reduce as much as possible the level and scaling differences between
tasters, in order to standardise their scores, and to ensure that the
variability is due to the tasters themselves and not to the tasting conditions
(see [Regarding Calibration](index.md#good-practices-in-sensory-analysis-calibration)).
Both are criteria that tasters can directly influence if they can see where they
stand. After evaluation, the data collected can be pre-processed to
mathematically reduce the differences before analysis.

In a sense, **level** is a matter of calibration between assessors. A score of 80
should represent the same quality for the whole panel. It can be easily
corrected by centering the individual scores on a common value (usually the
panel average) before any analyses.

**Scaling** is somewhat a matter of homogenisation between raters and individual
confidence. This is easily seen in a box plot of the scores. For meaningful
results, judges should aim for the largest possible scale to clearly
differentiate products. It is important to note that an evaluator who does not
show a clear differentiation between products (i.e. who would always give almost
the same score) can probably be discarded from the overall analyses, unless the
tendency is the same for all evaluators in the panel. This last scenario would
prove that the products are very similar. The scaling differences between the
raters can be reduced by normalising the scores individually after centering
(usually with a min-max, mean or standard deviation function scaling).

**Variability** is the difference in the rating of the same sample by a taster on
different occasions. It is important to remember that the tasting conditions
should be exactly the same in order to be absolutely unambiguous. In practice,
the influence of products tasted immediately before or after will affect a
taster's perception of a sample and some variability is to be expected. However,
too much variability would probably require the taster to be discarded from
further analysis, as it shows that the rating is more random than a true
opinion.

Of course, some **disagreement** is to be expected within a panel of judges:
cultural differences between judges will affect their sensitivity to, and
therefore their perception of, a number of product characteristics. However,
there are intrinsic qualities and attributes that all should agree on. This is
probably the most important result to analyse between the judges, and if
personal information about the judges themselves (such as their age, gender,
nationality, etc.) is available, some patterns can be drawn from the analysis of
the results (preferences by age category, gender, nationality, etc.).

## Good practices in sensory analysis: calibration

A crucial step in comparative sensory analysis, and one that is all too often
underestimated, is calibration. It allows a panel of assessors to work with a
common standard and to "re-balance" between samples.

Calibration involves providing the panel with an additional sample, which is not
analysed, but used as a standard for all other products. The scores for this
sample are also fixed (either agreed by the panel or given directly) so that
each of the samples to be evaluated can be compared to this base product: all
the assessors then have a reference scale for scoring (reducing the potential
level differences between the assessors) and the influence of the position of
the sample within the tasting flight is reduced (thus providing a more
meaningful analysis of taster variability). However, scale differences are not
affected and require further careful analysis and/or data pre-processing (see
section 1.3 Product or taster differences?).

!!! tip "About anonymity"
    Sensory analysis is meaningless unless the anonymity of both the tasters and the
    products is guaranteed. Ensuring that the products are unknown to the judges
    protects against any "branding influence" (brand history, price range, public
    opinion, etc. are many factors that have been shown to influence consumer
    ratings and evaluations). On the other hand, the anonymity of the tasters allows
    them to be free from "peer pressure" and gives them the confidence to express
    their own opinions.

## Types of dashboards

Dashboards are graphical displays of sensory analysis results. They allow
for an easy interpretation of results, comparison of products, characterisation
of tasters preferences, and visual representation of the evolution of a product
sensory profile.

According to a user's role, they have access to different types of dashboards:
while Admins have access to all the data within an organisation, Regular Users
can only view their own or anonymized results.

Conceptually, the dashboards can be divided in two categories:

1. **Tasters (self-)assessment dashboards**: used by tasters to assess their
   evaluation style compare to other tasters (user of the scale, sensitivity to
   certain characteristics, preferences, etc.)
2. **Products assessment dashboards**: taking into account the tasters profiles,
   preferences and (dis)agreement, they allow for characterisation and
   comparison of products, highlighting their qualities and defaults.

Depending on the chosen dashboard, the **data is pre-processed** in different
manners, and in most cases, the **charts do not display the raw data**. The raw
data can be downloaded directly from the dashboards, and the data processing
steps are described in details for each of the charts whenever necessary.

The following pages explains in details each dashboard available on Tastebuddy,
as well as guidelines on how to interpret the results and draw conclusions from
the charts. The chart section describes each chart individually for easier
direct access.
