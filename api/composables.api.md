## API Report File for "@shopware-pwa/composables"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AddressType } from '@shopware-pwa/commons/interfaces';
import { ApiDefaults } from '@shopware-pwa/commons';
import { App } from 'vue-demi';
import { BillingAddress } from '@shopware-pwa/commons/interfaces';
import { Breadcrumb } from '@shopware-pwa/commons/interfaces';
import { Cart } from '@shopware-pwa/commons/interfaces';
import { CmsPageResponse } from '@shopware-pwa/commons/interfaces';
import { CmsResourceType } from '@shopware-pwa/commons/interfaces';
import { ComputedRef } from 'vue-demi';
import { Country } from '@shopware-pwa/commons/interfaces';
import { CreateOrderParams } from '@shopware-pwa/commons/interfaces';
import { CrossSelling } from '@shopware-pwa/commons/interfaces';
import { Currency } from '@shopware-pwa/commons/interfaces';
import { Customer } from '@shopware-pwa/commons/interfaces';
import { CustomerAddress } from '@shopware-pwa/commons/interfaces';
import { CustomerRegistrationParams } from '@shopware-pwa/commons/interfaces';
import { CustomerResetPasswordParam } from '@shopware-pwa/shopware-6-client';
import { CustomerUpdateEmailParam } from '@shopware-pwa/shopware-6-client';
import { CustomerUpdatePasswordParam } from '@shopware-pwa/shopware-6-client';
import { CustomerUpdateProfileParam } from '@shopware-pwa/shopware-6-client';
import { EffectScope } from 'vue-demi';
import { EntityError } from '@shopware-pwa/commons/interfaces';
import { Includes } from '@shopware-pwa/commons/interfaces';
import { LineItem } from '@shopware-pwa/commons/interfaces';
import { ListingFilter } from '@shopware-pwa/helpers';
import { ListingResult } from '@shopware-pwa/commons/interfaces';
import { Order } from '@shopware-pwa/commons/interfaces';
import { PaymentMethod } from '@shopware-pwa/commons/interfaces';
import { Product } from '@shopware-pwa/commons/interfaces';
import { PropertyGroup } from '@shopware-pwa/commons/interfaces';
import { Ref } from 'vue-demi';
import { Salutation } from '@shopware-pwa/commons/interfaces';
import { SessionContext } from '@shopware-pwa/commons/interfaces';
import { ShippingAddress } from '@shopware-pwa/commons/interfaces';
import { ShippingMethod } from '@shopware-pwa/commons/interfaces';
import { ShopwareApiInstance } from '@shopware-pwa/shopware-6-client';
import { ShopwareAssociation } from '@shopware-pwa/commons/interfaces';
import { ShopwareError } from '@shopware-pwa/commons/interfaces';
import { ShopwareSearchParams } from '@shopware-pwa/commons/interfaces';
import { Sort } from '@shopware-pwa/commons/interfaces';
import { StoreNavigationElement } from '@shopware-pwa/commons/interfaces';
import { StoreNavigationType } from '@shopware-pwa/commons/interfaces';
import { UnwrapRef } from 'vue-demi';
import { WritableComputedRef } from 'vue-demi';

// @public
export function createListingComposable<ELEMENTS_TYPE>({ searchMethod, searchDefaults, listingKey, }: {
    searchMethod: (searchParams: Partial<ShopwareSearchParams>) => Promise<ListingResult<ELEMENTS_TYPE>>;
    searchDefaults: ShopwareSearchParams;
    listingKey: string;
}): IUseListing<ELEMENTS_TYPE>;

