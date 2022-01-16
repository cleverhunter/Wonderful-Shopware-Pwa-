<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@shopware-pwa/composables](./composables.md)

## composables package

Vue's composables to be used in Shopware frontend application.

## Functions

|  Function | Description |
|  --- | --- |
|  [createListingComposable({ searchMethod, searchDefaults, listingKey, })](./composables.createlistingcomposable.md) | Factory to create your own listing. By default you can use useListing composable, which provides you predefined listings for category(cms) listing and product search listing. Using factory you can provide our own compatible search method and use it for example for creating listing of orders in my account. |
|  [createShopware(app, options)](./composables.createshopware.md) | <b><i>(BETA)</i></b> Create ShopwarePlugin vue instance. Shpware PWA composables rely on this config. |
|  [getApplicationContext(params)](./composables.getapplicationcontext.md) | <b><i>(BETA)</i></b> Get the current application context values. The context is either a scope or a component instance. This method checks if the context contains all the necessary data.<!-- -->This method will likely change in future in order to provide full Vue3 compability. |
|  [getDefaultApiParams()](./composables.getdefaultapiparams.md) | <b><i>(BETA)</i></b> Returns default system API params |
|  [useAddToCart(params)](./composables.useaddtocart.md) | <b><i>(BETA)</i></b> Add product to cart. Options - [IUseAddToCart](./composables.iuseaddtocart.md) |
|  [useBreadcrumbs(params)](./composables.usebreadcrumbs.md) | <b><i>(BETA)</i></b> Composable for displaying and setting breadcrumbs for page. |
|  [useCart()](./composables.usecart.md) | <b><i>(BETA)</i></b> Composable for cart management. Options - [IUseCart](./composables.iusecart.md) |
|  [useCheckout()](./composables.usecheckout.md) | <b><i>(BETA)</i></b> Composable for Checkout management. Options - [IUseCheckout](./composables.iusecheckout.md) |
|  [useCms(params)](./composables.usecms.md) | <b><i>(BETA)</i></b> |
|  [useCountries()](./composables.usecountries.md) | <b><i>(BETA)</i></b> |
|  [useCountry(props)](./composables.usecountry.md) | <b><i>(BETA)</i></b> |
|  [useCurrency()](./composables.usecurrency.md) | <b><i>(BETA)</i></b> |
|  [useCustomerAddresses()](./composables.usecustomeraddresses.md) | <b><i>(BETA)</i></b> Composable for user's addresses management. Options - [IUseCustomerAddresses](./composables.iusecustomeraddresses.md) |
|  [useCustomerOrders()](./composables.usecustomerorders.md) | <b><i>(BETA)</i></b> Composable for listing customer orders. Options - [IUseCustomerOrders](./composables.iusecustomerorders.md) |
|  [useCustomerPassword()](./composables.usecustomerpassword.md) | <b><i>(BETA)</i></b> Composable for customer password management. Options - [IUseCustomerPassword](./composables.iusecustomerpassword.md) |
|  [useDefaults(params)](./composables.usedefaults.md) | <b><i>(BETA)</i></b> Returns default config depending on config key. It is used in composables, so defaultsKey is in most cases composable name (ex. <code>useDefaults({ defaultsKey: &quot;useCms&quot; })</code>) |
|  [useIntercept()](./composables.useintercept.md) | Allows to broadcast and intercept events across application. |
|  [useListing(params)](./composables.uselisting.md) | <b><i>(BETA)</i></b> |
|  [useNavigation(params)](./composables.usenavigation.md) | <b><i>(BETA)</i></b> Composable for navigation. Options - [IUseNavigation](./composables.iusenavigation.md) |
|  [useNotifications()](./composables.usenotifications.md) | <b><i>(BETA)</i></b> |
|  [useOrderDetails(params)](./composables.useorderdetails.md) | <b><i>(BETA)</i></b> Composable for managing an existing order. |
|  [useProduct(params)](./composables.useproduct.md) | <b><i>(BETA)</i></b> |
|  [useProductAssociations(params)](./composables.useproductassociations.md) | <b><i>(BETA)</i></b> Get product association entity. Options - [IUseProductAssociations](./composables.iuseproductassociations.md) |
|  [useProductConfigurator(params)](./composables.useproductconfigurator.md) | <b><i>(BETA)</i></b> Product options - [IUseAddToCart](./composables.iuseaddtocart.md) |
|  [useProductQuickSearch()](./composables.useproductquicksearch.md) | <b><i>(BETA)</i></b> |
|  [useSalutations()](./composables.usesalutations.md) | <b><i>(BETA)</i></b> |
|  [useSessionContext()](./composables.usesessioncontext.md) | <b><i>(BETA)</i></b> Composable for session management. Options - [IUseSessionContext](./composables.iusesessioncontext.md) |
|  [useSharedState()](./composables.usesharedstate.md) | Replacement for Vuex. Composable, which enables you to use shared state in your application. State is shared both on server and client side. |
|  [useUIState(params)](./composables.useuistate.md) | <b><i>(BETA)</i></b> Simple state management for UI purposes. |
|  [useUser()](./composables.useuser.md) | <b><i>(BETA)</i></b> Composable for user management. Options - [IUseUser](./composables.iuseuser.md) |
|  [useWishlist(params)](./composables.usewishlist.md) | <b><i>(BETA)</i></b> |

