# Property of the Components
|Component|Class or tag|Value or Template|Description|
|:--|:--|:--|:--|
|`usf`|`usf-filters-horz`|`usf.settings.filters.horz`|Check whether the Filter is in Vertical or Horizontal mode|

# Component
|Component|Template|
|:--|:--|
|**Filter**|`<usf-filters></usf-filters>`|
|**Search Result**|`<usf-sr></usf-sr>`|
|**Banner**|`<usf-sr-banner v-if="result && result.extra && result.extra.banner && result.extra.banner.isBottom" :banner="result.extra.banner"></usf-sr-banner>`|
|**Total Filtered Product**|`_usfSearchResultsSummaryTpl`|
|**Filter type drop down**|`_usfSearchResultsSortByTpl`|
|**Grid & List view buttons**|`_usfSearchResultsViewsTpl`|