// @beta
export function createShopware(app: App, options: {
    initialStore: any;
    shopwareDefaults: ApiDefaults;
    apiInstance: ShopwareApiInstance;
}): {
    install(app: App, options?: {
        enableDevtools: boolean;
    } | undefined): void;
    _a: App;
    _e: EffectScope;
    apiInstance: ShopwareApiInstance;
    state: {
        interceptors: {};
        sharedStore: any;
        shopwareDefaults: {
            [x: string]: {
                p?: number | undefined;
                limit?: number | undefined;
                sort?: string | undefined;
                order?: string | undefined;
                term?: string | undefined;
                ids?: string[] | undefined;
                associations?: {
                    [x: string]: {
                        associations?: any | undefined;
                        sort?: string | {
                            field: string;
                            order: string;
                            naturalSorting: boolean;
                        }[] | undefined;
                    };
                } | undefined;
                grouping?: {
                    field: string;
                } | undefined;
                properties?: string | never[] | undefined;
                manufacturer?: string | never[] | undefined;
                includes?: {
                    [x: string]: string[];
                } | undefined;
                query?: string | undefined;
            };
        };
    } | undefined;
};

// @alpha
export function extendScopeContext(scope: any, app: any): void;

// @beta
export function getApplicationContext(params?: {
    contextName?: string;
}): {
    apiInstance: any;
    router: any;
    route: any;
    routing: SwRouting;
    i18n: any;
    cookies: any;
    shopwareDefaults: any;
    interceptors: any;
    sharedStore: any;
    devtools: any;
    isServer: boolean;
    contextName: string;
} | {
    apiInstance: ShopwareApiInstance;
    router: any;
    route: any;
    routing: SwRouting;
    i18n: any;
    cookies: any;
    shopwareDefaults: ApiDefaults;
    interceptors: SwInterceptors;
    sharedStore: {
        [x: string]: any;
    };
    isServer: boolean;
    contextName: string;
    devtools?: undefined;
};

// @beta
export function getDefaultApiParams(): {
    [composableName: string]: ShopwareSearchParams;
};

// @public
export interface IInterceptorCallbackFunction {
    // (undocumented)
    (payload: any): void;
}

// @beta
export const INTERCEPTOR_KEYS: {
    ADD_TO_CART: string;
    ADD_TO_WISHLIST: string;
    ADD_PROMOTION_CODE: string;
    ERROR: string;
    WARNING: string;
    NOTICE: string;
    ORDER_PLACE: string;
    ORDER_PAYMENT_METHOD_CHANGED: string;
    ORDER_CANCELLED: string;
    ORDER_DETAILS_LOADED: string;
    ORDER_HANDLE_PAYMENT: string;
    SESSION_SET_CURRENCY: string;
    SESSION_SET_PAYMENT_METHOD: string;
    SESSION_SET_SHIPPING_METHOD: string;
    USER_LOGOUT: string;
    USER_LOGIN: string;
    USER_REGISTER: string;
};

// @beta
export interface IUseAddToCart {
    addToCart: () => Promise<void>;
    error: Ref<string>;
    getAvailableStock: Ref<number | null>;
    getStock: Ref<number | null>;
    isInCart: Ref<boolean>;
    loading: Ref<boolean>;
    onAddToCart: (fn: (params: {
        product: Product;
        quantity: Number;
    }) => void) => void;
    quantity: Ref<number>;
}

// @beta
export interface IUseCart {
    // (undocumented)
    addProduct: ({ id, quantity, }: {
        id: string;
        quantity?: number;
    }) => Promise<Cart>;
    // (undocumented)
    addPromotionCode: (promotionCode: string) => Promise<void>;
    // (undocumented)
    appliedPromotionCodes: ComputedRef<LineItem[]>;
    // (undocumented)
    cart: ComputedRef<Cart | null>;
    // (undocumented)
    cartErrors: ComputedRef<EntityError[]>;
    // (undocumented)
    cartItems: ComputedRef<LineItem[]>;
    // (undocumented)
    changeProductQuantity: ({ id, quantity, }: {
        id: string;
        quantity: number;
    }) => void;
    // (undocumented)
    count: ComputedRef<number>;
    // (undocumented)
    error: ComputedRef<string>;
    // (undocumented)
    getProductItemsSeoUrlsData(): Promise<Partial<Product>[]>;
    // (undocumented)
    loading: ComputedRef<boolean>;
    // (undocumented)
    refreshCart: () => void;
    // (undocumented)
    removeItem: ({ id }: LineItem) => Promise<void>;
    // (undocumented)
    shippingTotal: ComputedRef<number>;
    // (undocumented)
    subtotal: ComputedRef<number>;
    // (undocumented)
    totalPrice: ComputedRef<number>;
}

