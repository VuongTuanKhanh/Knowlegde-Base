# Code Snippet

## Get the metafields
```js
usf.utils.getMetafield(product,<METAFIELD_NAME>,<METAFIELD_KEY>)
```

## Change the size of an image
```js
function getImgWithSize (img, size = '') {
    return img.replace('{size}', size)
}
```
```js
const _usfImageWidths = [180, 220, 300, 360, 460, 540, 720, 900, 1080, 1296, 1512, 1728, 2048, 2450, 2700, 3000, 3350, 3750, 4100];
```
```js
const usfBgsetWidths = [180, 360, 540, 720, 900, 1080, 1296, 1512, 1728, 1950, 2100, 2260, 2450, 2700, 3000, 3350, 3750, 4100]

```

## USF Settings
### Section Settings
```js
if (!window.usf_sectionSettings)
    window.usf_sectionSettings = {
        coll_show_feat: true,
        coll_show_sort: true,
        grid_show_vendor: true,
        head_img_coll_handled: false,
        header_image: null,
        products_per_row_int: 3,
        show_tags: true
    };
```
### Global Settings
```js
if (!window.usf_globalSettings)
    window.usf_globalSettings = {
        label_remain_show: false,
        label_sale_show: true,
        label_soldout_show: true,
        prod_stock_warn_limit_int: 1,
        product_hover_image: true,
        product_label_position: "tr"
    };
```
### USF Text
#### From Text
```js
if (!window.usf_fromText)
    window.usf_fromText = "From";
```
#### Inventory Text
```js
if (!window.usf_inventoryText)
    window.usf_inventoryText = "Only {{ quantity }} left!";
```
### Number of Columns per row
```js
var col_class = "";
switch (window.usf_sectionSettings.products_per_row_int) {
    case 2:
        col_class = "half";
        break;
    case 3:
        col_class = "third";
        break;
    case 5:
        col_class = "fifth";
        break;
    default:
        break;
}
```