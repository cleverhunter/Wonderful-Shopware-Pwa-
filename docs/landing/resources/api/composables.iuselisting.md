<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@shopware-pwa/composables](./composables.md) &gt; [IUseListing](./composables.iuselisting.md)

## IUseListing interface

Listing interface, can be used to display category products, search products or any other Shopware search interface (ex. orders with pagination)

<b>Signature:</b>

```typescript
export interface IUseListing<ELEMENTS_TYPE> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [changeCurrentPage](./composables.iuselisting.changecurrentpage.md) | (pageNumber?: number \| string) =&gt; Promise&lt;void&gt; |  |
|  [changeCurrentSortingOrder](./composables.iuselisting.changecurrentsortingorder.md) | (order: string \| string\[\]) =&gt; Promise&lt;void&gt; |  |
|  [getAvailableFilters](./composables.iuselisting.getavailablefilters.md) | ComputedRef&lt;ListingFilter\[\]&gt; |  |
|  [getCurrentFilters](./composables.iuselisting.getcurrentfilters.md) | ComputedRef&lt;any&gt; |  |
|  [getCurrentListing](./composables.iuselisting.getcurrentlisting.md) | ComputedRef&lt;Partial&lt;ListingResult&lt;ELEMENTS\_TYPE&gt;&gt; \| null&gt; |  |
|  [getCurrentPage](./composables.iuselisting.getcurrentpage.md) | ComputedRef&lt;string \| number&gt; |  |
|  [getCurrentSortingOrder](./composables.iuselisting.getcurrentsortingorder.md) | ComputedRef&lt;string \| undefined&gt; |  |
|  [getElements](./composables.iuselisting.getelements.md) | ComputedRef&lt;ELEMENTS\_TYPE\[\]&gt; |  |
|  [getInitialListing](./composables.iuselisting.getinitiallisting.md) | ComputedRef&lt;ListingResult&lt;ELEMENTS\_TYPE&gt; \| null&gt; |  |
|  [getLimit](./composables.iuselisting.getlimit.md) | ComputedRef&lt;number&gt; |  |
|  [getSortingOrders](./composables.iuselisting.getsortingorders.md) | ComputedRef&lt;Sort\[\] \| { key: string; label: string; }&gt; |  |
|  [getTotal](./composables.iuselisting.gettotal.md) | ComputedRef&lt;number&gt; |  |
|  [getTotalPagesCount](./composables.iuselisting.gettotalpagescount.md) | ComputedRef&lt;number&gt; |  |
|  [initSearch](./composables.iuselisting.initsearch.md) | (criteria: Partial&lt;ShopwareSearchParams&gt;) =&gt; Promise&lt;void&gt; |  |
|  [loading](./composables.iuselisting.loading.md) | ComputedRef&lt;boolean&gt; |  |
|  [loadingMore](./composables.iuselisting.loadingmore.md) | ComputedRef&lt;boolean&gt; |  |
|  [loadMore](./composables.iuselisting.loadmore.md) | () =&gt; Promise&lt;void&gt; |  |
|  [search](./composables.iuselisting.search.md) | (criteria: Partial&lt;ShopwareSearchParams&gt;, options?: { preventRouteChange?: boolean; }) =&gt; Promise&lt;void&gt; |  |
|  [setInitialListing](./composables.iuselisting.setinitiallisting.md) | (initialListing: Partial&lt;ListingResult&lt;ELEMENTS\_TYPE&gt;&gt;) =&gt; void |  |