// @beta
export interface IUseCheckout {
    // (undocumented)
    billingAddress: ComputedRef<Partial<BillingAddress> | undefined>;
    // (undocumented)
    createOrder: (params?: CreateOrderParams) => Promise<Order>;
    // (undocumented)
    getPaymentMethods: (options?: {
        forceReload: boolean;
    }) => Promise<ComputedRef<PaymentMethod[]>>;
    // (undocumented)
    getShippingMethods: (options?: {
        forceReload: boolean;
    }) => Promise<ComputedRef<ShippingMethod[]>>;
    // (undocumented)
    loadings: UnwrapRef<{
        createOrder: boolean;
    }>;
    // (undocumented)
    onOrderPlace: (fn: (params: {
        order: Order;
    }) => void) => void;
    // (undocumented)
    paymentMethods: ComputedRef<PaymentMethod[]>;
    // (undocumented)
    shippingAddress: ComputedRef<ShippingAddress | undefined>;
    // (undocumented)
    shippingMethods: ComputedRef<ShippingMethod[]>;
}

// @beta (undocumented)
export interface IUseCountries {
    // (undocumented)
    error: Ref<any>;
    // (undocumented)
    fetchCountries: () => Promise<void>;
    // (undocumented)
    getCountries: ComputedRef<Country[]>;
    // (undocumented)
    mountedCallback: () => Promise<void>;
}

// @beta (undocumented)
export interface IUseCountry {
    // (undocumented)
    currentCountry: ComputedRef<Country | null>;
    // (undocumented)
    displayState: ComputedRef<boolean>;
    // (undocumented)
    forceState: ComputedRef<boolean>;
}

// @beta (undocumented)
export interface IUseCurrency {
    // (undocumented)
    availableCurrencies: ComputedRef<Currency[]>;
    // (undocumented)
    currency: ComputedRef<Currency | null>;
    // (undocumented)
    currencySymbol: ComputedRef<string>;
    // (undocumented)
    loadAvailableCurrencies: (options?: {
        forceReload: boolean;
    }) => Promise<void>;
    // (undocumented)
    setCurrency: (parameter: Partial<Currency>) => Promise<void>;
}

// @beta
export interface IUseCustomerAddresses {
    // (undocumented)
    addAddress: (params: Partial<CustomerAddress>) => Promise<string | undefined>;
    // (undocumented)
    addresses: ComputedRef<CustomerAddress[]>;
    // (undocumented)
    deleteAddress: (addressId: string) => Promise<boolean>;
    // (undocumented)
    errors: UnwrapRef<{
        markAddressAsDefault: ShopwareError[];
        loadAddresses: ShopwareError[];
        addAddress: ShopwareError[];
        updateAddress: ShopwareError[];
        deleteAddress: ShopwareError[];
    }>;
    // (undocumented)
    loadAddresses: () => Promise<void>;
    // (undocumented)
    markAddressAsDefault: ({ addressId, type, }: {
        addressId?: string;
        type?: AddressType;
    }) => Promise<string | boolean>;
    // (undocumented)
    updateAddress: (params: Partial<CustomerAddress>) => Promise<string | undefined>;
}

// @beta
export interface IUseCustomerOrders {
    // (undocumented)
    errors: UnwrapRef<{
        loadOrders: ShopwareError[];
    }>;
    // (undocumented)
    getOrderDetails: (orderId: string) => Promise<Order | undefined>;
    // (undocumented)
    loadOrders: () => Promise<void>;
    // (undocumented)
    orders: Ref<Order[] | null>;
}

