<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@eurisko/notifications-node](./notifications-node.md) &gt; [MailDataType](./notifications-node.maildatatype.md)

## MailDataType type

**Signature:**

```typescript
export type MailDataType = {
    to: string[];
    cc?: string[];
    bcc?: string[];
    body: string;
    subject: string;
    templateParams?: any;
    isHTML?: boolean;
    template?: string;
    attachments?: AttachmentType[];
};
```
**References:** [AttachmentType](./notifications-node.attachmenttype.md)

