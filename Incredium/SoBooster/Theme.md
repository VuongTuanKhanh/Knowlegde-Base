d# Ultimate Search and Filter
## Customize Process
- Navigate to **Customization** in the app.
- Select Javascript or Stylesheets.

## Defined template in `usf.templates` object
|Templates|Use Case|
|:-:|:-:|
|`app`|The wrapper widget template|
|`searchResults`|The search results container template|
|`searchResultsPages`|The search results grid view's classic pagination template|
|`searchResultsGridViewItem`|The search results grid item template|
|`searchResultsListViewItem`|The search results list item template|
|`addToCartPlugin`|The Add to cart plugin's button template|
|`previewPlugin`|The Preview plugin's button template|
|`previewPluginModal`|The Preview plugin's modal template|
|`gotoTop`|The Go to top element template|
|`searchResultsBanner`|The promotional banner template|
|`filtersBreadcrumb`|The attribute based filter breadcrumb template|
|`filters`|The template used to list all filters|
|`filter`|The filter template|
|`filterOption`|The filter option template|
|`instantSearch`|The template for displaying the instant search popup|
|`instantSearchItem`|The product template in the instant search popup|

## Resource
|||
|:-:|:-:|
|Javarscript Formatter|https://beautifier.io/|
|Check List|https://docs.google.com/spreadsheets/d/1oRH6LU1M_tYRvJqWOczeVr7WCGqFbMt1_4DJuNVQCK4/edit?ts=5e85deff#gid=1363574454|
|Document|https://docs.sobooster.com/search/developer/usf-sdk|
|Admin Page|http://admin.search-app.sobooster.com/login.aspx?ReturnUrl=%2fScripts%2fthemes.aspx|

## Process
- Duplicate the theme
- Preview the original one and the editing one, navigate to `collections/all`
- Theme `Setup` on the **USF** app, choose the editing theme
- Select `Customization` on the **USF** app to see the code
- On the Original theme, inspect to get the class name of the grid container ( this will be the section that hold all product ), then copy those class name and paste it to:
    - **Location**: Javascript - **USF** App
    - **Section**: `searchResults` in the `usf.templates`
    - **Position**: Find `view === \'grid\'`
- On the `Shopify Admin`, search for `collection`, navigate to `collection.liquid`
- Delete the `USF` section.
- `collection.liquid` will contain some template, navigate to the template that contain all of the products.
- Check the layout of the opened template whether it is `gird`, then navigate to the child template which is gridview
- On the opened template, find for the container class that we have, replace it with `<div id="usf_container"></div>` ( mean replace the theme's original contain with our container)
- Delete the pages section
- Recheck the editing theme whether our theme show up
- Take the HTML structure of a product on the original theme
- For product HTML ( check liquid of the origin ):
    - Tags:
        - `productUrl`
        - `selectedScaledImage`

## Convert
|Origin|USF|
|:-:|:-:|
|`product.variants.first.id`|`"product.selectedVariant || product.variants[0].id"`|
|`products.product.select_options`|`product.chooseOptions`|
|`products.product.select_options`|`loc.chooseOptions`|
|`product.handle`|`product.urlName`|