// @beta
export interface IUseCustomerPassword {
    // (undocumented)
    errors: UnwrapRef<{
        resetPassword: ShopwareError[];
        updatePassword: ShopwareError[];
    }>;
    // (undocumented)
    resetPassword: (resetPasswordData: CustomerResetPasswordParam) => Promise<boolean>;
    // (undocumented)
    updatePassword: (updatePasswordData: CustomerUpdatePasswordParam) => Promise<boolean>;
}

// @public
export interface IUseListing<ELEMENTS_TYPE> {
    // (undocumented)
    changeCurrentPage: (pageNumber?: number | string) => Promise<void>;
    // (undocumented)
    changeCurrentSortingOrder: (order: string | string[]) => Promise<void>;
    // (undocumented)
    getAvailableFilters: ComputedRef<ListingFilter[]>;
    // (undocumented)
    getCurrentFilters: ComputedRef<any>;
    // (undocumented)
    getCurrentListing: ComputedRef<Partial<ListingResult<ELEMENTS_TYPE>> | null>;
    // (undocumented)
    getCurrentPage: ComputedRef<string | number>;
    // (undocumented)
    getCurrentSortingOrder: ComputedRef<string | undefined>;
    // (undocumented)
    getElements: ComputedRef<ELEMENTS_TYPE[]>;
    // (undocumented)
    getInitialListing: ComputedRef<ListingResult<ELEMENTS_TYPE> | null>;
    // (undocumented)
    getLimit: ComputedRef<number>;
    // (undocumented)
    getSortingOrders: ComputedRef<Sort[] | {
        key: string;
        label: string;
    }>;
    // (undocumented)
    getTotal: ComputedRef<number>;
    // (undocumented)
    getTotalPagesCount: ComputedRef<number>;
    // (undocumented)
    initSearch: (criteria: Partial<ShopwareSearchParams>) => Promise<void>;
    // (undocumented)
    loading: ComputedRef<boolean>;
    // (undocumented)
    loadingMore: ComputedRef<boolean>;
    // (undocumented)
    loadMore: () => Promise<void>;
    // (undocumented)
    search: (criteria: Partial<ShopwareSearchParams>, options?: {
        preventRouteChange?: boolean;
    }) => Promise<void>;
    // (undocumented)
    setInitialListing: (initialListing: Partial<ListingResult<ELEMENTS_TYPE>>) => void;
}

// @beta
export interface IUseNavigation {
    loadNavigationElements: (params: {
        depth: number;
    }) => Promise<void>;
    // (undocumented)
    navigationElements: ComputedRef<StoreNavigationElement[] | null>;
}

// @beta (undocumented)
export interface IUseProduct<PRODUCT, SEARCH> {
    // (undocumented)
    [x: string]: any;
    // (undocumented)
    error: Ref<any>;
    // (undocumented)
    loading: Ref<boolean>;
    // (undocumented)
    product: Ref<PRODUCT | null>;
    // (undocumented)
    search: SEARCH;
}

// @beta
export interface IUseProductAssociations {
    isLoading: ComputedRef<boolean>;
    loadAssociations: (params: {
        params: unknown;
        method: "post" | "get";
    }) => Promise<void>;
    // (undocumented)
    productAssociations: ComputedRef<CrossSelling[]>;
}

// @beta
export interface IUseProductConfigurator {
    // (undocumented)
    findVariantForSelectedOptions: (options?: {
        [key: string]: string;
    }) => Promise<void>;
    getOptionGroups: Ref<PropertyGroup[]>;
    getSelectedOptions: Ref<{
        [key: string]: string;
    }>;
    handleChange: (attribute: string, option: string, onChangeHandled?: Function) => Promise<void>;
    isLoadingOptions: Ref<boolean>;
}

