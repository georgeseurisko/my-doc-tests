<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@eurisko/notifications-node](./notifications-node.md) &gt; [getUserNotifications](./notifications-node.getusernotifications.md)

## getUserNotifications variable

Function that returns a users saved notifications

**Signature:**

```typescript
getUserNotifications: (userId: Types.ObjectId, { page, limit, language, sortOrder, sortField, filter }: GetNotificationsType) => Promise<{
    data: any[];
    currentPage: number;
    totalPages: number;
    documentsPerPage: number;
    totalDocuments: number;
}>
```