## Interfaces

|  Interface | Description |
|  --- | --- |
|  [IInterceptorCallbackFunction](./composables.iinterceptorcallbackfunction.md) | interface for the callback function of interceptors |
|  [IUseAddToCart](./composables.iuseaddtocart.md) | <b><i>(BETA)</i></b> interface for [useAddToCart()](./composables.useaddtocart.md) composable |
|  [IUseCart](./composables.iusecart.md) | <b><i>(BETA)</i></b> interface for [useCart()](./composables.usecart.md) composable |
|  [IUseCheckout](./composables.iusecheckout.md) | <b><i>(BETA)</i></b> interface for [useCheckout()](./composables.usecheckout.md) composable |
|  [IUseCountries](./composables.iusecountries.md) | <b><i>(BETA)</i></b> |
|  [IUseCountry](./composables.iusecountry.md) | <b><i>(BETA)</i></b> |
|  [IUseCurrency](./composables.iusecurrency.md) | <b><i>(BETA)</i></b> |
|  [IUseCustomerAddresses](./composables.iusecustomeraddresses.md) | <b><i>(BETA)</i></b> interface for [useCustomerAddresses()](./composables.usecustomeraddresses.md) composable |
|  [IUseCustomerOrders](./composables.iusecustomerorders.md) | <b><i>(BETA)</i></b> interface for [useCustomerOrders()](./composables.usecustomerorders.md) composable |
|  [IUseCustomerPassword](./composables.iusecustomerpassword.md) | <b><i>(BETA)</i></b> interface for [useCustomerPassword()](./composables.usecustomerpassword.md) composable |
|  [IUseListing](./composables.iuselisting.md) | Listing interface, can be used to display category products, search products or any other Shopware search interface (ex. orders with pagination) |
|  [IUseNavigation](./composables.iusenavigation.md) | <b><i>(BETA)</i></b> interface for [useNavigation()](./composables.usenavigation.md) composable<!-- -->Provides state for navigation trees depending on navigation type. |
|  [IUseProduct](./composables.iuseproduct.md) | <b><i>(BETA)</i></b> |
|  [IUseProductAssociations](./composables.iuseproductassociations.md) | <b><i>(BETA)</i></b> interface for [IUseProductAssociations](./composables.iuseproductassociations.md) composable |
|  [IUseProductConfigurator](./composables.iuseproductconfigurator.md) | <b><i>(BETA)</i></b> interface for [useProductConfigurator()](./composables.useproductconfigurator.md) composable |
|  [IUseProductQuickSearch](./composables.iuseproductquicksearch.md) | <b><i>(BETA)</i></b> |
|  [IUseSalutations](./composables.iusesalutations.md) | <b><i>(BETA)</i></b> |
|  [IUseSessionContext](./composables.iusesessioncontext.md) | <b><i>(BETA)</i></b> interface for [useSessionContext()](./composables.usesessioncontext.md) composable |
|  [IUseUser](./composables.iuseuser.md) | <b><i>(BETA)</i></b> interface for [useUser()](./composables.useuser.md) composable |
|  [IUseWishlist](./composables.iusewishlist.md) | <b><i>(BETA)</i></b> interface for [useWishlist()](./composables.usewishlist.md) composable |
|  [Notification\_2](./composables.notification_2.md) | <b><i>(BETA)</i></b> |
|  [ShopwareDomain](./composables.shopwaredomain.md) | <b><i>(BETA)</i></b> |

## Variables

|  Variable | Description |
|  --- | --- |
|  [INTERCEPTOR\_KEYS](./composables.interceptor_keys.md) | <b><i>(BETA)</i></b> Keys used accross composables with the name of incommint parameters. |
|  [ShopwareVuePlugin](./composables.shopwarevueplugin.md) | <b><i>(BETA)</i></b> |

## Type Aliases

|  Type Alias | Description |
|  --- | --- |
|  [ListingType](./composables.listingtype.md) | <b><i>(BETA)</i></b> |
|  [Search](./composables.search.md) | <b><i>(BETA)</i></b> |
|  [SwInterceptor](./composables.swinterceptor.md) | <b><i>(BETA)</i></b> |
|  [SwInterceptors](./composables.swinterceptors.md) | <b><i>(BETA)</i></b> |
|  [SwRouting](./composables.swrouting.md) | <b><i>(BETA)</i></b> Routing type for Shopware SEO path resolvers |