// @beta (undocumented)
export interface IUseProductQuickSearch {
    // (undocumented)
    getProducts: ComputedRef<Product[]>;
    // (undocumented)
    getTotal: ComputedRef<number>;
    // (undocumented)
    loading: ComputedRef<boolean>;
    // (undocumented)
    loadMore: () => Promise<void>;
    // (undocumented)
    search: (additionalCriteria?: Partial<ShopwareSearchParams>) => Promise<void>;
    // (undocumented)
    searchTerm: Ref<string>;
}

// @beta (undocumented)
export interface IUseSalutations {
    // (undocumented)
    error: Ref<any>;
    // (undocumented)
    fetchSalutations: () => Promise<void>;
    // (undocumented)
    getSalutations: ComputedRef<Salutation[]>;
    // (undocumented)
    mountedCallback: () => Promise<void>;
}

// @beta
export interface IUseSessionContext {
    // (undocumented)
    activeBillingAddress: ComputedRef<BillingAddress | null>;
    // (undocumented)
    activeShippingAddress: ComputedRef<ShippingAddress | null>;
    // (undocumented)
    countryId: ComputedRef<string | undefined>;
    // (undocumented)
    currency: ComputedRef<Currency | null>;
    // (undocumented)
    onCurrencyChange: (fn: (params: {
        currency: Currency;
    }) => void) => void;
    // (undocumented)
    onPaymentMethodChange: (fn: (params: {
        paymentMethod: PaymentMethod;
    }) => void) => void;
    // (undocumented)
    onShippingMethodChange: (fn: (params: {
        shippingMethod: ShippingMethod;
    }) => void) => void;
    // (undocumented)
    paymentMethod: ComputedRef<PaymentMethod | null>;
    // (undocumented)
    refreshSessionContext: () => Promise<void>;
    // (undocumented)
    sessionContext: ComputedRef<SessionContext | null>;
    // (undocumented)
    setActiveBillingAddress: (address: Partial<BillingAddress>) => Promise<void>;
    // (undocumented)
    setActiveShippingAddress: (address: Partial<ShippingAddress>) => Promise<void>;
    // (undocumented)
    setCurrency: (currency: Partial<Currency>) => Promise<void>;
    // (undocumented)
    setPaymentMethod: (paymentMethod: Partial<PaymentMethod>) => Promise<void>;
    // (undocumented)
    setShippingMethod: (shippingMethod: Partial<ShippingMethod>) => Promise<void>;
    // (undocumented)
    shippingMethod: ComputedRef<ShippingMethod | null>;
}

// @beta
export interface IUseUser {
    // (undocumented)
    country: Ref<Country | null>;
    // (undocumented)
    error: ComputedRef<any>;
    // (undocumented)
    errors: UnwrapRef<{
        login: ShopwareError[];
        register: ShopwareError[];
        updateEmail: ShopwareError[];
    }>;
    // (undocumented)
    isCustomerSession: ComputedRef<boolean>;
    // (undocumented)
    isGuestSession: ComputedRef<boolean>;
    // (undocumented)
    isLoggedIn: ComputedRef<boolean>;
    // (undocumented)
    loadCountry: (countryId: string) => Promise<void>;
    // (undocumented)
    loading: ComputedRef<boolean>;
    // (undocumented)
    loadSalutation: (salutationId: string) => Promise<void>;
    // (undocumented)
    login: ({ username, password, }: {
        username?: string;
        password?: string;
    }) => Promise<boolean>;
    // (undocumented)
    logout: () => Promise<void>;
    onLogout: (fn: () => void) => void;
    // (undocumented)
    onUserLogin: (fn: (params: {
        customer: Customer;
    }) => void) => void;
    // (undocumented)
    onUserRegister: (fn: () => void) => void;
    // (undocumented)
    refreshUser: () => Promise<void>;
    // (undocumented)
    register: ({}: CustomerRegistrationParams) => Promise<boolean>;
    // (undocumented)
    salutation: Ref<Salutation | null>;
    // (undocumented)
    updateEmail: (updateEmailData: CustomerUpdateEmailParam) => Promise<boolean>;
    // (undocumented)
    updatePersonalInfo: (personals: CustomerUpdateProfileParam) => Promise<boolean>;
    // (undocumented)
    user: ComputedRef<Partial<Customer> | null>;
}

