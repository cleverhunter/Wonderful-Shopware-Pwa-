<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@shopware-pwa/composables](./composables.md) &gt; [useNotifications](./composables.usenotifications.md)

## useNotifications() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 


<b>Signature:</b>

```typescript
export declare function useNotifications(): {
    notifications: ComputedRef<Notification[]>;
    removeOne: (id: number) => void;
    removeAll: () => void;
    pushInfo: (message: string, options?: any) => void;
    pushWarning: (message: string, options?: any) => void;
    pushError: (message: string, options?: any) => void;
    pushSuccess: (message: string, options?: any) => void;
};
```
<b>Returns:</b>

{ notifications: ComputedRef&lt;Notification\[\]&gt;; removeOne: (id: number) =&gt; void; removeAll: () =&gt; void; pushInfo: (message: string, options?: any) =&gt; void; pushWarning: (message: string, options?: any) =&gt; void; pushError: (message: string, options?: any) =&gt; void; pushSuccess: (message: string, options?: any) =&gt; void; }
