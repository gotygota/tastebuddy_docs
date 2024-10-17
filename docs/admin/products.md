# Products management

The second building block of sensory evaluation, products can be either wines or
spirits, which are evaluated by one or more tasters.

## Tasting session _versus_ One-off tasting

Before going into the details of product creation and updating, it is important
to consider two use cases that require two different setups:

1. :material-glass-wine::material-glass-wine::material-glass-wine: **Tasting session**: understood as the comparative evaluation of a range or
   flight of products, a tasting session requires the products to have been
   created beforehand;
2. :material-liquor: **One-off tasting**: understood as the evaluation of a single product on the
   move, a one-off tasting allows the creation of a product directly from the
   tasting grid. Existing products are automatically suggested, but a completely
   new sample can be automatically added to the database.

!!! note "Regular user rights"
    A regular user can add their own product to the database, which will then appear
    in the organisation's sample list. However, they will only be able to update or
    view the results of the product they have created. See the Dashboard section of
    the documentation.

## Product creation

Tastebuddy covers two types of products: wines and spirits. Both are created and
updated in the same way, albeit on different pages, but there are some
differences in their characterisation.

<div class="grid cards" markdown>

-   :material-glass-wine:{ .lg .middle} __Wines__{ .xl .middle }

    ---

    Wines take the following attributes:
    
    :octicons-triangle-right-24: Name

    :octicons-triangle-right-24: Category[^1]{ title="This information is required on product creation. If irrelevant or unavailable, the other fields can be left blank" } (_either of Red, White, Rosé, Sparkling, Fortified, Other_)

    :octicons-triangle-right-24: Brand

    :octicons-triangle-right-24: Country

    :octicons-triangle-right-24: Region

    :octicons-triangle-right-24: Description

    :octicons-triangle-right-24: Alcohol content

    :octicons-triangle-right-24: Vintage

    :octicons-triangle-right-24: Varietal

-   :material-glass-tulip:{ .lg .middle } __Spirits__

    ---

    Wines take the following attributes:
    
    :octicons-triangle-right-24: Name

    :octicons-triangle-right-24: Category[^1]{ title="This information is required on product creation. If irrelevant or unavailable, the other fields can be left blank" } (_Any category can be created_)

    :octicons-triangle-right-24: Brand

    :octicons-triangle-right-24: Country

    :octicons-triangle-right-24: Region

    :octicons-triangle-right-24: Description

    :octicons-triangle-right-24: Alcohol content

    :octicons-triangle-right-24: Age (in months)

    :octicons-triangle-right-24: Sugar content (in g/L)

</div>


[^1]:
    This information is required on product creation. All the other fields can
    be left blank if the information is irrelevant or unavailable

- To add a new wine, go to [https://tastebuddy.io/products/wine/](https://tastebuddy.io/products/wine/) and click `+ Add wine`
- To add a new spirit, go to [https://tastebuddy.io/products/spirit/](https://tastebuddy.io/products/spirit/) and click `+ Add spirit`

<figure markdown="span">
![Product creation](images/product.png#only-light){ loading=lazy }
![Product creation](images/product_dark.png#only-dark){ loading=lazy }
</figure>

Products can also be created directly from an existing tasting grid (for
_one-off tastings_). Existing categories and products are automatically
suggested to reduce the risk of duplication.

!!! warning "Duplicate samples"
    Currently the sample related fields of a point tasting are not automatically
    filled in, even if an existing product name is selected. Be careful not to
    create duplicates, as the system will treat them as different products when
    analysing the results.

    If some products are duplicates and need to be merged, please contact us using
    [using this form](https://tastebuddy.io/contact/) or any other means linked to your account.

## Updating product information

Products can be updated by clicking `Edit` on the relevant row in the product
table available on the above page.

!!! tip "Filling in the additional information for further analysis"
    Although most of the product identification fields are optional, it is good
    practice to characterise products as thoroughly as possible, as this information
    can be used to analyse trends and compare products over time.

<figure markdown="span">
![Product update](images/product_2.png#only-light){ loading=lazy, width="80%" }
![Product update](images/product_2_dark.png#only-dark){ loading=lazy, width="80%" }
</figure>