// @beta
export interface IUseWishlist {
    // (undocumented)
    addToWishlist: () => void;
    // (undocumented)
    clearWishlist: () => void;
    // (undocumented)
    count: Ref<number>;
    // (undocumented)
    isInWishlist: Ref<boolean>;
    // (undocumented)
    items: Ref<string[]>;
    // (undocumented)
    onAddToWishlist: (fn: (params: {
        product: Product;
    }) => void) => void;
    // (undocumented)
    removeFromWishlist: (id: string) => void;
}

// @beta (undocumented)
export type ListingType = "productSearchListing" | "categoryListing";

// @beta (undocumented)
interface Notification_2 {
    // (undocumented)
    id?: number;
    // (undocumented)
    message: string;
    // (undocumented)
    type: "info" | "warning" | "success" | "danger";
}
export { Notification_2 as Notification }

// @beta (undocumented)
export type Search = (path: string, associations?: any) => any;

// @beta (undocumented)
export interface ShopwareDomain {
    // (undocumented)
    currencyId: string;
    // (undocumented)
    domainId: string;
    // (undocumented)
    host: string;
    // (undocumented)
    languageId: string;
    // (undocumented)
    languageLabel: string;
    // (undocumented)
    languageLocaleCode: string;
    // (undocumented)
    languageName: string;
    // (undocumented)
    origin: string;
    // (undocumented)
    pathPrefix: string;
    // (undocumented)
    snippetSetId: string;
    // (undocumented)
    url: string;
}

// @beta (undocumented)
export const ShopwareVuePlugin: (_Vue: any, pluginOptions: {
    enableDevtools: boolean;
}) => void;

// @beta (undocumented)
export type SwInterceptor = {
    name: string;
    handler: IInterceptorCallbackFunction;
};

// @beta (undocumented)
export type SwInterceptors = {
    [broadcastKey: string]: Array<SwInterceptor>;
};

// @beta
export type SwRouting = {
    availableDomains: ShopwareDomain[];
    fallbackDomain?: string;
    fallbackLocale?: string;
    getCurrentDomain: ComputedRef<ShopwareDomain>;
    setCurrentDomain: (domainData: any) => void;
    getUrl: (path: string) => string;
    getAbsoluteUrl: (path: string) => string;
};

// @beta
export function useAddToCart(params: {
    product: Ref<Product> | Product;
}): IUseAddToCart;

// @beta
export function useBreadcrumbs(params?: {
    hideHomeLink: boolean;
}): {
    breadcrumbs: ComputedRef<Breadcrumb[]>;
    setBreadcrumbs: (breadcrumbs: Breadcrumb[]) => void;
    clear: () => void;
};

// @beta
export function useCart(): IUseCart;

// @beta
export function useCheckout(): IUseCheckout;

// @beta (undocumented)
export function useCms(params?: {
    cmsContextName?: string;
}): {
    page: ComputedRef<CmsPageResponse | null>;
    resourceType: ComputedRef<CmsResourceType | null>;
    resourceIdentifier: ComputedRef<string | null>;
    currentSearchPathKey: ComputedRef<string | null>;
    loading: Ref<boolean>;
    search: (path: string, query?: any) => Promise<void>;
    error: Ref<any>;
};

// @beta (undocumented)
export function useCountries(): IUseCountries;

// @beta (undocumented)
export function useCountry(props: {
    countryId: ComputedRef<string>;
}): IUseCountry;

// @beta (undocumented)
export function useCurrency(): IUseCurrency;

// @beta
export function useCustomerAddresses(): IUseCustomerAddresses;

// @beta
export function useCustomerOrders(): IUseCustomerOrders;

// @beta
export function useCustomerPassword(): IUseCustomerPassword;

// @beta
export function useDefaults(params: {
    defaultsKey: string;
}): {
    getIncludesConfig: () => Includes;
    getAssociationsConfig: () => ShopwareAssociation;
    getDefaults: () => ShopwareSearchParams;
};

// @public
export function useIntercept(): {
    broadcast: (broadcastKey: string, value?: any) => void;
    intercept: (broadcastKey: string, handler: IInterceptorCallbackFunction) => void;
    disconnect: (broadcastKey: string, interceptor: string | IInterceptorCallbackFunction) => void;
    on: (params: {
        broadcastKey: string;
        name: string;
        handler: IInterceptorCallbackFunction;
    }) => void;
};

// @beta (undocumented)
export function useListing(params?: {
    listingType: ListingType;
}): IUseListing<Product>;

// @beta
export function useNavigation(params?: {
    type?: StoreNavigationType;
}): IUseNavigation;

// @beta (undocumented)
export function useNotifications(): {
    notifications: ComputedRef<Notification_2[]>;
    removeOne: (id: number) => void;
    removeAll: () => void;
    pushInfo: (message: string, options?: any) => void;
    pushWarning: (message: string, options?: any) => void;
    pushError: (message: string, options?: any) => void;
    pushSuccess: (message: string, options?: any) => void;
};

// @beta
export function useOrderDetails(params: {
    order: Ref<Order> | Order;
}): {
    order: ComputedRef<Order | undefined | null>;
    status: ComputedRef<string | undefined>;
    total: ComputedRef<number | undefined>;
    subtotal: ComputedRef<number | undefined>;
    shippingCosts: ComputedRef<number | undefined>;
    shippingAddress: ComputedRef<ShippingAddress | undefined>;
    billingAddress: ComputedRef<BillingAddress | undefined>;
    personalDetails: ComputedRef<{
        email: string | undefined;
        firstName: string | undefined;
        lastName: string | undefined;
    }>;
    paymentUrl: Ref<null | string>;
    shippingMethod: ComputedRef<ShippingMethod | undefined | null>;
    paymentMethod: ComputedRef<PaymentMethod | undefined | null>;
    errors: UnwrapRef<{
        [key: string]: ShopwareError[];
    }>;
    loaders: UnwrapRef<{
        [key: string]: boolean;
    }>;
    loadOrderDetails: () => void;
    handlePayment: (successUrl?: string, errorUrl?: string) => void;
    cancel: () => Promise<void>;
    changePaymentMethod: (paymentMethodId: string) => Promise<void>;
};

// @beta (undocumented)
export function useProduct(params?: {
    product?: Ref<Product> | Product;
}): IUseProduct<Product, Search>;

// @beta
export function useProductAssociations(params: {
    product: Ref<Product> | Product;
    associationContext: "cross-selling" | "reviews";
}): IUseProductAssociations;

// @beta
export function useProductConfigurator(params: {
    product: Ref<Product> | Product;
}): IUseProductConfigurator;

// @beta (undocumented)
export function useProductQuickSearch(): IUseProductQuickSearch;

// @beta (undocumented)
export function useSalutations(): IUseSalutations;

// @beta
export function useSessionContext(): IUseSessionContext;

// @public
export function useSharedState(): {
    sharedRef: <T>(uniqueKey: string, defaultValue?: T | undefined) => WritableComputedRef<T | null>;
    preloadRef: (refObject: Ref<unknown>, callback: () => Promise<void>) => Promise<void>;
};

// @beta
export function useUIState(params?: {
    stateName?: Ref<string> | string;
}): {
    isOpen: ComputedRef<boolean>;
    switchState: (to?: boolean) => void;
};

// @beta
export function useUser(): IUseUser;

// @alpha
export function useVueContext(): {
    isVueComponent: boolean;
    isVueScope: boolean;
};

// @beta (undocumented)
export function useWishlist(params?: {
    product?: Product | Ref<Product>;
}): IUseWishlist;

```